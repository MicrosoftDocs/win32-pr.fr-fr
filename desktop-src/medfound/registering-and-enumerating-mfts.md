---
description: Cette section décrit comment énumérer Media Foundation transformations et comment inscrire une table MFT personnalisée afin que les applications puissent la découvrir.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Inscription et énumération de MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951477"
---
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="14e5b-103">Inscription et énumération de MFTs</span><span class="sxs-lookup"><span data-stu-id="14e5b-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="14e5b-104">Cette section décrit comment énumérer Media Foundation transformations et comment inscrire une table MFT personnalisée afin que les applications puissent la découvrir.</span><span class="sxs-lookup"><span data-stu-id="14e5b-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="14e5b-105">Énumération de MFTs</span><span class="sxs-lookup"><span data-stu-id="14e5b-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="14e5b-106">Inscription de MFTs</span><span class="sxs-lookup"><span data-stu-id="14e5b-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="14e5b-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14e5b-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="14e5b-108">Énumération de MFTs</span><span class="sxs-lookup"><span data-stu-id="14e5b-108">Enumerating MFTs</span></span>

<span data-ttu-id="14e5b-109">Pour découvrir les MFTs enregistrés sur le système, une application peut appeler la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="14e5b-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="14e5b-110">Cette fonction requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14e5b-110">This function requires to Windows 7.</span></span> <span data-ttu-id="14e5b-111">Avant Windows 7, les applications devaient utiliser la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) à la place.</span><span class="sxs-lookup"><span data-stu-id="14e5b-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="14e5b-112">Cette fonction prend les informations suivantes comme entrée :</span><span class="sxs-lookup"><span data-stu-id="14e5b-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="14e5b-113">Catégorie de MFT à énumérer, telle que le décodeur vidéo ou le décodeur audio.</span><span class="sxs-lookup"><span data-stu-id="14e5b-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="14e5b-114">Format d’entrée ou de sortie à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="14e5b-114">An input or output format to match.</span></span>
-   <span data-ttu-id="14e5b-115">Indicateurs qui spécifient des conditions de recherche supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="14e5b-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="14e5b-116">La fonction retourne un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , chacun représentant une table MFT qui correspond aux critères d’énumération.</span><span class="sxs-lookup"><span data-stu-id="14e5b-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="14e5b-117">Par exemple, le code suivant énumère Windows Media Video décodeurs :</span><span class="sxs-lookup"><span data-stu-id="14e5b-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



<span data-ttu-id="14e5b-118">Par défaut, certains types de MFT sont exclus de l’énumération, y compris MFTs asynchrones, matériel MFTs et MFTs avec des réstructs de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="14e5b-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="14e5b-119">Celles-ci sont exclues, car elles nécessitent toutes un traitement particulier.</span><span class="sxs-lookup"><span data-stu-id="14e5b-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="14e5b-120">Utilisez le paramètre *Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour modifier la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="14e5b-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="14e5b-121">Par exemple, pour inclure le matériel MFTs dans les résultats de l’énumération, définissez l’indicateur de **\_ \_ \_ matériel indicateur** d’énumération MFT :</span><span class="sxs-lookup"><span data-stu-id="14e5b-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a><span data-ttu-id="14e5b-122">Inscription de MFTs</span><span class="sxs-lookup"><span data-stu-id="14e5b-122">Registering MFTs</span></span>

<span data-ttu-id="14e5b-123">Lorsque vous inscrivez une Media Foundation transformation (MFT), deux types d’informations sont écrits dans le registre :</span><span class="sxs-lookup"><span data-stu-id="14e5b-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="14e5b-124">CLSID de la table MFT, afin que les clients puissent appeler **CoCreateInstance** ou **CoGetClassObject** pour créer une instance de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="14e5b-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="14e5b-125">Cette entrée de Registre suit le format standard pour les fabriques de classes COM.</span><span class="sxs-lookup"><span data-stu-id="14e5b-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="14e5b-126">Pour plus d’informations, consultez la documentation SDK Windows pour le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="14e5b-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="14e5b-127">Informations qui permettent à une application d’énumérer les MFTs par catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="14e5b-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="14e5b-128">Pour créer les entrées d’énumération MFT dans le registre, appelez la fonction [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="14e5b-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="14e5b-129">Vous pouvez inclure les informations suivantes sur la table MFT :</span><span class="sxs-lookup"><span data-stu-id="14e5b-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="14e5b-130">Catégorie de la table MFT, telle que le décodeur vidéo ou l’encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="14e5b-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="14e5b-131">Pour obtenir la liste des catégories, consultez [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="14e5b-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="14e5b-132">Liste des formats d’entrée et de sortie pris en charge par la table MFT.</span><span class="sxs-lookup"><span data-stu-id="14e5b-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="14e5b-133">Chaque format est défini par un type principal et un sous-type.</span><span class="sxs-lookup"><span data-stu-id="14e5b-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="14e5b-134">(Pour obtenir des informations plus détaillées sur le format, le client doit créer la table MFT et appeler les méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) Le chargeur de topologie utilise ces informations lorsqu’il résout une topologie partielle.</span><span class="sxs-lookup"><span data-stu-id="14e5b-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="14e5b-135">Pour supprimer les entrées du Registre, appelez [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="14e5b-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="14e5b-136">Le code suivant montre comment inscrire une table MFT.</span><span class="sxs-lookup"><span data-stu-id="14e5b-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="14e5b-137">Cet exemple suppose que la table MFT est un effet vidéo qui prend en charge les mêmes formats pour les entrées et les sorties.</span><span class="sxs-lookup"><span data-stu-id="14e5b-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="14e5b-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14e5b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e5b-139">Champ des restrictions d’utilisation</span><span class="sxs-lookup"><span data-stu-id="14e5b-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="14e5b-140">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14e5b-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



