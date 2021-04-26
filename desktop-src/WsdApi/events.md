---
description: Spécifie si les événements connexes sont inclus dans les fonctions générées.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: élément Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995927"
---
# <a name="events-element"></a><span data-ttu-id="f30b0-103">élément Events</span><span class="sxs-lookup"><span data-stu-id="f30b0-103">events element</span></span>

<span data-ttu-id="f30b0-104">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="f30b0-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="f30b0-105">Usage</span><span class="sxs-lookup"><span data-stu-id="f30b0-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="f30b0-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="f30b0-106">Attributes</span></span>

<span data-ttu-id="f30b0-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f30b0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f30b0-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f30b0-108">Child elements</span></span>

<span data-ttu-id="f30b0-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="f30b0-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f30b0-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f30b0-110">Parent elements</span></span>



| <span data-ttu-id="f30b0-111">Élément</span><span class="sxs-lookup"><span data-stu-id="f30b0-111">Element</span></span>                                                                         | <span data-ttu-id="f30b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="f30b0-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f30b0-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f30b0-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="f30b0-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="f30b0-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="f30b0-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f30b0-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="f30b0-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="f30b0-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="f30b0-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="f30b0-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="f30b0-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="f30b0-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="f30b0-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f30b0-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="f30b0-120">Génère des déclarations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="f30b0-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="f30b0-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f30b0-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="f30b0-122">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="f30b0-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="f30b0-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f30b0-123">Remarks</span></span>

<span data-ttu-id="f30b0-124">Les valeurs possibles sont 1 (événements inclus) et 0 (valeur par défaut, événements exclus).</span><span class="sxs-lookup"><span data-stu-id="f30b0-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="f30b0-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f30b0-125">Element information</span></span>



| <span data-ttu-id="f30b0-126">Étiquette</span><span class="sxs-lookup"><span data-stu-id="f30b0-126">Label</span></span> | <span data-ttu-id="f30b0-127">Value</span><span class="sxs-lookup"><span data-stu-id="f30b0-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f30b0-128">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f30b0-128">Minimum supported system</span></span><br/> | <span data-ttu-id="f30b0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f30b0-129">Windows Vista</span></span> |
| <span data-ttu-id="f30b0-130">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="f30b0-130">Can be empty</span></span>                        | <span data-ttu-id="f30b0-131">Oui</span><span class="sxs-lookup"><span data-stu-id="f30b0-131">Yes</span></span>           |



 

 




