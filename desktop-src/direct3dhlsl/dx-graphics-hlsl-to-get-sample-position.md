---
title: GetSamplePosition (objet texture HLSL DirectX)
description: Obtient la position de l’échantillon spécifié.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381131"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="a2d05-103">GetSamplePosition (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="a2d05-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="a2d05-104">Obtient la position de l’échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2d05-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="a2d05-105">RET Object. GetSamplePosition (int s);</span><span class="sxs-lookup"><span data-stu-id="a2d05-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a2d05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2d05-106">Parameters</span></span>



| <span data-ttu-id="a2d05-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a2d05-107">Item</span></span>                                                                                           | <span data-ttu-id="a2d05-108">Description</span><span class="sxs-lookup"><span data-stu-id="a2d05-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d05-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*</span><span class="sxs-lookup"><span data-stu-id="a2d05-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="a2d05-110">Type d' [objet de texture](dx-graphics-hlsl-to-type.md) Texture2DMS ou Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="a2d05-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="a2d05-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a2d05-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="a2d05-112">\[dans \] l’exemple d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="a2d05-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="a2d05-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a2d05-113">Return Value</span></span>

<span data-ttu-id="a2d05-114">Retourne la position d’échantillon (x, y), un vecteur à virgule flottante à deux composants.</span><span class="sxs-lookup"><span data-stu-id="a2d05-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="a2d05-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a2d05-115">Minimum Shader Model</span></span>

<span data-ttu-id="a2d05-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="a2d05-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a2d05-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2d05-117">vs\_4\_0</span></span> | <span data-ttu-id="a2d05-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a2d05-118">vs\_4\_1</span></span>  | <span data-ttu-id="a2d05-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2d05-119">ps\_4\_0</span></span> | <span data-ttu-id="a2d05-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a2d05-120">ps\_4\_1</span></span>  | <span data-ttu-id="a2d05-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2d05-121">gs\_4\_0</span></span> | <span data-ttu-id="a2d05-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a2d05-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="a2d05-123">x</span><span class="sxs-lookup"><span data-stu-id="a2d05-123">x</span></span>         |          | <span data-ttu-id="a2d05-124">x</span><span class="sxs-lookup"><span data-stu-id="a2d05-124">x</span></span>         |          | <span data-ttu-id="a2d05-125">x</span><span class="sxs-lookup"><span data-stu-id="a2d05-125">x</span></span>         |



 

-   <span data-ttu-id="a2d05-126">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a2d05-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d05-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a2d05-127">Remarks</span></span>

<span data-ttu-id="a2d05-128">Un nuanceur de pixels peut être évalué à la fréquence d’échantillonnage (exécuter un nuanceur de pixels une fois par échantillon) ou à fréquence en pixels (exécuter un nuanceur de pixels une fois par pixel).</span><span class="sxs-lookup"><span data-stu-id="a2d05-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="a2d05-129">Attacher la \_ sémantique SV SampleIndex à une entrée de nuanceur de pixels pour appeler un nuanceur de pixels à la fréquence d’échantillonnage, la valeur d’entrée est ensuite utilisée comme exemple d’index lors de l’échantillonnage de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="a2d05-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="a2d05-130">Vous pouvez interpoler une entrée de nuanceur de pixels de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="a2d05-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="a2d05-131">Pour interpoler à :</span><span class="sxs-lookup"><span data-stu-id="a2d05-131">To interpolate at:</span></span>

-   <span data-ttu-id="a2d05-132">Un centre de pixels, n’utilisez aucune sémantique.</span><span class="sxs-lookup"><span data-stu-id="a2d05-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="a2d05-133">Un exemple, utilisez la \_ sémantique SV SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="a2d05-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="a2d05-134">Un emplacement de centre de gravité, utilisez le modificateur de centre de [ \_ gravité](dx-graphics-hlsl-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="a2d05-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d05-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2d05-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d05-136">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="a2d05-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





