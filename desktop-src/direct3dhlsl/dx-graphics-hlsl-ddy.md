---
title: ddy
description: Retourne la dérivée partielle de la valeur spécifiée par rapport à la coordonnée y de l’espace d’écran.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- langage HLSL ddy
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382147"
---
# <a name="ddy"></a><span data-ttu-id="1f906-104">ddy</span><span class="sxs-lookup"><span data-stu-id="1f906-104">ddy</span></span>

<span data-ttu-id="1f906-105">Retourne la dérivée partielle de la valeur spécifiée par rapport à la coordonnée y de l’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="1f906-105">Returns the partial derivative of the specified value with respect to the screen-space y-coordinate.</span></span>



| <span data-ttu-id="1f906-106">*RET* ddY (*x*)</span><span class="sxs-lookup"><span data-stu-id="1f906-106">*ret* ddy(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="1f906-107">Cette fonction calcule la dérivée partielle par rapport à la coordonnée y de l’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="1f906-107">This function computes the partial derivative with respect to the screen-space y-coordinate.</span></span> <span data-ttu-id="1f906-108">Pour calculer la dérivée partielle par rapport à la coordonnée x de l’espace écran, utilisez la fonction [**ddx**](dx-graphics-hlsl-ddx.md) .</span><span class="sxs-lookup"><span data-stu-id="1f906-108">To compute the partial derivative with respect to the screen-space x-coordinate, use the [**ddx**](dx-graphics-hlsl-ddx.md) function.</span></span>

<span data-ttu-id="1f906-109">Cette fonction est prise en charge uniquement dans les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="1f906-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f906-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f906-110">Parameters</span></span>



| <span data-ttu-id="1f906-111">Élément</span><span class="sxs-lookup"><span data-stu-id="1f906-111">Item</span></span>                                                   | <span data-ttu-id="1f906-112">Description</span><span class="sxs-lookup"><span data-stu-id="1f906-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1f906-113"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="1f906-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1f906-114">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1f906-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1f906-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f906-115">Return Value</span></span>

<span data-ttu-id="1f906-116">Dérivée partielle du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="1f906-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="1f906-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="1f906-117">Type Description</span></span>



| <span data-ttu-id="1f906-118">Nom</span><span class="sxs-lookup"><span data-stu-id="1f906-118">Name</span></span>  | [<span data-ttu-id="1f906-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="1f906-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1f906-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="1f906-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1f906-121">Taille</span><span class="sxs-lookup"><span data-stu-id="1f906-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1f906-122">*x*</span><span class="sxs-lookup"><span data-stu-id="1f906-122">*x*</span></span>   | <span data-ttu-id="1f906-123">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="1f906-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="1f906-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="1f906-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1f906-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="1f906-125">any</span></span>                            |
| <span data-ttu-id="1f906-126">*Av*</span><span class="sxs-lookup"><span data-stu-id="1f906-126">*ret*</span></span> | <span data-ttu-id="1f906-127">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="1f906-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1f906-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="1f906-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1f906-129">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="1f906-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1f906-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1f906-130">Minimum Shader Model</span></span>

<span data-ttu-id="1f906-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1f906-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1f906-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1f906-132">Shader Model</span></span>                                                                | <span data-ttu-id="1f906-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1f906-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="1f906-134">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="1f906-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1f906-135">Oui</span><span class="sxs-lookup"><span data-stu-id="1f906-135">yes</span></span>                                       |
| [<span data-ttu-id="1f906-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1f906-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="1f906-137">Oui</span><span class="sxs-lookup"><span data-stu-id="1f906-137">yes</span></span>                                       |
| [<span data-ttu-id="1f906-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f906-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="1f906-139">Oui</span><span class="sxs-lookup"><span data-stu-id="1f906-139">yes</span></span>                                       |
| [<span data-ttu-id="1f906-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f906-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="1f906-141">Oui dans PS \_ 2 \_ x ; non pris en charge dans PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="1f906-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="1f906-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f906-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="1f906-143">non</span><span class="sxs-lookup"><span data-stu-id="1f906-143">no</span></span>                                        |



 

<span data-ttu-id="1f906-144">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1f906-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1f906-145">Sommet</span><span class="sxs-lookup"><span data-stu-id="1f906-145">Vertex</span></span> | <span data-ttu-id="1f906-146">Forme</span><span class="sxs-lookup"><span data-stu-id="1f906-146">Hull</span></span> | <span data-ttu-id="1f906-147">Domain</span><span class="sxs-lookup"><span data-stu-id="1f906-147">Domain</span></span> | <span data-ttu-id="1f906-148">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1f906-148">Geometry</span></span> | <span data-ttu-id="1f906-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="1f906-149">Pixel</span></span> | <span data-ttu-id="1f906-150">Compute</span><span class="sxs-lookup"><span data-stu-id="1f906-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1f906-151">x</span><span class="sxs-lookup"><span data-stu-id="1f906-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="1f906-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f906-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f906-153">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1f906-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

