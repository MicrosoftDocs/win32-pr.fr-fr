---
description: La reconnaissance du système de fichiers est la possibilité de reconnaître les supports de stockage qui contiennent une disposition de volume/système de fichiers valide qui n’a pas encore été définie, mais le média est en mesure de s’identifier via la présence de la structure de reconnaissance définie en interne par Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Obtention d’informations sur la reconnaissance du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318693"
---
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="725d7-103">Obtention d’informations sur la reconnaissance du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="725d7-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="725d7-104">La [reconnaissance du système de fichiers](file-system-recognition.md) est la possibilité de reconnaître les supports de stockage qui contiennent une disposition de volume/système de fichiers valide qui n’a pas encore été définie, mais le média est en mesure de s’identifier via la présence de la structure de reconnaissance définie en interne par Windows.</span><span class="sxs-lookup"><span data-stu-id="725d7-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="725d7-105">Dans la mesure où aucun système de fichiers existant ne reconnaît une nouvelle disposition de disque, le système de fichiers « brut » monte le volume et fournit un accès direct au niveau du bloc.</span><span class="sxs-lookup"><span data-stu-id="725d7-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="725d7-106">Le système de fichiers « brut », incorporé dans *NtosKrnl*, a la capacité de lire la structure de reconnaissance du système de fichiers et de fournir aux applications un accès à ces structures par le biais de la demande de contrôle du système de fichiers [**FSCTL la reconnaissance du système de \_ \_ fichiers de \_ \_ requête**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="725d7-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="725d7-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="725d7-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="725d7-108">Reconnaissance du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="725d7-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="725d7-109">**\_structure de \_ reconnaissance du système de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="725d7-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="725d7-110">**\_reconnaissance du \_ système de fichiers de requête FSCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="725d7-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
