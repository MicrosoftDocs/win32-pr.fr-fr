---
description: Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: élément Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994956"
---
# <a name="async-element"></a><span data-ttu-id="2c3ac-103">élément Async</span><span class="sxs-lookup"><span data-stu-id="2c3ac-103">async element</span></span>

<span data-ttu-id="2c3ac-104">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="2c3ac-105">Usage</span><span class="sxs-lookup"><span data-stu-id="2c3ac-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="2c3ac-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="2c3ac-106">Attributes</span></span>

<span data-ttu-id="2c3ac-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2c3ac-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2c3ac-108">Child elements</span></span>

<span data-ttu-id="2c3ac-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2c3ac-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2c3ac-110">Parent elements</span></span>



| <span data-ttu-id="2c3ac-111">Élément</span><span class="sxs-lookup"><span data-stu-id="2c3ac-111">Element</span></span>                                                                         | <span data-ttu-id="2c3ac-112">Description</span><span class="sxs-lookup"><span data-stu-id="2c3ac-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c3ac-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2c3ac-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="2c3ac-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="2c3ac-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2c3ac-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="2c3ac-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="2c3ac-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="2c3ac-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="2c3ac-118">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="2c3ac-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="2c3ac-119">Remarks</span></span>

<span data-ttu-id="2c3ac-120">Les valeurs possibles sont 1 (opérations asynchrones incluses) et 0 (opérations asynchrones par défaut exclues).</span><span class="sxs-lookup"><span data-stu-id="2c3ac-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="2c3ac-121">Un proxy peut avoir des versions asynchrones et synchrones des mêmes opérations.</span><span class="sxs-lookup"><span data-stu-id="2c3ac-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="2c3ac-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2c3ac-122">Element information</span></span>



| <span data-ttu-id="2c3ac-123">Étiquette</span><span class="sxs-lookup"><span data-stu-id="2c3ac-123">Label</span></span> | <span data-ttu-id="2c3ac-124">Value</span><span class="sxs-lookup"><span data-stu-id="2c3ac-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2c3ac-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c3ac-125">Minimum supported system</span></span><br/> | <span data-ttu-id="2c3ac-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c3ac-126">Windows Vista</span></span> |
| <span data-ttu-id="2c3ac-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="2c3ac-127">Can be empty</span></span>                        | <span data-ttu-id="2c3ac-128">Oui</span><span class="sxs-lookup"><span data-stu-id="2c3ac-128">Yes</span></span>           |



 

 




