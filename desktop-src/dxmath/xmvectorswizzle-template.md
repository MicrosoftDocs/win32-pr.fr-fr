---
description: Swizzles un vecteur.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modèle XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541760"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="bfa6e-103">Modèle XMVectorSwizzle</span><span class="sxs-lookup"><span data-stu-id="bfa6e-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="bfa6e-104">Swizzles un vecteur.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfa6e-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="bfa6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfa6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa6e-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="bfa6e-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="bfa6e-108">\[dans \] vector to Swizzle.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa6e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bfa6e-109">Return Value</span></span>

<span data-ttu-id="bfa6e-110">Retourne le [**XMVECTOR**](xmvector-data-type.md)swizzled.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bfa6e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bfa6e-111">Remarks</span></span>

<span data-ttu-id="bfa6e-112">Cette fonction est une version de modèle de [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) où les arguments *Swizzle \** sont des valeurs de modèle.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="bfa6e-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` et `XM_SWIZZLE_W` sont des constantes qui prennent respectivement la valeur 0, 1, 2 et 3 pour une utilisation avec `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="bfa6e-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="bfa6e-114">Identique à,, `XM_PERMUTE_0X` `XM_PERMUTE_0Y` `XM_PERMUTE_0Z` et `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="bfa6e-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="bfa6e-115">Le `XMVectorSwizzle` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="bfa6e-116">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="bfa6e-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="bfa6e-117">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="bfa6e-117">Platform Requirements</span></span>

<span data-ttu-id="bfa6e-118">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="bfa6e-119">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="bfa6e-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa6e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfa6e-120">Requirements</span></span>



| <span data-ttu-id="bfa6e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfa6e-121">Requirement</span></span> | <span data-ttu-id="bfa6e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa6e-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa6e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfa6e-123">Header</span></span><br/> | <dl> <span data-ttu-id="bfa6e-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa6e-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa6e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa6e-126">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="bfa6e-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="bfa6e-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="bfa6e-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
