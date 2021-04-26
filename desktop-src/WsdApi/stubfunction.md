---
description: Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: élément stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994146"
---
# <a name="stubfunction-element"></a><span data-ttu-id="17182-103">élément stubFunction</span><span class="sxs-lookup"><span data-stu-id="17182-103">stubFunction element</span></span>

<span data-ttu-id="17182-104">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="17182-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="17182-105">Usage</span><span class="sxs-lookup"><span data-stu-id="17182-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="17182-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="17182-106">Attributes</span></span>

<span data-ttu-id="17182-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="17182-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17182-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17182-108">Child elements</span></span>

<span data-ttu-id="17182-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="17182-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="17182-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17182-110">Parent elements</span></span>



| <span data-ttu-id="17182-111">Élément</span><span class="sxs-lookup"><span data-stu-id="17182-111">Element</span></span>                                                       | <span data-ttu-id="17182-112">Description</span><span class="sxs-lookup"><span data-stu-id="17182-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="17182-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="17182-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="17182-114">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="17182-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="17182-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="17182-115">Remarks</span></span>

<span data-ttu-id="17182-116">Les références de fonction stub sont utilisées dans les scénarios d’hébergement pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="17182-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="17182-117">Les valeurs valides pour cet élément sont 1 (TRUE/stub Function References incluses) et 0 (FALSe/aucune référence à la fonction stub incluse).</span><span class="sxs-lookup"><span data-stu-id="17182-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="17182-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17182-118">Element information</span></span>



| <span data-ttu-id="17182-119">Étiquette</span><span class="sxs-lookup"><span data-stu-id="17182-119">Label</span></span> | <span data-ttu-id="17182-120">Value</span><span class="sxs-lookup"><span data-stu-id="17182-120">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="17182-121">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17182-121">Minimum supported system</span></span><br/> | <span data-ttu-id="17182-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17182-122">Windows Vista</span></span> |
| <span data-ttu-id="17182-123">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="17182-123">Can be empty</span></span>                        | <span data-ttu-id="17182-124">Oui</span><span class="sxs-lookup"><span data-stu-id="17182-124">Yes</span></span>           |



 

 




