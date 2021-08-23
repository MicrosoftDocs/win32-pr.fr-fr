---
description: La reconnaissance du système de fichiers est la possibilité de reconnaître les supports de stockage qui contiennent une disposition de volume/système de fichiers valide qui n’a pas encore été définie, mais le média est en mesure de s’identifier via la présence de la structure de reconnaissance définie en interne par Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Obtention d’informations sur la reconnaissance du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c10b538f9e98ecab3f8f8f72784ef658c068f780388dc7b600be68b76380757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148504"
---
# <a name="obtaining-file-system-recognition-information"></a>Obtention d’informations sur la reconnaissance du système de fichiers

La [reconnaissance du système de fichiers](file-system-recognition.md) est la possibilité de reconnaître les supports de stockage qui contiennent une disposition de volume/système de fichiers valide qui n’a pas encore été définie, mais le média est en mesure de s’identifier via la présence de la structure de reconnaissance définie en interne par Windows.

Dans la mesure où aucun système de fichiers existant ne reconnaît une nouvelle disposition de disque, le système de fichiers « brut » monte le volume et fournit un accès direct au niveau du bloc. Le système de fichiers « brut », incorporé dans *NtosKrnl*, a la capacité de lire la structure de reconnaissance du système de fichiers et de fournir aux applications un accès à ces structures par le biais de la demande de contrôle du système de fichiers [**FSCTL la reconnaissance du système de \_ \_ fichiers de \_ \_ requête**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), comme illustré dans l’exemple suivant.


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Reconnaissance du système de fichiers](file-system-recognition.md)
</dt> <dt>

[**\_structure de \_ reconnaissance du système de fichiers \_**](file-system-recognition-structure.md)
</dt> <dt>

[**\_reconnaissance du \_ système de fichiers de requête FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
