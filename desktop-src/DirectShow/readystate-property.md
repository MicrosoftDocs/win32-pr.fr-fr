---
description: La propriété ReadyState récupère l’ReadyState de l’objet MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propriété ReadyState (ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520872"
---
# <a name="readystate-property"></a><span data-ttu-id="95ef4-103">Propriété ReadyState</span><span class="sxs-lookup"><span data-stu-id="95ef4-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="95ef4-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="95ef4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="95ef4-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95ef4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="95ef4-106">La `ReadyState` propriété récupère l’readyState de l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="95ef4-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="95ef4-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95ef4-107">Return Value</span></span>

<span data-ttu-id="95ef4-108">Retourne une valeur entière représentant l’ReadyState du contrôle.</span><span class="sxs-lookup"><span data-stu-id="95ef4-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="95ef4-109">Code de retour</span><span class="sxs-lookup"><span data-stu-id="95ef4-109">Return code</span></span> | <span data-ttu-id="95ef4-110">Description</span><span class="sxs-lookup"><span data-stu-id="95ef4-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="95ef4-111">0</span><span class="sxs-lookup"><span data-stu-id="95ef4-111">0</span></span>           | <span data-ttu-id="95ef4-112">État d’initialisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="95ef4-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="95ef4-113">1</span><span class="sxs-lookup"><span data-stu-id="95ef4-113">1</span></span>           | <span data-ttu-id="95ef4-114">L’objet charge ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="95ef4-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="95ef4-115">2</span><span class="sxs-lookup"><span data-stu-id="95ef4-115">2</span></span>           | <span data-ttu-id="95ef4-116">L’objet a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="95ef4-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="95ef4-117">3</span><span class="sxs-lookup"><span data-stu-id="95ef4-117">3</span></span>           | <span data-ttu-id="95ef4-118">L’objet est interactif, mais les données ne sont pas toutes disponibles.</span><span class="sxs-lookup"><span data-stu-id="95ef4-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="95ef4-119">4</span><span class="sxs-lookup"><span data-stu-id="95ef4-119">4</span></span>           | <span data-ttu-id="95ef4-120">L’objet a reçu toutes ses données.</span><span class="sxs-lookup"><span data-stu-id="95ef4-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="95ef4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="95ef4-121">Remarks</span></span>

<span data-ttu-id="95ef4-122">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="95ef4-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="95ef4-123">Tout objet incorporé dans une page Web expose la `ReadyState` propriété.</span><span class="sxs-lookup"><span data-stu-id="95ef4-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ef4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95ef4-124">Requirements</span></span>



| <span data-ttu-id="95ef4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95ef4-125">Requirement</span></span> | <span data-ttu-id="95ef4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="95ef4-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95ef4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="95ef4-127">Header</span></span><br/> | <dl> <span data-ttu-id="95ef4-128"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ef4-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




