---
description: Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: élément faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203351"
---
# <a name="faultinfo-element"></a><span data-ttu-id="b6d3c-103">élément faultInfo</span><span class="sxs-lookup"><span data-stu-id="b6d3c-103">faultInfo element</span></span>

<span data-ttu-id="b6d3c-104">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="b6d3c-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b6d3c-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="b6d3c-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b6d3c-106">Attributes</span></span>

<span data-ttu-id="b6d3c-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b6d3c-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6d3c-108">Child elements</span></span>

<span data-ttu-id="b6d3c-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6d3c-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b6d3c-110">Parent elements</span></span>



| <span data-ttu-id="b6d3c-111">Élément</span><span class="sxs-lookup"><span data-stu-id="b6d3c-111">Element</span></span>                                                                         | <span data-ttu-id="b6d3c-112">Description</span><span class="sxs-lookup"><span data-stu-id="b6d3c-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6d3c-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b6d3c-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="b6d3c-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b6d3c-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b6d3c-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b6d3c-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b6d3c-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b6d3c-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="b6d3c-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="b6d3c-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b6d3c-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="b6d3c-120">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="b6d3c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b6d3c-121">Remarks</span></span>

<span data-ttu-id="b6d3c-122">Les valeurs possibles sont 1 (paramètres d’erreur inclus) et 0 (paramètres d’erreur exclus).</span><span class="sxs-lookup"><span data-stu-id="b6d3c-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="b6d3c-123">Par défaut, les paramètres d’erreur sont exclus.</span><span class="sxs-lookup"><span data-stu-id="b6d3c-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="b6d3c-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6d3c-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b6d3c-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6d3c-125">Minimum supported system</span></span><br/> | <span data-ttu-id="b6d3c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6d3c-126">Windows Vista</span></span> |
| <span data-ttu-id="b6d3c-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b6d3c-127">Can be empty</span></span>                        | <span data-ttu-id="b6d3c-128">Oui</span><span class="sxs-lookup"><span data-stu-id="b6d3c-128">Yes</span></span>           |



 

 




