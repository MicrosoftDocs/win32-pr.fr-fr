---
title: Prise en charge du contenu côté appareil (feuille)
description: Découvrez comment utiliser l’API de shell Windows ou l’API WPD pour obtenir des données pour les objets d’appareil, qui n’est pas accessible via le système de fichiers dans Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404192"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="69f9c-103">Prise en charge du contenu côté appareil</span><span class="sxs-lookup"><span data-stu-id="69f9c-103">Supporting device-side content</span></span>

<span data-ttu-id="69f9c-104">Étant donné que le contenu côté appareil n’est pas accessible par le biais du système de fichiers dans Windows Vista, vous devez utiliser l’API shell Windows ou l’API WPD pour récupérer des données pour les objets périphérique.</span><span class="sxs-lookup"><span data-stu-id="69f9c-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="69f9c-105">Il s’agit de la principale différence entre un gestionnaire de feuille de propriétés normal et un gestionnaire de feuille de propriétés WPD.</span><span class="sxs-lookup"><span data-stu-id="69f9c-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="69f9c-106">L’exemple de code suivant illustre la récupération du contenu côté appareil à l’aide de l’API du shell Windows.</span><span class="sxs-lookup"><span data-stu-id="69f9c-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="69f9c-107">La première étape est l’initialisation de la liste d’identificateurs d’élément ou de PIDL.</span><span class="sxs-lookup"><span data-stu-id="69f9c-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="69f9c-108">(Cette liste contient l’identificateur unique pour l’objet d’appareil donné.)</span><span class="sxs-lookup"><span data-stu-id="69f9c-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



<span data-ttu-id="69f9c-109">La fonction d’initialisation appelle la \_ fonction ExaminePIDLArray, qui récupère les propriétés de l’objet identifié par un PIDL dans le tableau PIDL.</span><span class="sxs-lookup"><span data-stu-id="69f9c-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



<span data-ttu-id="69f9c-110">En plus de l’initialisation et du traitement de la liste d’identificateurs d’élément, votre application doit implémenter la méthode IShellPropSheetExt :: ReplacePage et insérer les gestionnaires de remplacement appropriés.</span><span class="sxs-lookup"><span data-stu-id="69f9c-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="69f9c-111">Le shell Windows appelle cette méthode chaque fois qu’il est sur le point d’afficher une feuille de propriétés remplaçable, donnant à votre application la possibilité d’appeler un gestionnaire de remplacement correspondant.</span><span class="sxs-lookup"><span data-stu-id="69f9c-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="69f9c-112">Le mot de poids faible du premier paramètre de la méthode ReplacePage est un identificateur pour la feuille de propriétés donnée que Windows va afficher.</span><span class="sxs-lookup"><span data-stu-id="69f9c-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="69f9c-113">Les valeurs passées dans le mot de poids faible du premier paramètre correspondent aux valeurs définies dans le fichier WpdShellExtension. h.</span><span class="sxs-lookup"><span data-stu-id="69f9c-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="69f9c-114">Ces valeurs et leurs descriptions apparaissent dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69f9c-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="69f9c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="69f9c-115">Value</span></span>                                  | <span data-ttu-id="69f9c-116">Description</span><span class="sxs-lookup"><span data-stu-id="69f9c-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="69f9c-117">WPDNSE \_ PROPSHEET \_ appareil \_ général</span><span class="sxs-lookup"><span data-stu-id="69f9c-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="69f9c-118">Correspond à l’onglet général de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="69f9c-119">\_ \_ stockage général WPDNSE \_ PROPSHEET</span><span class="sxs-lookup"><span data-stu-id="69f9c-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="69f9c-120">Correspond à l’onglet général pour un objet de stockage trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="69f9c-121">WPDNSE \_ PROPSHEET \_ contenu \_ général</span><span class="sxs-lookup"><span data-stu-id="69f9c-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="69f9c-122">Correspond à l’onglet général pour l’objet de contenu trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="69f9c-123">\_références de \_ contenu WPDNSE PROPSHEET \_</span><span class="sxs-lookup"><span data-stu-id="69f9c-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="69f9c-124">Correspond à l’onglet Références pour un objet de contenu trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="69f9c-125">\_ressources de \_ contenu WPDNSE PROPSHEET \_</span><span class="sxs-lookup"><span data-stu-id="69f9c-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="69f9c-126">Correspond à l’onglet ressources pour un objet de contenu trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="69f9c-127">\_Détails du \_ contenu WPDNSE PROPSHEET \_</span><span class="sxs-lookup"><span data-stu-id="69f9c-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="69f9c-128">Correspond à un onglet Détails pour un objet de contenu trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="69f9c-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="69f9c-129">Dans l’exemple d’extension de la feuille de propriétés, la méthode ReplacePage appelle deux gestionnaires \_ de remplacement : ReplaceDeviceGeneral et \_ ReplaceContentReferences.</span><span class="sxs-lookup"><span data-stu-id="69f9c-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="69f9c-130">Ces gestionnaires remplacent les onglets général du périphérique et références du contenu dans les feuilles de propriétés extensibles.</span><span class="sxs-lookup"><span data-stu-id="69f9c-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



<span data-ttu-id="69f9c-131">Étant donné qu’un utilisateur peut sélectionner plusieurs appareils, une application doit enregistrer le tableau PIDL retourné par IShellExtInit :: Initialize, puis examiner le mot haut du premier paramètre de ReplacePage.</span><span class="sxs-lookup"><span data-stu-id="69f9c-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="69f9c-132">Une valeur de zéro dans ce mot haute correspond au premier élément dans le tableau PIDL, la valeur un correspond au deuxième élément, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="69f9c-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="69f9c-133">Dans la fonction ReplacePage de l’exemple d’application, cette valeur de mot haute est passée aux deux gestionnaires de remplacement.</span><span class="sxs-lookup"><span data-stu-id="69f9c-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="69f9c-134">Ces gestionnaires utilisent ensuite cette valeur pour identifier un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="69f9c-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69f9c-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69f9c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f9c-136">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="69f9c-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



