---
description: Fait pivoter un vecteur vers la gauche d’un nombre donné de composants 32 bits et insérer les éléments sélectionnés de ce résultat dans un autre vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modèle XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526319"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="524d8-103">Modèle XMVectorInsert</span><span class="sxs-lookup"><span data-stu-id="524d8-103">XMVectorInsert template</span></span>

<span data-ttu-id="524d8-104">Fait pivoter un vecteur vers la gauche d’un nombre donné de composants 32 bits et insérer les éléments sélectionnés de ce résultat dans un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="524d8-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="524d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="524d8-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="524d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="524d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="524d8-107"><span id="VD"></span><span id="vd"></span>*VD*</span><span class="sxs-lookup"><span data-stu-id="524d8-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="524d8-108">\[dans \] Vector à insérer dans.</span><span class="sxs-lookup"><span data-stu-id="524d8-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="524d8-109"><span id="VS"></span><span id="vs"></span>*COMPARATIF*</span><span class="sxs-lookup"><span data-stu-id="524d8-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="524d8-110">\[dans \] Vector pour faire pivoter vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="524d8-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="524d8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="524d8-111">Return Value</span></span>

<span data-ttu-id="524d8-112">Retourne le [**XMVECTOR**](xmvector-data-type.md) qui résulte de la rotation et de l’insertion.</span><span class="sxs-lookup"><span data-stu-id="524d8-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="524d8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="524d8-113">Remarks</span></span>

<span data-ttu-id="524d8-114">Cette fonction est une version de modèle de [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) où les arguments *Select \** sont des valeurs de modèle.</span><span class="sxs-lookup"><span data-stu-id="524d8-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="524d8-115">Pour des performances optimales, le résultat de `XMVectorInsert` doit être attribué à *VD*.</span><span class="sxs-lookup"><span data-stu-id="524d8-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="524d8-116">Le `XMVectorInsert` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="524d8-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="524d8-117">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="524d8-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="524d8-118">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="524d8-118">Platform Requirements</span></span>

<span data-ttu-id="524d8-119">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="524d8-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="524d8-120">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="524d8-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="524d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="524d8-121">Requirements</span></span>



| <span data-ttu-id="524d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="524d8-122">Requirement</span></span> | <span data-ttu-id="524d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="524d8-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="524d8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="524d8-124">Header</span></span><br/> | <dl> <span data-ttu-id="524d8-125"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="524d8-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="524d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="524d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524d8-127">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="524d8-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="524d8-128">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="524d8-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="524d8-129">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="524d8-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="524d8-130">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="524d8-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="524d8-131">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="524d8-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
