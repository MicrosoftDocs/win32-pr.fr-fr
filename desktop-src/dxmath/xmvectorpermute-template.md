---
description: Permute les composants de deux vecteurs pour créer un nouveau vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modèle XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539311"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="5b42e-103">Modèle XMVectorPermute</span><span class="sxs-lookup"><span data-stu-id="5b42e-103">XMVectorPermute template</span></span>

<span data-ttu-id="5b42e-104">Permute les composants de deux vecteurs pour créer un nouveau vecteur.</span><span class="sxs-lookup"><span data-stu-id="5b42e-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b42e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b42e-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="5b42e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b42e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b42e-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="5b42e-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="5b42e-108">\[dans le \] premier vecteur.</span><span class="sxs-lookup"><span data-stu-id="5b42e-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="5b42e-109"><span id="V2"></span><span id="v2"></span>*MIME*</span><span class="sxs-lookup"><span data-stu-id="5b42e-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="5b42e-110">\[dans le \] second vecteur.</span><span class="sxs-lookup"><span data-stu-id="5b42e-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b42e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b42e-111">Return Value</span></span>

<span data-ttu-id="5b42e-112">Retourne le vecteur permuté qui résulte de la combinaison des vecteurs sources.</span><span class="sxs-lookup"><span data-stu-id="5b42e-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b42e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5b42e-113">Remarks</span></span>

<span data-ttu-id="5b42e-114">Si les 4 index ne référencent qu’un seul vecteur (c’est-à-dire qu’ils se trouvent tous dans la plage 0-3 ou dans la plage 4-7), utilisez [**XMVectorSwizzle**](xmvectorswizzle-template.md) à la place pour obtenir de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="5b42e-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="5b42e-115">Notez que la bibliothèque utilise des spécialisations de modèle sur certaines plateformes pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="5b42e-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="5b42e-116">Tous les cas de mise en miroir possibles ne sont pas implémentés pour ces cas spéciaux. par conséquent, il est préférable de faire en sorte que l’élément X du vecteur résultant provient du paramètre v1 plutôt que du paramètre v2.</span><span class="sxs-lookup"><span data-stu-id="5b42e-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="5b42e-117">Par exemple, préférez utiliser `XMVectorPermute<0,1,4,5>(A,B);` à `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="5b42e-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="5b42e-118">Cette fonction est une version de modèle de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) où les arguments *permute \** sont des valeurs de modèle.</span><span class="sxs-lookup"><span data-stu-id="5b42e-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="5b42e-119">Les constantes [XM \_ permute \_](ovw-xnamath-reference-constants.md) sont fournies pour une utilisation en tant que valeurs d’entrée pour *permutex*,*permute*,*PermuteZ* et *PermuteW*.</span><span class="sxs-lookup"><span data-stu-id="5b42e-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="5b42e-120">Le `XMVectorPermute` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="5b42e-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="5b42e-121">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="5b42e-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="5b42e-122">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="5b42e-122">Platform Requirements</span></span>

<span data-ttu-id="5b42e-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5b42e-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="5b42e-124">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="5b42e-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b42e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b42e-125">Requirements</span></span>



| <span data-ttu-id="5b42e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b42e-126">Requirement</span></span> | <span data-ttu-id="5b42e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b42e-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b42e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b42e-128">Header</span></span><br/> | <dl> <span data-ttu-id="5b42e-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b42e-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b42e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b42e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b42e-131">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="5b42e-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="5b42e-132">**XMVectorSwizzle**</span><span class="sxs-lookup"><span data-stu-id="5b42e-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
