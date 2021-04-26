---
description: Spécifie le type de annulateur à utiliser par une fonction stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: élément annulateur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994936"
---
# <a name="deallocator-element"></a><span data-ttu-id="5d9a4-103">élément annulateur</span><span class="sxs-lookup"><span data-stu-id="5d9a4-103">deallocator element</span></span>

<span data-ttu-id="5d9a4-104">Spécifie le type de annulateur à utiliser par une fonction stub.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="5d9a4-105">Usage</span><span class="sxs-lookup"><span data-stu-id="5d9a4-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="5d9a4-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="5d9a4-106">Attributes</span></span>

<span data-ttu-id="5d9a4-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5d9a4-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5d9a4-108">Child elements</span></span>

<span data-ttu-id="5d9a4-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5d9a4-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5d9a4-110">Parent elements</span></span>



| <span data-ttu-id="5d9a4-111">Élément</span><span class="sxs-lookup"><span data-stu-id="5d9a4-111">Element</span></span>                                               | <span data-ttu-id="5d9a4-112">Description</span><span class="sxs-lookup"><span data-stu-id="5d9a4-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d9a4-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5d9a4-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="5d9a4-114">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5d9a4-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d9a4-115">Remarks</span></span>

<span data-ttu-id="5d9a4-116">Le type annulateur doit être placé dans une paire de <deallocator></deallocator> balises.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="5d9a4-117">Les chaînes suivantes sont des valeurs annulateur valides :</span><span class="sxs-lookup"><span data-stu-id="5d9a4-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="5d9a4-118">aucun</span><span class="sxs-lookup"><span data-stu-id="5d9a4-118">none</span></span>
-   <span data-ttu-id="5d9a4-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="5d9a4-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="5d9a4-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="5d9a4-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="5d9a4-121">gratuit</span><span class="sxs-lookup"><span data-stu-id="5d9a4-121">free</span></span>
-   <span data-ttu-id="5d9a4-122">supprimer</span><span class="sxs-lookup"><span data-stu-id="5d9a4-122">delete</span></span>
-   <span data-ttu-id="5d9a4-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="5d9a4-123">deleteArray</span></span>
-   <span data-ttu-id="5d9a4-124">Libérer</span><span class="sxs-lookup"><span data-stu-id="5d9a4-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="5d9a4-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5d9a4-125">Element information</span></span>



| <span data-ttu-id="5d9a4-126">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5d9a4-126">Label</span></span> | <span data-ttu-id="5d9a4-127">Value</span><span class="sxs-lookup"><span data-stu-id="5d9a4-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="5d9a4-128">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d9a4-128">Minimum supported system</span></span><br/> | <span data-ttu-id="5d9a4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d9a4-129">Windows Vista</span></span> |
| <span data-ttu-id="5d9a4-130">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5d9a4-130">Can be empty</span></span>                        | <span data-ttu-id="5d9a4-131">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a4-131">Yes</span></span>           |



 

 




