---
description: Spécifie le type annulateur à utiliser par une fonction stub d’opérations.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: élément operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522704"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="8f154-103">élément operationDeallocator</span><span class="sxs-lookup"><span data-stu-id="8f154-103">operationDeallocator element</span></span>

<span data-ttu-id="8f154-104">Spécifie le type annulateur à utiliser par la fonction stub d’une opération.</span><span class="sxs-lookup"><span data-stu-id="8f154-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="8f154-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="8f154-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="8f154-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="8f154-106">Attributes</span></span>



| <span data-ttu-id="8f154-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="8f154-107">Attribute</span></span>                  | <span data-ttu-id="8f154-108">Type</span><span class="sxs-lookup"><span data-stu-id="8f154-108">Type</span></span>                         | <span data-ttu-id="8f154-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8f154-109">Required</span></span>       | <span data-ttu-id="8f154-110">Description</span><span class="sxs-lookup"><span data-stu-id="8f154-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f154-111">**annulateur**</span><span class="sxs-lookup"><span data-stu-id="8f154-111">**deallocator**</span></span><br/> | <span data-ttu-id="8f154-112">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="8f154-112">character\_string</span></span><br/> | <span data-ttu-id="8f154-113">Oui</span><span class="sxs-lookup"><span data-stu-id="8f154-113">Yes</span></span><br/> | <span data-ttu-id="8f154-114">Annulateur à utiliser pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="8f154-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="8f154-115">Les chaînes suivantes sont des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="8f154-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="8f154-116"><span id="none"></span><span id="NONE"></span>\* \* \* \* <dt>aucun \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* \* \* \* \* <dt>WSDFreeLinkedMemory \* \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* \* \* \* \* \* \* \* \* \* <dt>CoTaskMemFree \* \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* \* \* \* \* <dt>gratuit \* \*</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* \* \* \* \* <dt>supprimer \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* \* \* \* <dt>deleteArray \* \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* \* \* \* \* \* \* \* \* <dt>Version \*</dt> \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8f154-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="8f154-117">**opération**</span><span class="sxs-lookup"><span data-stu-id="8f154-117">**operation**</span></span><br/>   | <span data-ttu-id="8f154-118">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="8f154-118">character\_string</span></span><br/> | <span data-ttu-id="8f154-119">Oui</span><span class="sxs-lookup"><span data-stu-id="8f154-119">Yes</span></span><br/> | <span data-ttu-id="8f154-120">Nom de l'opération.</span><span class="sxs-lookup"><span data-stu-id="8f154-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="8f154-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8f154-121">Child elements</span></span>

<span data-ttu-id="8f154-122">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="8f154-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8f154-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8f154-123">Parent elements</span></span>



| <span data-ttu-id="8f154-124">Élément</span><span class="sxs-lookup"><span data-stu-id="8f154-124">Element</span></span>                                               | <span data-ttu-id="8f154-125">Description</span><span class="sxs-lookup"><span data-stu-id="8f154-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f154-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8f154-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="8f154-127">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="8f154-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8f154-128">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8f154-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8f154-129">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f154-129">Minimum supported system</span></span><br/> | <span data-ttu-id="8f154-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f154-130">Windows Vista</span></span> |
| <span data-ttu-id="8f154-131">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="8f154-131">Can be empty</span></span>                        | <span data-ttu-id="8f154-132">Oui</span><span class="sxs-lookup"><span data-stu-id="8f154-132">Yes</span></span>           |



 

 




