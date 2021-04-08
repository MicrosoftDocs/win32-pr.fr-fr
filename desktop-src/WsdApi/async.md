---
description: Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: élément Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035111"
---
# <a name="async-element"></a><span data-ttu-id="225a1-103">élément Async</span><span class="sxs-lookup"><span data-stu-id="225a1-103">async element</span></span>

<span data-ttu-id="225a1-104">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="225a1-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="225a1-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="225a1-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="225a1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="225a1-106">Attributes</span></span>

<span data-ttu-id="225a1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="225a1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="225a1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="225a1-108">Child elements</span></span>

<span data-ttu-id="225a1-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="225a1-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="225a1-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="225a1-110">Parent elements</span></span>



| <span data-ttu-id="225a1-111">Élément</span><span class="sxs-lookup"><span data-stu-id="225a1-111">Element</span></span>                                                                         | <span data-ttu-id="225a1-112">Description</span><span class="sxs-lookup"><span data-stu-id="225a1-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="225a1-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="225a1-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="225a1-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="225a1-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="225a1-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="225a1-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="225a1-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="225a1-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="225a1-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="225a1-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="225a1-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="225a1-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="225a1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="225a1-119">Remarks</span></span>

<span data-ttu-id="225a1-120">Les valeurs possibles sont 1 (opérations asynchrones incluses) et 0 (opérations asynchrones par défaut exclues).</span><span class="sxs-lookup"><span data-stu-id="225a1-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="225a1-121">Un proxy peut avoir des versions asynchrones et synchrones des mêmes opérations.</span><span class="sxs-lookup"><span data-stu-id="225a1-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="225a1-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="225a1-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="225a1-123">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="225a1-123">Minimum supported system</span></span><br/> | <span data-ttu-id="225a1-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="225a1-124">Windows Vista</span></span> |
| <span data-ttu-id="225a1-125">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="225a1-125">Can be empty</span></span>                        | <span data-ttu-id="225a1-126">Oui</span><span class="sxs-lookup"><span data-stu-id="225a1-126">Yes</span></span>           |



 

 




