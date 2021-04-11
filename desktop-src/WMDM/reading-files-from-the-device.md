---
title: Lecture des fichiers à partir de l’appareil
description: Lecture des fichiers à partir de l’appareil
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Media Gestionnaire de périphériques, lire des fichiers à partir d’appareils
- Gestionnaire de périphériques, lire des fichiers à partir d’appareils
- Guide de programmation, lire des fichiers à partir d’appareils
- applications de bureau, lire des fichiers à partir d’appareils
- création d’applications Windows Media Gestionnaire de périphériques, lecture de fichiers à partir d’appareils
- lecture de fichiers à partir d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190897"
---
# <a name="reading-files-from-the-device"></a><span data-ttu-id="6b452-109">Lecture des fichiers à partir de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6b452-109">Reading Files from the Device</span></span>

<span data-ttu-id="6b452-110">Une fois que vous avez trouvé un fichier à copier à partir de l’appareil, vous pouvez copier le fichier de l’appareil vers l’ordinateur en un seul appel, ou utiliser un rappel pour que les octets de fichier soient lus directement dans votre application, qui peut ensuite traiter ou stocker les données à mesure qu’elles s’affichent.</span><span class="sxs-lookup"><span data-stu-id="6b452-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="6b452-111">Les étapes suivantes illustrent la façon de copier un fichier à partir d’un appareil en un seul appel :</span><span class="sxs-lookup"><span data-stu-id="6b452-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="6b452-112">Obtient un handle du fichier sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6b452-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="6b452-113">Vous pouvez obtenir le handle à l’aide d’une recherche de fichier récursive ou, si vous connaissez l’ID persistant du stockage, en appelant [**IWMDMDevice3 :: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span><span class="sxs-lookup"><span data-stu-id="6b452-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="6b452-114">Dans les deux cas, vous avez besoin de l’interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b452-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="6b452-115">Déterminez si le stockage est un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="6b452-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="6b452-116">Seuls les fichiers peuvent être copiés à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6b452-116">Only files can be copied from the device.</span></span> <span data-ttu-id="6b452-117">Appelez [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) pour obtenir les attributs de stockage, ce qui vous indique si le stockage est un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="6b452-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="6b452-118">Interrogez **IWMDMStorage** pour [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)et appelez [**IWMDMStorageControl :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) pour lire le fichier à partir de l’appareil et l’enregistrer à un emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b452-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="6b452-119">Si, à la place, vous souhaitez lire le bloc de fichier par bloc à partir de l’appareil, vous devez implémenter l’interface de rappel [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) .</span><span class="sxs-lookup"><span data-stu-id="6b452-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="6b452-120">Transmettez cette interface dans l’appel **IWMDMStorageControl :: Read** , et Windows Media gestionnaire de périphériques enverra des segments de données de fichier de manière séquentielle à votre rappel.</span><span class="sxs-lookup"><span data-stu-id="6b452-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="6b452-121">Les étapes suivantes montrent comment lire un bloc de fichiers de périphérique par bloc :</span><span class="sxs-lookup"><span data-stu-id="6b452-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="6b452-122">Obtenir l’interface **IWMDMStorage** pour le stockage et déterminer s’il s’agit d’un fichier, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="6b452-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="6b452-123">Préparez les descripteurs de fichiers ou d’autres Handles dont vous avez besoin pour stocker les données reçues.</span><span class="sxs-lookup"><span data-stu-id="6b452-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="6b452-124">Interroger l’interface **IWMDMStorageControl** du stockage</span><span class="sxs-lookup"><span data-stu-id="6b452-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="6b452-125">Appelez **IWMDMStorageControl :: Read** pour commencer l’opération de lecture, en passant l’interface **IWMDMOperation** que vous avez implémentée.</span><span class="sxs-lookup"><span data-stu-id="6b452-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="6b452-126">Windows Media Gestionnaire de périphériques enverra le bloc de données par bloc à votre appareil, comme décrit dans [gestion manuelle des transferts de fichiers](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="6b452-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="6b452-127">L’exemple de fonction C++ suivant lit un objet de stockage à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="6b452-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="6b452-128">La fonction accepte un pointeur d’interface **IWMDMOperation** facultatif ; Si elle est envoyée, la fonction crée un fichier explicitement et gère l’écriture des données dans le fichier lors de son implémentation de **IWMDMOperation :: TransferObjectData**; Si ce n’est pas le cas, il lit le fichier et l’enregistre dans la destination spécifiée par *pwszDestName*.</span><span class="sxs-lookup"><span data-stu-id="6b452-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6b452-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b452-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b452-130">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="6b452-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




