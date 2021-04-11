---
description: Spécifie si les événements connexes sont inclus dans les fonctions générées.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: élément Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202271"
---
# <a name="events-element"></a><span data-ttu-id="3b6a8-103">élément Events</span><span class="sxs-lookup"><span data-stu-id="3b6a8-103">events element</span></span>

<span data-ttu-id="3b6a8-104">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="3b6a8-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3b6a8-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="3b6a8-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="3b6a8-106">Attributes</span></span>

<span data-ttu-id="3b6a8-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3b6a8-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b6a8-108">Child elements</span></span>

<span data-ttu-id="3b6a8-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3b6a8-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3b6a8-110">Parent elements</span></span>



| <span data-ttu-id="3b6a8-111">Élément</span><span class="sxs-lookup"><span data-stu-id="3b6a8-111">Element</span></span>                                                                         | <span data-ttu-id="3b6a8-112">Description</span><span class="sxs-lookup"><span data-stu-id="3b6a8-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b6a8-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="3b6a8-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="3b6a8-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="3b6a8-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="3b6a8-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="3b6a8-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="3b6a8-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="3b6a8-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="3b6a8-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="3b6a8-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="3b6a8-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="3b6a8-120">Génère des déclarations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="3b6a8-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="3b6a8-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="3b6a8-122">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3b6a8-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="3b6a8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3b6a8-123">Remarks</span></span>

<span data-ttu-id="3b6a8-124">Les valeurs possibles sont 1 (événements inclus) et 0 (valeur par défaut, événements exclus).</span><span class="sxs-lookup"><span data-stu-id="3b6a8-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="3b6a8-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3b6a8-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="3b6a8-126">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b6a8-126">Minimum supported system</span></span><br/> | <span data-ttu-id="3b6a8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b6a8-127">Windows Vista</span></span> |
| <span data-ttu-id="3b6a8-128">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="3b6a8-128">Can be empty</span></span>                        | <span data-ttu-id="3b6a8-129">Oui</span><span class="sxs-lookup"><span data-stu-id="3b6a8-129">Yes</span></span>           |



 

 




