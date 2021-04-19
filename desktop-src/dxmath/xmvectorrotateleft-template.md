---
description: Fait pivoter le vecteur vers la gauche d’un nombre donné d’éléments de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modèle XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535260"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="e10cd-103">Modèle XMVectorRotateLeft</span><span class="sxs-lookup"><span data-stu-id="e10cd-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="e10cd-104">Fait pivoter le vecteur vers la gauche d’un nombre donné d’éléments de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e10cd-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e10cd-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="e10cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e10cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10cd-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="e10cd-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="e10cd-108">\[dans \] Vector pour faire pivoter vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="e10cd-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10cd-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e10cd-109">Return Value</span></span>

<span data-ttu-id="e10cd-110">Retourne le [**XMVECTOR**](xmvector-data-type.md)pivoté.</span><span class="sxs-lookup"><span data-stu-id="e10cd-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e10cd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e10cd-111">Remarks</span></span>

<span data-ttu-id="e10cd-112">Cette fonction est une version de modèle de [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) où l’argument *Elements* est une valeur de modèle.</span><span class="sxs-lookup"><span data-stu-id="e10cd-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="e10cd-113">Le `XMVectorRotateLeft` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="e10cd-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="e10cd-114">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="e10cd-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e10cd-115">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="e10cd-115">Platform Requirements</span></span>

<span data-ttu-id="e10cd-116">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e10cd-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="e10cd-117">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="e10cd-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10cd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e10cd-118">Requirements</span></span>



| <span data-ttu-id="e10cd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e10cd-119">Requirement</span></span> | <span data-ttu-id="e10cd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e10cd-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10cd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e10cd-121">Header</span></span><br/> | <dl> <span data-ttu-id="e10cd-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10cd-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10cd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e10cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10cd-124">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e10cd-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="e10cd-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="e10cd-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="e10cd-126">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="e10cd-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="e10cd-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="e10cd-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
