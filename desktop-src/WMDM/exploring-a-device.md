---
title: Exploration d’un appareil
description: Exploration d’un appareil
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Gestionnaire de périphériques, exploration des appareils
- Gestionnaire de périphériques, exploration des appareils
- Guide de programmation, exploration des appareils
- applications de bureau, exploration des appareils
- création d’applications Windows Media Gestionnaire de périphériques, exploration des appareils
- exploration des appareils
- stockages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379981"
---
# <a name="exploring-a-device"></a><span data-ttu-id="29c6d-110">Exploration d’un appareil</span><span class="sxs-lookup"><span data-stu-id="29c6d-110">Exploring a Device</span></span>

<span data-ttu-id="29c6d-111">L’exploration d’un appareil est similaire à l’exploration d’un lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="29c6d-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="29c6d-112">Tous les objets sur un appareil sont appelés « *stockages*».</span><span class="sxs-lookup"><span data-stu-id="29c6d-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="29c6d-113">Un stockage peut être un fichier, un dossier ou un objet abstrait (par exemple, une sélection) sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29c6d-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="29c6d-114">Vous devez examiner les attributs et les métadonnées d’un stockage (si pris en charge) pour comprendre le type de stockage.</span><span class="sxs-lookup"><span data-stu-id="29c6d-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="29c6d-115">Les stockages sont organisés de manière hiérarchique sur l’appareil. chaque stockage a exactement un parent et tous les stockages sont finalement décroissants d’un stockage d’appareil racine unique, généralement nommé « \\ ».</span><span class="sxs-lookup"><span data-stu-id="29c6d-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="29c6d-116">Les étapes suivantes décrivent comment explorer un appareil :</span><span class="sxs-lookup"><span data-stu-id="29c6d-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="29c6d-117">Obtenir l’interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) d’un appareil, comme décrit dans la section [énumération des appareils](enumerating-devices.md).</span><span class="sxs-lookup"><span data-stu-id="29c6d-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="29c6d-118">Appelez [**IWMDMDevice :: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) pour récupérer une interface [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="29c6d-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="29c6d-119">Cette interface est utilisée pour récupérer tous les objets enfants du stockage qui retourne cette interface.</span><span class="sxs-lookup"><span data-stu-id="29c6d-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="29c6d-120">Lors de l’obtention de cette interface à partir de l’appareil, comme nous sommes ici, il ne contiendra qu’un seul stockage : le stockage de l’appareil racine.</span><span class="sxs-lookup"><span data-stu-id="29c6d-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="29c6d-121">Appelez [**IWMDMEnumStorage :: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) avec un nombre de 1 pour récupérer l’interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) pour le stockage de l’appareil racine.</span><span class="sxs-lookup"><span data-stu-id="29c6d-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="29c6d-122">(Vous ne pouvez pas demander plus d’un enfant de l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="29c6d-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="29c6d-123">Examinez tous les stockages sur l’appareil en appelant de manière récursive [**IWMDMStorage :: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) , puis **IWMDMEnumStorage :: Next** pour obtenir les enfants d’un stockage.</span><span class="sxs-lookup"><span data-stu-id="29c6d-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="29c6d-124">Pour voir si un stockage a des enfants pour éviter les appels à **EnumStorage** et **Next**, vous pouvez appeler [**IWMDMStorage :: GETATTRIBUTES**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) pour rechercher les indicateurs WMDM \_ Storage \_ attr \_ contient des \_ fichiers ou WMDM \_ Storage \_ attr contient des \_ \_ dossiers.</span><span class="sxs-lookup"><span data-stu-id="29c6d-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="29c6d-125">Pour plus d’informations sur la façon d’obtenir les propriétés d’un stockage, consultez [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md) et [obtention et définition des métadonnées et des attributs dans l’application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="29c6d-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="29c6d-126">Windows Media Gestionnaire de périphériques n’expose pas un ensemble standard de dossiers pour stocker les éléments multimédias d’un type spécifique (par exemple, un dossier « Mes playlists » pour les playlists).</span><span class="sxs-lookup"><span data-stu-id="29c6d-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="29c6d-127">Chaque appareil possède un système de fichiers unique, et vous devez choisir un emplacement approprié pour rechercher ou envoyer un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="29c6d-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="29c6d-128">L’Explorateur Windows peut afficher des dossiers virtuels qui n’existent pas réellement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29c6d-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="29c6d-129">Les dossiers virtuels sont, par exemple, les dossiers « Media » et « Data » affichés pour les appareils MTP.</span><span class="sxs-lookup"><span data-stu-id="29c6d-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="29c6d-130">Ces dossiers sont créés par Windows pour simplifier les téléchargements pour les utilisateurs finaux. ils n’existent pas réellement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29c6d-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="29c6d-131">Votre application ne doit pas dépendre de la recherche de ces types de dossiers généraux.</span><span class="sxs-lookup"><span data-stu-id="29c6d-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="29c6d-132">À l’inverse, l’Explorateur Windows peut ne pas afficher certains dossiers ou objets qui existent sur l’appareil (par exemple, les sélections).</span><span class="sxs-lookup"><span data-stu-id="29c6d-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="29c6d-133">L’exemple de code C++ suivant illustre l’exploration récursive d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="29c6d-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="29c6d-134">Il utilise deux fonctions :</span><span class="sxs-lookup"><span data-stu-id="29c6d-134">It uses two functions:</span></span>

-   <span data-ttu-id="29c6d-135">ExploreDevice, une fonction de démarrage qui reçoit un pointeur d’appareil et obtient un pointeur vers l’énumérateur racine de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="29c6d-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="29c6d-136">RecursiveExploreStorage, qui est appelé pour explorer un appareil de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="29c6d-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="29c6d-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29c6d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29c6d-138">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="29c6d-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




