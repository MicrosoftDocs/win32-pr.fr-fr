---
description: 'Fonction D3DXFresnelTerm (D3dx9math. h) : calcule le terme de la Fresnel.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114477"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="20db8-103">D3DXFresnelTerm, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="20db8-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="20db8-104">Calculez le terme de la Fresnel.</span><span class="sxs-lookup"><span data-stu-id="20db8-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="20db8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20db8-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="20db8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20db8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20db8-107">*CosTheta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20db8-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20db8-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20db8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20db8-109">Elle doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="20db8-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="20db8-110">*RefractionIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20db8-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20db8-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20db8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20db8-112">Index de réfraction d’un matériau.</span><span class="sxs-lookup"><span data-stu-id="20db8-112">The refraction index of a material.</span></span> <span data-ttu-id="20db8-113">La valeur doit être supérieure à 1.</span><span class="sxs-lookup"><span data-stu-id="20db8-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20db8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20db8-114">Return value</span></span>

<span data-ttu-id="20db8-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20db8-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20db8-116">Cette fonction retourne le terme de Fresnel pour la lumière dépolarisée.</span><span class="sxs-lookup"><span data-stu-id="20db8-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="20db8-117">CosTheta est le cosinus de l’angle d’incident.</span><span class="sxs-lookup"><span data-stu-id="20db8-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="20db8-118">Notes </span><span class="sxs-lookup"><span data-stu-id="20db8-118">Remarks</span></span>

<span data-ttu-id="20db8-119">Pour rechercher le terme de la Fresnel (F) :</span><span class="sxs-lookup"><span data-stu-id="20db8-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="20db8-120">Si un est un angle d’incidence et que B est l’angle de réfraction, alors</span><span class="sxs-lookup"><span data-stu-id="20db8-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="20db8-121">Ensuite, en développant à l’aide des identités trig et en simplifiant, vous bénéficiez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="20db8-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="20db8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20db8-122">Requirements</span></span>



| <span data-ttu-id="20db8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20db8-123">Requirement</span></span> | <span data-ttu-id="20db8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="20db8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20db8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="20db8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="20db8-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20db8-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="20db8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20db8-127">Library</span></span><br/> | <dl> <span data-ttu-id="20db8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20db8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20db8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20db8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20db8-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="20db8-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
