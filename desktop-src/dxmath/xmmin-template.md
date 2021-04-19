---
description: Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus petite des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modèle XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538574"
---
# <a name="xmmin-template"></a><span data-ttu-id="d4336-104">Modèle XMMin</span><span class="sxs-lookup"><span data-stu-id="d4336-104">XMMin template</span></span>

<span data-ttu-id="d4336-105">Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus petite des deux instances.</span><span class="sxs-lookup"><span data-stu-id="d4336-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="d4336-106">Le type de données des arguments et la valeur de retour sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="d4336-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4336-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4336-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="d4336-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4336-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4336-109"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="d4336-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="d4336-110">\[dans \] spécifie le premier des deux objets.</span><span class="sxs-lookup"><span data-stu-id="d4336-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="d4336-111"><span id="b"></span><span id="B"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="d4336-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="d4336-112">\[dans \] spécifie les deux des deux objets.</span><span class="sxs-lookup"><span data-stu-id="d4336-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4336-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4336-113">Return Value</span></span>

<span data-ttu-id="d4336-114">Retourne le plus petit des deux objets d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d4336-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4336-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d4336-115">Remarks</span></span>

<span data-ttu-id="d4336-116">`XMMin` est un modèle et le type T est spécifié quand le modèle est instancié.</span><span class="sxs-lookup"><span data-stu-id="d4336-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="d4336-117">Le `XMMin` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="d4336-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="d4336-118">`XMMin` est disponible en tant que macro dans XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="d4336-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4336-119">Dans l’idéal, utilisez std :: min au lieu de `XMMin` .</span><span class="sxs-lookup"><span data-stu-id="d4336-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="d4336-120">Pour éviter les conflits avec les en-têtes Windows avec std :: min, vous devez \# définir NOMINMAX avant d’inclure les en-têtes Windows.</span><span class="sxs-lookup"><span data-stu-id="d4336-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="d4336-121">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="d4336-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="d4336-122">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="d4336-122">Platform Requirements</span></span>

<span data-ttu-id="d4336-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d4336-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="d4336-124">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="d4336-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4336-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4336-125">Requirements</span></span>



| <span data-ttu-id="d4336-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4336-126">Requirement</span></span> | <span data-ttu-id="d4336-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4336-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4336-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4336-128">Header</span></span><br/> | <dl> <span data-ttu-id="d4336-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4336-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4336-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4336-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4336-131">Fonctions de modèle de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="d4336-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="d4336-132">**XMMax**</span><span class="sxs-lookup"><span data-stu-id="d4336-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




