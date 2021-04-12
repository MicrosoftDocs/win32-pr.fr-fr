---
description: Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: élément stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209851"
---
# <a name="stubfunction-element"></a><span data-ttu-id="9f503-103">élément stubFunction</span><span class="sxs-lookup"><span data-stu-id="9f503-103">stubFunction element</span></span>

<span data-ttu-id="9f503-104">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="9f503-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9f503-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9f503-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="9f503-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="9f503-106">Attributes</span></span>

<span data-ttu-id="9f503-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9f503-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9f503-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9f503-108">Child elements</span></span>

<span data-ttu-id="9f503-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="9f503-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9f503-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9f503-110">Parent elements</span></span>



| <span data-ttu-id="9f503-111">Élément</span><span class="sxs-lookup"><span data-stu-id="9f503-111">Element</span></span>                                                       | <span data-ttu-id="9f503-112">Description</span><span class="sxs-lookup"><span data-stu-id="9f503-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="9f503-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9f503-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="9f503-114">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="9f503-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9f503-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9f503-115">Remarks</span></span>

<span data-ttu-id="9f503-116">Les références de fonction stub sont utilisées dans les scénarios d’hébergement pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="9f503-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="9f503-117">Les valeurs valides pour cet élément sont 1 (TRUE/stub Function References incluses) et 0 (FALSe/aucune référence à la fonction stub incluse).</span><span class="sxs-lookup"><span data-stu-id="9f503-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="9f503-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9f503-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9f503-119">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f503-119">Minimum supported system</span></span><br/> | <span data-ttu-id="9f503-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f503-120">Windows Vista</span></span> |
| <span data-ttu-id="9f503-121">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="9f503-121">Can be empty</span></span>                        | <span data-ttu-id="9f503-122">Oui</span><span class="sxs-lookup"><span data-stu-id="9f503-122">Yes</span></span>           |



 

 




