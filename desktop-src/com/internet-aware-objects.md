---
title: Objets Internet-Aware
description: Objets Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941411"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="5d5ae-103">Objets Internet-Aware</span><span class="sxs-lookup"><span data-stu-id="5d5ae-103">Internet-Aware Objects</span></span>

<span data-ttu-id="5d5ae-104">Certaines catégories sont identifiées pour couvrir les interfaces persistances ; celles-ci ont été identifiées à la suite de la définition de la façon dont les contrôles fonctionnent sur Internet.</span><span class="sxs-lookup"><span data-stu-id="5d5ae-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="5d5ae-105">Un conteneur qui ne prend pas en charge la plage complète d’interfaces persistance doit s’assurer qu’il n’héberge pas un contrôle qui requiert une combinaison d’interfaces qu’il ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="5d5ae-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="5d5ae-106">Les tableaux suivants décrivent la signification de différentes catégories à la fois comme catégories implémentées et requises.</span><span class="sxs-lookup"><span data-stu-id="5d5ae-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="5d5ae-107">Catégories requises</span><span class="sxs-lookup"><span data-stu-id="5d5ae-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="5d5ae-108">Description</span><span class="sxs-lookup"><span data-stu-id="5d5ae-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d5ae-109">CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, catidd \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5d5ae-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="5d5ae-110">Chacune de ces catégories s’exclut mutuellement et n’est utilisée que lorsqu’un objet ne prend en charge qu’un seul mécanisme de persistance (par conséquent, l’exclusion mutuelle).</span><span class="sxs-lookup"><span data-stu-id="5d5ae-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="5d5ae-111">Les conteneurs qui ne prennent pas en charge le mécanisme de persistance décrit par l’une de ces catégories doivent empêcher eux-mêmes de créer des objets de classes donc marqués.</span><span class="sxs-lookup"><span data-stu-id="5d5ae-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="5d5ae-112">RequiresDataPathHost CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="5d5ae-113">L’objet nécessite la possibilité d’enregistrer des données dans un ou plusieurs chemins d’accès et requiert l’implication d’un conteneur, ce qui nécessite une prise en charge de conteneur pour [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d5ae-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="5d5ae-114">Catégories implémentées</span><span class="sxs-lookup"><span data-stu-id="5d5ae-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="5d5ae-115">Description</span><span class="sxs-lookup"><span data-stu-id="5d5ae-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d5ae-116">CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, catidd \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5d5ae-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="5d5ae-117">L’objet prend en charge le mécanisme IPersist correspondant \* pour la catégorie.</span><span class="sxs-lookup"><span data-stu-id="5d5ae-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="5d5ae-118">Le tableau suivant fournit le CATID exact affecté à chaque catégorie :</span><span class="sxs-lookup"><span data-stu-id="5d5ae-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="5d5ae-119">Category</span><span class="sxs-lookup"><span data-stu-id="5d5ae-119">Category</span></span>                                | <span data-ttu-id="5d5ae-120">CATID</span><span class="sxs-lookup"><span data-stu-id="5d5ae-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="5d5ae-121">RequiresDataPathHost CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="5d5ae-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-123">PersistsToMoniker CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="5d5ae-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-125">PersistsToStorage CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="5d5ae-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-127">PersistsToStreamInit CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="5d5ae-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-129">PersistsToStream CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="5d5ae-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-131">PersistsToMemory CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="5d5ae-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-133">PersistsToFile CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="5d5ae-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="5d5ae-135">PersistsToPropertyBag CATID \_</span><span class="sxs-lookup"><span data-stu-id="5d5ae-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="5d5ae-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="5d5ae-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5d5ae-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d5ae-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d5ae-138">Catégories de composant</span><span class="sxs-lookup"><span data-stu-id="5d5ae-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

