---
title: Lecture des fichiers à partir de l’appareil
description: Lecture des fichiers à partir de l’appareil
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Gestionnaire de périphériques de média, lire des fichiers à partir d’appareils
- Gestionnaire de périphériques, lire des fichiers à partir d’appareils
- Guide de programmation, lire des fichiers à partir d’appareils
- applications de bureau, lire des fichiers à partir d’appareils
- création d’applications Windows Media Gestionnaire de périphériques, lecture de fichiers à partir d’appareils
- lecture de fichiers à partir d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903999"
---
# <a name="reading-files-from-the-device"></a>Lecture des fichiers à partir de l’appareil

Une fois que vous avez trouvé un fichier à copier à partir de l’appareil, vous pouvez copier le fichier de l’appareil vers l’ordinateur en un seul appel, ou utiliser un rappel pour que les octets de fichier soient lus directement dans votre application, qui peut ensuite traiter ou stocker les données à mesure qu’elles s’affichent.

Les étapes suivantes illustrent la façon de copier un fichier à partir d’un appareil en un seul appel :

1.  Obtient un handle du fichier sur l’appareil. Vous pouvez obtenir le handle à l’aide d’une recherche de fichier récursive ou, si vous connaissez l’ID persistant du stockage, en appelant [**IWMDMDevice3 :: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). Dans les deux cas, vous avez besoin de l’interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) de l’objet.
2.  Déterminez si le stockage est un fichier ou un dossier. Seuls les fichiers peuvent être copiés à partir de l’appareil. Appelez [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) pour obtenir les attributs de stockage, ce qui vous indique si le stockage est un fichier ou un dossier.
3.  Interrogez **IWMDMStorage** pour [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)et appelez [**IWMDMStorageControl :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) pour lire le fichier à partir de l’appareil et l’enregistrer à un emplacement spécifié.

Si, à la place, vous souhaitez lire le bloc de fichier par bloc à partir de l’appareil, vous devez implémenter l’interface de rappel [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) . transmettez cette interface dans l’appel **IWMDMStorageControl :: Read** et Windows Media Gestionnaire de périphériques enverra des segments de données de fichier de manière séquentielle à votre rappel. Les étapes suivantes montrent comment lire un bloc de fichiers de périphérique par bloc :

1.  Obtenir l’interface **IWMDMStorage** pour le stockage et déterminer s’il s’agit d’un fichier, comme décrit précédemment.
2.  Préparez les descripteurs de fichiers ou d’autres Handles dont vous avez besoin pour stocker les données reçues.
3.  Interroger l’interface **IWMDMStorageControl** du stockage
4.  Appelez **IWMDMStorageControl :: Read** pour commencer l’opération de lecture, en passant l’interface **IWMDMOperation** que vous avez implémentée.
5.  Windows Media Gestionnaire de périphériques enverra le bloc de données par bloc à votre appareil, comme décrit dans [gestion manuelle des transferts de fichiers](handling-file-transfers-manually.md).

L’exemple de fonction C++ suivant lit un objet de stockage à partir d’un appareil. La fonction accepte un pointeur d’interface **IWMDMOperation** facultatif ; Si elle est envoyée, la fonction crée un fichier explicitement et gère l’écriture des données dans le fichier lors de son implémentation de **IWMDMOperation :: TransferObjectData**; Si ce n’est pas le cas, il lit le fichier et l’enregistre dans la destination spécifiée par *pwszDestName*.


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




