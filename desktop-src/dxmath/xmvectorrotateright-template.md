---
description: Fait pivoter le vecteur vers la droite d’un nombre donné d’éléments de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modèle XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526470"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="50b6d-103">Modèle XMVectorRotateRight</span><span class="sxs-lookup"><span data-stu-id="50b6d-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="50b6d-104">Fait pivoter le vecteur vers la droite d’un nombre donné d’éléments de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50b6d-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b6d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50b6d-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="50b6d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b6d-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="50b6d-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="50b6d-108">\[dans \] Vector pour faire pivoter vers la droite.</span><span class="sxs-lookup"><span data-stu-id="50b6d-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b6d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50b6d-109">Return Value</span></span>

<span data-ttu-id="50b6d-110">Retourne le [**XMVECTOR**](xmvector-data-type.md)pivoté.</span><span class="sxs-lookup"><span data-stu-id="50b6d-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="50b6d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="50b6d-111">Remarks</span></span>

<span data-ttu-id="50b6d-112">Cette fonction est une version de modèle de [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) où l’argument *Elements* est une valeur de modèle.</span><span class="sxs-lookup"><span data-stu-id="50b6d-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="50b6d-113">Le `XMVectorRotateRight` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="50b6d-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="50b6d-114">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="50b6d-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="50b6d-115">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="50b6d-115">Platform Requirements</span></span>

<span data-ttu-id="50b6d-116">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50b6d-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="50b6d-117">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="50b6d-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b6d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b6d-118">Requirements</span></span>



| <span data-ttu-id="50b6d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50b6d-119">Requirement</span></span> | <span data-ttu-id="50b6d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b6d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b6d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="50b6d-121">Header</span></span><br/> | <dl> <span data-ttu-id="50b6d-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="50b6d-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b6d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b6d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b6d-124">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="50b6d-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="50b6d-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="50b6d-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="50b6d-126">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="50b6d-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="50b6d-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="50b6d-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
