---
description: Effet d’accesseur Set alpha
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Effet d’accesseur Set alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746372"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="535c0-103">Effet d’accesseur Set alpha</span><span class="sxs-lookup"><span data-stu-id="535c0-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="535c0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="535c0-104">\[Deprecated.</span></span> <span data-ttu-id="535c0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="535c0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="535c0-106">L’effet de l’accesseur Set alpha définit les bits alpha sur une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="535c0-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="535c0-107">ID de classe (CLSID) : {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="535c0-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="535c0-108">Nom de la variable CLSID : CLSID \_ DxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="535c0-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="535c0-109">Nom convivial : « DxtAlphaSetter »</span><span class="sxs-lookup"><span data-stu-id="535c0-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="535c0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="535c0-110">Properties</span></span>



| <span data-ttu-id="535c0-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="535c0-111">Property</span></span>  | <span data-ttu-id="535c0-112">Type</span><span class="sxs-lookup"><span data-stu-id="535c0-112">Type</span></span>   | <span data-ttu-id="535c0-113">Default</span><span class="sxs-lookup"><span data-stu-id="535c0-113">Default</span></span> | <span data-ttu-id="535c0-114">Description</span><span class="sxs-lookup"><span data-stu-id="535c0-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="535c0-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="535c0-115">Alpha</span></span>     | <span data-ttu-id="535c0-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="535c0-116">BYTE</span></span>   | <span data-ttu-id="535c0-117">-1</span><span class="sxs-lookup"><span data-stu-id="535c0-117">-1</span></span>      | <span data-ttu-id="535c0-118">Définit l’alpha pour la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="535c0-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="535c0-119">AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="535c0-119">AlphaRamp</span></span> | <span data-ttu-id="535c0-120">double</span><span class="sxs-lookup"><span data-stu-id="535c0-120">double</span></span> | <span data-ttu-id="535c0-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="535c0-121">-1.0</span></span>    | <span data-ttu-id="535c0-122">Définit le alpha comme pourcentage de la valeur alpha d’origine.</span><span class="sxs-lookup"><span data-stu-id="535c0-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="535c0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="535c0-123">Remarks</span></span>

<span data-ttu-id="535c0-124">Une propriété avec une valeur négative est ignorée.</span><span class="sxs-lookup"><span data-stu-id="535c0-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="535c0-125">Une seule propriété peut avoir une valeur non négative.</span><span class="sxs-lookup"><span data-stu-id="535c0-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="535c0-126">La propriété alpha spécifie une valeur alpha constante pour chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="535c0-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="535c0-127">Cette propriété remplace les valeurs alpha de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="535c0-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="535c0-128">La propriété AlphaRamp spécifie la valeur alpha de chaque pixel sous la forme d’un pourcentage de la valeur d’origine du pixel, de 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="535c0-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="535c0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="535c0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="535c0-130">Fusion alpha</span><span class="sxs-lookup"><span data-stu-id="535c0-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



