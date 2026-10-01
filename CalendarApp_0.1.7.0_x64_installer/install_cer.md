```
$cer = Get-ChildItem ".\artifacts\CalendarApp_*_x64_cert.cer" | Sort-Object LastWriteTime -Descending | Select-Object -First 1 -ExpandProperty FullName
Import-Certificate -FilePath $cer -CertStoreLocation Cert:\LocalMachine\Root
Import-Certificate -FilePath $cer -CertStoreLocation Cert:\LocalMachine\TrustedPeople
```