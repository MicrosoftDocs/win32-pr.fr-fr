---
title: Envoi du fichier à l’appareil
description: Envoi du fichier à l’appareil
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Gestionnaire de périphériques Windows Media, envoyer des fichiers aux appareils
- Gestionnaire de périphériques, envoi de fichiers aux appareils
- Guide de programmation, envoi de fichiers aux appareils
- applications de bureau, envoyer des fichiers aux appareils
- création d’applications Windows Media Gestionnaire de périphériques, envoi de fichiers aux appareils
- écriture de fichiers sur des appareils, envoi de fichiers à des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507259"
---
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="818b5-109">Envoi du fichier à l’appareil</span><span class="sxs-lookup"><span data-stu-id="818b5-109">Sending the File to the Device</span></span>

<span data-ttu-id="818b5-110">Une fois que le fichier a été transcodé si nécessaire, et que toutes les métadonnées, y compris le format, ont été définies, votre application peut envoyer le fichier à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="818b5-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="818b5-111">Pour ce faire, vous devez d’abord obtenir une interface **IWMDMStorageControl** (ou une version ultérieure) pour un emplacement cible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="818b5-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="818b5-112">Les indicateurs d' **insertion** spécifient si le nouveau stockage doit être un frère ou un enfant de la cible.</span><span class="sxs-lookup"><span data-stu-id="818b5-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="818b5-113">Une fois que vous avez obtenu la cible, vous pouvez appeler [**IWMDMStorageControl :: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2 :: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)ou [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) pour transférer le fichier.</span><span class="sxs-lookup"><span data-stu-id="818b5-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="818b5-114">L’application peut gérer la lecture des données de fichier elles-mêmes en implémentant [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), ou elle peut permettre à la méthode **Insert** de lire et de transférer le fichier automatiquement en ne fournissant pas de pointeur vers un **IWMDMOperation** implémenté par l’application.</span><span class="sxs-lookup"><span data-stu-id="818b5-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="818b5-115">Le code C++ suivant illustre l’appel de **Insert3** pour écrire un fichier sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="818b5-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="818b5-116">Si le pointeur *pOperation* passé à **Insert3** a la **valeur null**, le fichier est envoyé en une seule étape. Si ce pointeur est un pointeur d’interface valide, Windows Media Gestionnaire de périphériques appellera votre méthode de rappel pour obtenir des données en blocs.</span><span class="sxs-lookup"><span data-stu-id="818b5-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="818b5-117">Pour plus d’informations sur l’implémentation de **IWMDMOperation**, consultez [gestion manuelle des transferts de fichiers](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="818b5-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="818b5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="818b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="818b5-119">**Écriture de fichiers sur l’appareil**</span><span class="sxs-lookup"><span data-stu-id="818b5-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




