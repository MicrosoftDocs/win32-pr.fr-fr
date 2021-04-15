---
title: Effet Atlas
description: Vous pouvez utiliser cet effet pour sortir une partie d’une image tout en conservant la région en dehors de la partie pour une utilisation dans les opérations suivantes.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466319"
---
# <a name="atlas-effect"></a><span data-ttu-id="f063c-103">Effet Atlas</span><span class="sxs-lookup"><span data-stu-id="f063c-103">Atlas effect</span></span>

<span data-ttu-id="f063c-104">Vous pouvez utiliser cet effet pour sortir une partie d’une image tout en conservant la région en dehors de la partie pour une utilisation dans les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="f063c-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="f063c-105">Le CLSID de cet effet est CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="f063c-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="f063c-106">L’effet Atlas est utile si vous souhaitez charger une grande image composée de nombreuses images plus petites, telles que des images différentes d’un sprite.</span><span class="sxs-lookup"><span data-stu-id="f063c-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="f063c-107">Pour créer la sortie, l’effet :</span><span class="sxs-lookup"><span data-stu-id="f063c-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="f063c-108">Découpe l’entrée vers la propriété *InputRect* donnée.</span><span class="sxs-lookup"><span data-stu-id="f063c-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="f063c-109">Convertit l’origine du résultat en (0,0).</span><span class="sxs-lookup"><span data-stu-id="f063c-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="f063c-110">La propriété *InputPaddingRect* doit être supérieure uniquement si et seulement si les pixels entre les deux rectangles sont transparents en noir sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f063c-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="f063c-111">Cela peut entraîner l’exécution de Direct2D de manière plus optimale sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="f063c-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="f063c-112">Voici un exemple de l’effet.</span><span class="sxs-lookup"><span data-stu-id="f063c-112">Here is an example of the effect.</span></span> <span data-ttu-id="f063c-113">Cette image est petite et simple à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="f063c-113">This image is small and simple for illustration purposes.</span></span>

![image d’entrée.](images/atlas.png)

<span data-ttu-id="f063c-115">L’image précédente est l’entrée de l’effet.</span><span class="sxs-lookup"><span data-stu-id="f063c-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="f063c-116">Le code suivant crée un effet Atlas, définit l’entrée, définit le rectangle de saisie, puis dessine la sortie.</span><span class="sxs-lookup"><span data-stu-id="f063c-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="f063c-117">Le code précédent sélectionne un rectangle autour du deuxième triangle.</span><span class="sxs-lookup"><span data-stu-id="f063c-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="f063c-118">La marge autour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f063c-118">The padding around it is ignored.</span></span> <span data-ttu-id="f063c-119">Voici l’image résultante.</span><span class="sxs-lookup"><span data-stu-id="f063c-119">Here is the resulting image.</span></span>

![image de sortie.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="f063c-121">Il s’agit d’une situation dans laquelle vous pouvez choisir de spécifier un *InputPaddingRect* , car le remplissage est transparent.</span><span class="sxs-lookup"><span data-stu-id="f063c-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="f063c-122">Le rectangle est `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="f063c-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="f063c-123">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="f063c-123">Effect properties</span></span>



| <span data-ttu-id="f063c-124">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="f063c-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="f063c-125">Description</span><span class="sxs-lookup"><span data-stu-id="f063c-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f063c-126">InputRect</span><span class="sxs-lookup"><span data-stu-id="f063c-126">InputRect</span></span><br/> <span data-ttu-id="f063c-127">\_ \_ \_ Recto d’entrée d2d1 Atlas prop \_</span><span class="sxs-lookup"><span data-stu-id="f063c-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="f063c-128">Partie de l’image passée à l’effet suivant.</span><span class="sxs-lookup"><span data-stu-id="f063c-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="f063c-129">Le type est D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="f063c-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="f063c-130">La valeur par défaut est (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).</span><span class="sxs-lookup"><span data-stu-id="f063c-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="f063c-131">InputPaddingRect</span><span class="sxs-lookup"><span data-stu-id="f063c-131">InputPaddingRect</span></span><br/> <span data-ttu-id="f063c-132">D2D1 \_ Atlas \_ prop \_ de \_ remplissage d' \_ entrée</span><span class="sxs-lookup"><span data-stu-id="f063c-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="f063c-133">Taille maximale échantillonnée pour le rectangle de sortie.</span><span class="sxs-lookup"><span data-stu-id="f063c-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="f063c-134">Le type est D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="f063c-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="f063c-135">La valeur par défaut est (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).</span><span class="sxs-lookup"><span data-stu-id="f063c-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="f063c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f063c-136">Requirements</span></span>



| <span data-ttu-id="f063c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f063c-137">Requirement</span></span> | <span data-ttu-id="f063c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f063c-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f063c-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f063c-139">Minimum supported client</span></span> | <span data-ttu-id="f063c-140">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f063c-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f063c-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f063c-141">Minimum supported server</span></span> | <span data-ttu-id="f063c-142">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f063c-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f063c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="f063c-143">Header</span></span>                   | <span data-ttu-id="f063c-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="f063c-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="f063c-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f063c-145">Library</span></span>                  | <span data-ttu-id="f063c-146">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f063c-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f063c-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f063c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f063c-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="f063c-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

