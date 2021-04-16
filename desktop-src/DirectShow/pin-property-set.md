---
description: Épingler le jeu de propriétés
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Épingler le jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392504"
---
# <a name="pin-property-set"></a><span data-ttu-id="a1ed9-103">Épingler le jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a1ed9-103">Pin Property Set</span></span>

<span data-ttu-id="a1ed9-104">La propriété pin définie renvoie la catégorie pin d’un code confidentiel sur un filtre.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="a1ed9-105">La catégorie est définie par le filtre lorsqu’elle crée le code confidentiel. la catégorie indique le type de données que le code confidentiel est remis ou reçoit par ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="a1ed9-106">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a1ed9-106">Property Set GUID</span></span> | <span data-ttu-id="a1ed9-107">**\_Code PIN AMPROPSETID**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="a1ed9-108">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="a1ed9-108">Property ID</span></span>                   | <span data-ttu-id="a1ed9-109">Description</span><span class="sxs-lookup"><span data-stu-id="a1ed9-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="a1ed9-110">**\_catégorie de code confidentiel AMPROPERTY \_**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="a1ed9-111">Spécifie la catégorie d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="a1ed9-112">DirectShow définit les catégories de code confidentiel suivantes dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="a1ed9-113">GUID de la catégorie</span><span class="sxs-lookup"><span data-stu-id="a1ed9-113">Category GUID</span></span>                     | <span data-ttu-id="a1ed9-114">Description</span><span class="sxs-lookup"><span data-stu-id="a1ed9-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ed9-115">**PIN \_ catégorie \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="a1ed9-116">Broche d’entrée du filtre de capture qui prend le analogique et le numérise.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a1ed9-117">**ÉPINGLer la \_ capture de catégorie \_**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="a1ed9-118">Code PIN de capture.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a1ed9-119">**ÉPINGLer la \_ catégorie \_ CC**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="a1ed9-120">Code PIN fournissant les données de sous-titrage de la ligne 21.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a1ed9-121">**ÉPINGLer la \_ catégorie \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="a1ed9-122">Code confidentiel fournissant des Data Services étendues (lignes 21, même champs).</span><span class="sxs-lookup"><span data-stu-id="a1ed9-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a1ed9-123">**PIN \_ catégorie \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="a1ed9-124">Code PIN fournissant des données standard Videotext de l’Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a1ed9-125">**Aperçu de la \_ catégorie pin \_**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="a1ed9-126">Code pin d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a1ed9-127">**catégorie de PIN \_ \_ toujours**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="a1ed9-128">Code confidentiel qui fournit une image continue.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-128">Pin that provides a still image.</span></span> <span data-ttu-id="a1ed9-129">Le code PIN de capture du filtre doit être connecté avant que le code confidentiel d’image continue soit connecté.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="a1ed9-130">**ÉPINGLer la \_ catégorie \_ télétexte**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="a1ed9-131">Code confidentiel fournissant du télétexte (variante de sous-titrage).</span><span class="sxs-lookup"><span data-stu-id="a1ed9-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a1ed9-132">**code \_ temporel de la catégorie pin \_**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="a1ed9-133">Code PIN fournissant les données de code temporel.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a1ed9-134">**BROCHE \_ catégorie \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="a1ed9-135">Code PIN fournissant les données de l’intervalle de l’occultation vertical.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a1ed9-136">**PIN \_ catégorie \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="a1ed9-137">Broche de sortie vidéo à connecter à la broche d’entrée zéro dans le [mélangeur de superposition](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a1ed9-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="a1ed9-138">**BROCHE \_ catégorie \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="a1ed9-139">Code confidentiel à connecter à l' [allocateur de surface VBI](vbi-surface-allocator.md), filtre d’allocateur de surface VBI requis pour allouer la mémoire vidéo correcte pour des éléments tels que les superpositions de sous-titrage dans les scénarios où un port vidéo est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="a1ed9-140">Les scénarios PCI, IEEE 1394 et USB n’utilisent pas ce filtre.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="a1ed9-141">**\_ \_ capture CC de la vidéo PINNAME \_**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="a1ed9-142">Découpage matériel fermé-code confidentiel</span><span class="sxs-lookup"><span data-stu-id="a1ed9-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="a1ed9-143">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="a1ed9-144">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="a1ed9-144">Example Code</span></span>

<span data-ttu-id="a1ed9-145">Le code suivant montre comment vérifier si un code PIN prend en charge ce jeu de propriétés et, le cas échéant, comment obtenir la catégorie de code confidentiel :</span><span class="sxs-lookup"><span data-stu-id="a1ed9-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="a1ed9-146">Cet exemple utilise la fonction [SafeRelease](../medfound/saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a1ed9-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1ed9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ed9-148">Exigences de code confidentiel pour les filtres de capture</span><span class="sxs-lookup"><span data-stu-id="a1ed9-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="a1ed9-149">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="a1ed9-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="a1ed9-150">Utilisation des catégories de code confidentiel</span><span class="sxs-lookup"><span data-stu-id="a1ed9-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
