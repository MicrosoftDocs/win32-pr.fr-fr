---
description: Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus grande des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modèle XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522804"
---
# <a name="xmmax-template"></a><span data-ttu-id="4cfc7-104">Modèle XMMax</span><span class="sxs-lookup"><span data-stu-id="4cfc7-104">XMMax template</span></span>

<span data-ttu-id="4cfc7-105">Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus grande des deux instances.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the larger one of the two instances.</span></span> <span data-ttu-id="4cfc7-106">Le type de données des arguments et la valeur de retour sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfc7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cfc7-107">Syntax</span></span>

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="4cfc7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cfc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfc7-109"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="4cfc7-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="4cfc7-110">\[dans \] spécifie le premier des deux objets.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc7-111"><span id="b"></span><span id="B"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="4cfc7-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="4cfc7-112">\[dans \] spécifie les deux des deux objets.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfc7-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4cfc7-113">Return Value</span></span>

<span data-ttu-id="4cfc7-114">Retourne le plus grand des deux objets d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-114">Returns the larger of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfc7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4cfc7-115">Remarks</span></span>

<span data-ttu-id="4cfc7-116">`XMMax` est un modèle et le type T est spécifié quand le modèle est instancié.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-116">`XMMax` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="4cfc7-117">Le `XMMax` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-117">The `XMMax` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="4cfc7-118">`XMMax` est disponible en tant que macro dans XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-118">`XMMax` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cfc7-119">Dans l’idéal, utilisez std :: Max au lieu de `XMMax` .</span><span class="sxs-lookup"><span data-stu-id="4cfc7-119">Ideally use std::max instead of `XMMax`.</span></span> <span data-ttu-id="4cfc7-120">Pour éviter les conflits avec les en-têtes Windows avec std :: Max, vous devez \# définir NOMINMAX avant d’inclure les en-têtes Windows.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-120">To avoid conflicts with Windows headers with std::max, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="4cfc7-121">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="4cfc7-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="4cfc7-122">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="4cfc7-122">Platform Requirements</span></span>

<span data-ttu-id="4cfc7-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="4cfc7-124">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="4cfc7-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfc7-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cfc7-125">Requirements</span></span>



| <span data-ttu-id="4cfc7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cfc7-126">Requirement</span></span> | <span data-ttu-id="4cfc7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfc7-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfc7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cfc7-128">Header</span></span><br/> | <dl> <span data-ttu-id="4cfc7-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfc7-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cfc7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cfc7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfc7-131">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4cfc7-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="4cfc7-132">**XMMin**</span><span class="sxs-lookup"><span data-stu-id="4cfc7-132">**XMMin**</span></span>](xmmin-template.md)
</dt> </dl>

 

 




