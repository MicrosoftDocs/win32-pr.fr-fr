---
description: Spécifie le type de annulateur à utiliser par une fonction stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: élément annulateur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202272"
---
# <a name="deallocator-element"></a><span data-ttu-id="3094e-103">élément annulateur</span><span class="sxs-lookup"><span data-stu-id="3094e-103">deallocator element</span></span>

<span data-ttu-id="3094e-104">Spécifie le type de annulateur à utiliser par une fonction stub.</span><span class="sxs-lookup"><span data-stu-id="3094e-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="3094e-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3094e-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="3094e-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="3094e-106">Attributes</span></span>

<span data-ttu-id="3094e-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3094e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3094e-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3094e-108">Child elements</span></span>

<span data-ttu-id="3094e-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="3094e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3094e-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3094e-110">Parent elements</span></span>



| <span data-ttu-id="3094e-111">Élément</span><span class="sxs-lookup"><span data-stu-id="3094e-111">Element</span></span>                                               | <span data-ttu-id="3094e-112">Description</span><span class="sxs-lookup"><span data-stu-id="3094e-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3094e-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="3094e-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="3094e-114">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="3094e-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3094e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3094e-115">Remarks</span></span>

<span data-ttu-id="3094e-116">Le type annulateur doit être placé dans une paire de <deallocator></deallocator> balises.</span><span class="sxs-lookup"><span data-stu-id="3094e-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="3094e-117">Les chaînes suivantes sont des valeurs annulateur valides :</span><span class="sxs-lookup"><span data-stu-id="3094e-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="3094e-118">aucun</span><span class="sxs-lookup"><span data-stu-id="3094e-118">none</span></span>
-   <span data-ttu-id="3094e-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="3094e-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="3094e-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="3094e-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="3094e-121">gratuit</span><span class="sxs-lookup"><span data-stu-id="3094e-121">free</span></span>
-   <span data-ttu-id="3094e-122">supprimer</span><span class="sxs-lookup"><span data-stu-id="3094e-122">delete</span></span>
-   <span data-ttu-id="3094e-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="3094e-123">deleteArray</span></span>
-   <span data-ttu-id="3094e-124">Libérer</span><span class="sxs-lookup"><span data-stu-id="3094e-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="3094e-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3094e-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="3094e-126">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3094e-126">Minimum supported system</span></span><br/> | <span data-ttu-id="3094e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3094e-127">Windows Vista</span></span> |
| <span data-ttu-id="3094e-128">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="3094e-128">Can be empty</span></span>                        | <span data-ttu-id="3094e-129">Oui</span><span class="sxs-lookup"><span data-stu-id="3094e-129">Yes</span></span>           |



 

 




