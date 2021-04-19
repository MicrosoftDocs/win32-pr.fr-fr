---
description: Déplace un vecteur vers la gauche d’un nombre donné d’éléments 32 bits, en remplissant les éléments libérés avec les éléments d’un second vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modèle XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544449"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="f9637-103">Modèle XMVectorShiftLeft</span><span class="sxs-lookup"><span data-stu-id="f9637-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="f9637-104">Déplace un vecteur vers la gauche d’un nombre donné d’éléments 32 bits, en remplissant les éléments libérés avec les éléments d’un second vecteur.</span><span class="sxs-lookup"><span data-stu-id="f9637-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9637-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9637-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="f9637-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9637-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="f9637-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="f9637-108">\[dans \] Vector, déplacer vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="f9637-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="f9637-109"><span id="V2"></span><span id="v2"></span>*MIME*</span><span class="sxs-lookup"><span data-stu-id="f9637-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="f9637-110">\[dans \] Vector utilisé pour remplir les composants libérés de V1 après leur décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="f9637-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9637-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9637-111">Return Value</span></span>

<span data-ttu-id="f9637-112">Retourne le décalage et le remplissage de [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="f9637-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9637-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f9637-113">Remarks</span></span>

<span data-ttu-id="f9637-114">Cette fonction est une version de modèle de [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) où l’argument *Elements* est une valeur de modèle.</span><span class="sxs-lookup"><span data-stu-id="f9637-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="f9637-115">Le `XMVectorShiftLeft` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="f9637-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="f9637-116">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="f9637-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="f9637-117">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="f9637-117">Platform Requirements</span></span>

<span data-ttu-id="f9637-118">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9637-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="f9637-119">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="f9637-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9637-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9637-120">Requirements</span></span>



| <span data-ttu-id="f9637-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9637-121">Requirement</span></span> | <span data-ttu-id="f9637-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9637-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9637-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9637-123">Header</span></span><br/> | <dl> <span data-ttu-id="f9637-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9637-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9637-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9637-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9637-126">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f9637-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="f9637-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="f9637-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="f9637-128">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="f9637-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="f9637-129">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="f9637-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
