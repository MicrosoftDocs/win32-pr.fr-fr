---
title: Envoi du fichier à l’appareil
description: Envoi du fichier à l’appareil
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Gestionnaire de périphériques de média, envoyer des fichiers aux appareils
- Gestionnaire de périphériques, envoi de fichiers aux appareils
- Guide de programmation, envoi de fichiers aux appareils
- applications de bureau, envoyer des fichiers aux appareils
- création d’applications Windows Media Gestionnaire de périphériques, envoi de fichiers à des appareils
- écriture de fichiers sur des appareils, envoi de fichiers à des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a47de872d03d42701ff6e95516a9ead59f1206729ae9ca70d6dd9e5f1260f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124139"
---
# <a name="sending-the-file-to-the-device"></a>Envoi du fichier à l’appareil

Une fois que le fichier a été transcodé si nécessaire, et que toutes les métadonnées, y compris le format, ont été définies, votre application peut envoyer le fichier à l’appareil. Pour ce faire, vous devez d’abord obtenir une interface **IWMDMStorageControl** (ou une version ultérieure) pour un emplacement cible sur l’appareil. Les indicateurs d' **insertion** spécifient si le nouveau stockage doit être un frère ou un enfant de la cible. Une fois que vous avez obtenu la cible, vous pouvez appeler [**IWMDMStorageControl :: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2 :: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)ou [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) pour transférer le fichier. L’application peut gérer la lecture des données de fichier elles-mêmes en implémentant [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), ou elle peut permettre à la méthode **Insert** de lire et de transférer le fichier automatiquement en ne fournissant pas de pointeur vers un **IWMDMOperation** implémenté par l’application.

Le code C++ suivant illustre l’appel de **Insert3** pour écrire un fichier sur un appareil. Si le pointeur *pOperation* passé à **Insert3** a la **valeur null**, le fichier est envoyé en une seule étape. si ce pointeur est un pointeur d’interface valide, Windows Gestionnaire de périphériques multimédia appellera votre méthode de rappel pour obtenir des données en blocs. Pour plus d’informations sur l’implémentation de **IWMDMOperation**, consultez [gestion manuelle des transferts de fichiers](handling-file-transfers-manually.md).


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers sur l’appareil**](writing-files-to-the-device.md)
</dt> </dl>

 

 




