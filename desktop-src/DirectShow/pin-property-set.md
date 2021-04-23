---
description: Épingler le jeu de propriétés
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Épingler le jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909617"
---
# <a name="pin-property-set"></a><span data-ttu-id="e37b7-103">Épingler le jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="e37b7-103">Pin Property Set</span></span>

<span data-ttu-id="e37b7-104">La propriété pin définie renvoie la catégorie pin d’un code confidentiel sur un filtre.</span><span class="sxs-lookup"><span data-stu-id="e37b7-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="e37b7-105">La catégorie est définie par le filtre lorsqu’elle crée le code confidentiel. la catégorie indique le type de données que le code confidentiel est remis ou reçoit par ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="e37b7-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="e37b7-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="e37b7-106">Label</span></span> | <span data-ttu-id="e37b7-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="e37b7-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="e37b7-108">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="e37b7-108">Property Set GUID</span></span> | <span data-ttu-id="e37b7-109">**\_Code PIN AMPROPSETID**</span><span class="sxs-lookup"><span data-stu-id="e37b7-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="e37b7-110">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="e37b7-110">Property ID</span></span>                   | <span data-ttu-id="e37b7-111">Description</span><span class="sxs-lookup"><span data-stu-id="e37b7-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="e37b7-112">**\_catégorie de code confidentiel AMPROPERTY \_**</span><span class="sxs-lookup"><span data-stu-id="e37b7-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="e37b7-113">Spécifie la catégorie d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="e37b7-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="e37b7-114">DirectShow définit les catégories de code confidentiel suivantes dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="e37b7-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="e37b7-115">GUID de la catégorie</span><span class="sxs-lookup"><span data-stu-id="e37b7-115">Category GUID</span></span>                     | <span data-ttu-id="e37b7-116">Description</span><span class="sxs-lookup"><span data-stu-id="e37b7-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37b7-117">**PIN \_ catégorie \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="e37b7-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="e37b7-118">Broche d’entrée du filtre de capture qui prend le analogique et le numérise.</span><span class="sxs-lookup"><span data-stu-id="e37b7-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e37b7-119">**ÉPINGLer la \_ capture de catégorie \_**</span><span class="sxs-lookup"><span data-stu-id="e37b7-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="e37b7-120">Code PIN de capture.</span><span class="sxs-lookup"><span data-stu-id="e37b7-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e37b7-121">**ÉPINGLer la \_ catégorie \_ CC**</span><span class="sxs-lookup"><span data-stu-id="e37b7-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="e37b7-122">Code PIN fournissant les données de sous-titrage de la ligne 21.</span><span class="sxs-lookup"><span data-stu-id="e37b7-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e37b7-123">**ÉPINGLer la \_ catégorie \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="e37b7-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="e37b7-124">Code confidentiel fournissant des Data Services étendues (lignes 21, même champs).</span><span class="sxs-lookup"><span data-stu-id="e37b7-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e37b7-125">**PIN \_ catégorie \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="e37b7-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="e37b7-126">Code PIN fournissant des données standard Videotext de l’Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="e37b7-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e37b7-127">**Aperçu de la \_ catégorie pin \_**</span><span class="sxs-lookup"><span data-stu-id="e37b7-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="e37b7-128">Code pin d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e37b7-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e37b7-129">**catégorie de PIN \_ \_ toujours**</span><span class="sxs-lookup"><span data-stu-id="e37b7-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="e37b7-130">Code confidentiel qui fournit une image continue.</span><span class="sxs-lookup"><span data-stu-id="e37b7-130">Pin that provides a still image.</span></span> <span data-ttu-id="e37b7-131">Le code PIN de capture du filtre doit être connecté avant que le code confidentiel d’image continue soit connecté.</span><span class="sxs-lookup"><span data-stu-id="e37b7-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="e37b7-132">**ÉPINGLer la \_ catégorie \_ télétexte**</span><span class="sxs-lookup"><span data-stu-id="e37b7-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="e37b7-133">Code confidentiel fournissant du télétexte (variante de sous-titrage).</span><span class="sxs-lookup"><span data-stu-id="e37b7-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e37b7-134">**code \_ temporel de la catégorie pin \_**</span><span class="sxs-lookup"><span data-stu-id="e37b7-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="e37b7-135">Code PIN fournissant les données de code temporel.</span><span class="sxs-lookup"><span data-stu-id="e37b7-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e37b7-136">**BROCHE \_ catégorie \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="e37b7-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="e37b7-137">Code PIN fournissant les données de l’intervalle de l’occultation vertical.</span><span class="sxs-lookup"><span data-stu-id="e37b7-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e37b7-138">**PIN \_ catégorie \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="e37b7-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="e37b7-139">Broche de sortie vidéo à connecter à la broche d’entrée zéro dans le [mélangeur de superposition](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e37b7-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="e37b7-140">**BROCHE \_ catégorie \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="e37b7-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="e37b7-141">Code confidentiel à connecter à l' [allocateur de surface VBI](vbi-surface-allocator.md), filtre d’allocateur de surface VBI requis pour allouer la mémoire vidéo correcte pour des éléments tels que les superpositions de sous-titrage dans les scénarios où un port vidéo est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e37b7-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="e37b7-142">Les scénarios PCI, IEEE 1394 et USB n’utilisent pas ce filtre.</span><span class="sxs-lookup"><span data-stu-id="e37b7-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="e37b7-143">**\_ \_ capture CC de la vidéo PINNAME \_**</span><span class="sxs-lookup"><span data-stu-id="e37b7-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="e37b7-144">Découpage matériel fermé-code confidentiel</span><span class="sxs-lookup"><span data-stu-id="e37b7-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="e37b7-145">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e37b7-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="e37b7-146">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e37b7-146">Example Code</span></span>

<span data-ttu-id="e37b7-147">Le code suivant montre comment vérifier si un code PIN prend en charge ce jeu de propriétés et, le cas échéant, comment obtenir la catégorie de code confidentiel :</span><span class="sxs-lookup"><span data-stu-id="e37b7-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="e37b7-148">Cet exemple utilise la fonction [SafeRelease](../medfound/saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="e37b7-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e37b7-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e37b7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e37b7-150">Exigences de code confidentiel pour les filtres de capture</span><span class="sxs-lookup"><span data-stu-id="e37b7-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="e37b7-151">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="e37b7-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="e37b7-152">Utilisation des catégories de code confidentiel</span><span class="sxs-lookup"><span data-stu-id="e37b7-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
