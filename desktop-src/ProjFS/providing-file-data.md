---
title: Envoi de données de fichier
description: Décrit comment un fournisseur fournit des informations d’espace réservé et des données de fichier.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413636"
---
# <a name="providing-file-data"></a>Envoi de données de fichier

Lorsqu’un fournisseur crée d’abord une racine de virtualisation, il est vide sur le système local. Autrement dit, aucun des éléments de la Banque de données de stockage n’a encore été mis en cache sur le disque. À mesure que des éléments sont ouverts, ProjFS demande des informations au fournisseur pour permettre la création d’espaces réservés pour ces éléments dans le système de fichiers local.  Au fur et à mesure de l’accès au contenu des éléments, ProjFS demande ce contenu auprès du fournisseur.  Il en résulte que du point de vue de l’utilisateur, les fichiers et les répertoires virtualisés sont semblables aux fichiers et répertoires normaux qui résident déjà sur le système de fichiers local.

## <a name="placeholder-creation"></a>Création d’espaces réservés

Lorsqu’une application tente d’ouvrir un handle vers un fichier virtualisé, ProjFS appelle le rappel **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** pour chaque élément du chemin d’accès qui n’existe pas encore sur le disque.  Par exemple, si une application tente d’ouvrir `C:\virtRoot\dir1\dir2\file.txt` , mais que seul le chemin `C:\virtRoot\dir1` existe sur le disque, le fournisseur recevra un rappel pour `C:\virtRoot\dir1\dir2` , puis pour `C:\virtRoot\dir1\dir2\file.txt` .

Quand ProjFS appelle le rappel **PRJ_GET_PLACEHOLDER_INFO_CB** du fournisseur, le fournisseur effectue les actions suivantes :

1. Le fournisseur détermine si le nom demandé existe dans le magasin de stockage.  Le fournisseur doit utiliser **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** comme routine de comparaison lors de la recherche de son magasin de stockage pour déterminer si le nom demandé existe dans le magasin de stockage.  Si ce n’est pas le cas, le fournisseur retourne HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) à partir du rappel.

1. Si le nom demandé existe dans le magasin de stockage, le fournisseur remplit une structure [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) avec les métadonnées du système de fichiers de l’élément et appelle **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** pour envoyer les données à ProjFS.  ProjFS utilise ces informations pour créer un espace réservé dans le système de fichiers local pour l’élément.

    > ProjFS utilise tout FILE_ATTRIBUTE indicateurs que le fournisseur définit dans le membre **FileBasicInfo. FileAttributes** de PRJ_PLACEHOLDER_INFO à l’exception de FILE_ATTRIBUTE_DIRECTORY ; Elle définit la valeur correcte pour FILE_ATTRIBUTE_DIRECTORY dans le membre **FileBasicInfo. FileAttributes** en fonction de la valeur fournie du membre **FileBasicInfo. IsDirectory** .

    > Si le magasin de stockage prend en charge les liens symboliques, le fournisseur doit utiliser **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** pour envoyer les données d’espace réservé à ProjFS.  **PrjWritePlaceholderInfo2** prend en charge une entrée de mémoire tampon supplémentaire qui permet au fournisseur de spécifier que l’espace réservé est un lien symbolique et quelle est sa cible.  Elle se comporte autrement comme décrit ci-dessus pour **PrjWritePlaceholderInfo**.  L’exemple suivant illustre l’utilisation de **PrjWritePlaceholderInfo2** pour assurer la prise en charge des liens symboliques.
    >
    > notez que **PrjWritePlaceholderInfo2** est pris en charge à partir de Windows 10, version 2004.  Un fournisseur doit détecter l’existence de **PrjWritePlaceholderInfo2**, par exemple à l’aide de **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a>Fournir le contenu du fichier

Quand ProjFS doit s’assurer qu’un fichier virtualisé contient des données, par exemple lorsqu’une application tente de lire à partir du fichier, ProjFS appelle le rappel **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** pour cet élément afin de demander que le fournisseur fournisse le contenu du fichier.  Le fournisseur récupère les données du fichier à partir de son magasin de stockage et utilise **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** pour envoyer les données au système de fichiers local.

> Quand ProjFS appelle ce rappel, le membre **FilePathName** du paramètre _callbackdata_ fournit le nom du fichier lors de la création de son espace réservé.  Autrement dit, si le fichier a été renommé depuis la création de son espace réservé, le rappel fournit le nom (pré-renommer) d’origine, et non le nom actuel (après le changement de nom).  Si nécessaire, le fournisseur peut utiliser le membre **VERSIONINFO** du paramètre _callbackdata_ pour déterminer les données du fichier qui sont demandées.
>
> Pour plus d’informations sur la façon dont le membre **VERSIONINFO** de PRJ_CALLBACK_DATA peut être utilisé, consultez la documentation de [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) et la rubrique [gestion des modifications d’affichage](handling-view-changes.md) .

Le fournisseur est autorisé à fractionner la plage de données demandée dans le rappel **PRJ_GET_FILE_DATA_CB** en plusieurs appels à **PrjWriteFileData**, chacun fournissant une partie de la plage demandée.  Toutefois, le fournisseur doit fournir l’intégralité de la plage demandée avant de terminer le rappel.  Par exemple, si le rappel demande 10 Mo de données à partir de _byteOffset_ 0 pour la _longueur_ 10 485 760, le fournisseur peut choisir de fournir les données dans 10 appels à **PrjWriteFileData**, chacun d’eux envoyant 1 Mo.

Le fournisseur est également libre de fournir plus que la plage demandée, jusqu’à la longueur du fichier.  La plage que le fournisseur fournit doit couvrir la plage demandée.  Par exemple, si le rappel demande 1 Mo de données à partir de _byteOffset_ 4096 pour la _longueur_ 1 052 672, et que le fichier a une taille totale de 10 Mo, le fournisseur peut choisir de retourner 2 Mo de données en commençant à l’offset 0.

### <a name="buffer-alignment-considerations"></a>Considérations sur l’alignement de la mémoire tampon

ProjFS utilise le [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) de l’appelant qui requiert les données pour écrire les données dans le système de fichiers local.  Toutefois, ProjFS ne peut pas contrôler si ce FILE_OBJECT a été ouvert pour des e/s mises en mémoire tampon ou non.  Si le FILE_OBJECT a été ouvert pour des e/s non mises en mémoire tampon, les lectures et les écritures dans le fichier doivent respecter certaines exigences d’alignement.  Le fournisseur peut répondre à ces exigences d’alignement en procédant de deux façons :

1. Utilisez **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** pour allouer la mémoire tampon à transmettre dans le paramètre de _mémoire tampon_ de **PrjWriteFileData**.
1. Assurez-vous que les paramètres _byteOffset_ et _Length_ de **PrjWriteFileData** sont des multiples de l’exigence d’alignement du dispositif de stockage (Notez que le paramètre de _longueur_ ne doit pas répondre à cette exigence si la   +  _longueur_ de byteOffset est égale à la fin du fichier).  Le fournisseur peut utiliser **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** pour récupérer la spécification d’alignement du périphérique de stockage.

ProjFS le laisse au fournisseur pour calculer l’alignement approprié.  En effet, lors du traitement d’un rappel de **PRJ_GET_FILE_DATA_CB** , le fournisseur peut choisir de retourner les données demandées dans plusieurs appels **PrjWriteFileData** , chacun renvoyant une partie du nombre total de données demandées, avant de terminer le rappel.

> Si le fournisseur va utiliser un seul appel à **PrjWriteFileData** pour écrire l’ensemble du fichier, c’est-à-dire de _byteOffset_ = 0 à _Length_ = taille du fichier, ou pour retourner la plage exacte demandée dans le rappel **PRJ_GET_FILE_DATA_CB** , le fournisseur n’a pas besoin d’effectuer des calculs d’alignement.  Toutefois, il doit toujours utiliser **PrjAllocateAlignedBuffer** pour s’assurer que la _mémoire tampon_ répond aux exigences d’alignement du dispositif de stockage.

Consultez la rubrique [mise en mémoire tampon des fichiers](/windows/desktop/FileIO/file-buffering) pour plus d’informations sur les e/s mises en mémoire tampon et non mises en mémoire tampon.

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```