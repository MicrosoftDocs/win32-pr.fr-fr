---
description: Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: élément faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995856"
---
# <a name="faultinfo-element"></a><span data-ttu-id="52cbe-103">élément faultInfo</span><span class="sxs-lookup"><span data-stu-id="52cbe-103">faultInfo element</span></span>

<span data-ttu-id="52cbe-104">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="52cbe-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="52cbe-105">Usage</span><span class="sxs-lookup"><span data-stu-id="52cbe-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="52cbe-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="52cbe-106">Attributes</span></span>

<span data-ttu-id="52cbe-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="52cbe-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="52cbe-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52cbe-108">Child elements</span></span>

<span data-ttu-id="52cbe-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="52cbe-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="52cbe-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52cbe-110">Parent elements</span></span>



| <span data-ttu-id="52cbe-111">Élément</span><span class="sxs-lookup"><span data-stu-id="52cbe-111">Element</span></span>                                                                         | <span data-ttu-id="52cbe-112">Description</span><span class="sxs-lookup"><span data-stu-id="52cbe-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52cbe-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="52cbe-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="52cbe-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="52cbe-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="52cbe-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="52cbe-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="52cbe-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="52cbe-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="52cbe-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="52cbe-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="52cbe-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="52cbe-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="52cbe-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="52cbe-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="52cbe-120">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="52cbe-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="52cbe-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="52cbe-121">Remarks</span></span>

<span data-ttu-id="52cbe-122">Les valeurs possibles sont 1 (paramètres d’erreur inclus) et 0 (paramètres d’erreur exclus).</span><span class="sxs-lookup"><span data-stu-id="52cbe-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="52cbe-123">Par défaut, les paramètres d’erreur sont exclus.</span><span class="sxs-lookup"><span data-stu-id="52cbe-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="52cbe-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="52cbe-124">Element information</span></span>



| <span data-ttu-id="52cbe-125">Étiquette</span><span class="sxs-lookup"><span data-stu-id="52cbe-125">Label</span></span> | <span data-ttu-id="52cbe-126">Value</span><span class="sxs-lookup"><span data-stu-id="52cbe-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="52cbe-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cbe-127">Minimum supported system</span></span><br/> | <span data-ttu-id="52cbe-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52cbe-128">Windows Vista</span></span> |
| <span data-ttu-id="52cbe-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="52cbe-129">Can be empty</span></span>                        | <span data-ttu-id="52cbe-130">Oui</span><span class="sxs-lookup"><span data-stu-id="52cbe-130">Yes</span></span>           |



 

 




