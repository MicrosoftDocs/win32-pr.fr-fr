---
title: Stockage structuré
description: Le stockage structuré fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Stockage structuré Strctd STG
- Stockage structuré Strctd STG, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315707"
---
# <a name="structured-storage"></a><span data-ttu-id="6f906-105">Stockage structuré</span><span class="sxs-lookup"><span data-stu-id="6f906-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="6f906-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="6f906-106">Purpose</span></span>

<span data-ttu-id="6f906-107">Le stockage structuré fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.</span><span class="sxs-lookup"><span data-stu-id="6f906-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="6f906-108">L’objectif du stockage structuré est de réduire les pénalités de performances et la surcharge associées au stockage d’objets distincts dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="6f906-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="6f906-109">Le stockage structuré fournit une solution en définissant comment gérer une entité de fichier unique comme une collection structurée de deux types de stockages d’objets et de flux via une implémentation standard appelée fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="6f906-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="6f906-110">Cela permet à l’utilisateur d’interagir avec un fichier composé, et de le gérer, comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.</span><span class="sxs-lookup"><span data-stu-id="6f906-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6f906-111">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="6f906-111">Where applicable</span></span>

<span data-ttu-id="6f906-112">Le stockage structuré peut être utilisé sur les systèmes d’exploitation basés sur Microsoft COM.</span><span class="sxs-lookup"><span data-stu-id="6f906-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6f906-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="6f906-113">Developer audience</span></span>

<span data-ttu-id="6f906-114">La documentation sur le stockage structuré est destinée aux programmeurs C et C++ expérimentés et aux développeurs de systèmes COM.</span><span class="sxs-lookup"><span data-stu-id="6f906-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="6f906-115">Le stockage structuré prend principalement en charge les langages de programmation C et C++. Toutefois, toute technologie COM prendra également en charge tout langage de programmation qui utilise des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="6f906-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="6f906-116">Une bonne compréhension des technologies COM est prérequise pour l’utilisation du stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="6f906-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6f906-117">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="6f906-117">Run-time requirements</span></span>

<span data-ttu-id="6f906-118">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser un élément d’API particulier, consultez la section Configuration requise de la documentation relative à l’élément.</span><span class="sxs-lookup"><span data-stu-id="6f906-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f906-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="6f906-119">In this section</span></span>



| <span data-ttu-id="6f906-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="6f906-120">Topic</span></span>                                                               | <span data-ttu-id="6f906-121">Description</span><span class="sxs-lookup"><span data-stu-id="6f906-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f906-122">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="6f906-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="6f906-123">Informations générales sur le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="6f906-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="6f906-124">Utilisation du stockage structuré</span><span class="sxs-lookup"><span data-stu-id="6f906-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="6f906-125">Utilisation d’informations pour le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="6f906-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6f906-126">Référence</span><span class="sxs-lookup"><span data-stu-id="6f906-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="6f906-127">Documentation des interfaces, des fonctions, des structures et des énumérations spécifiques au stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="6f906-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="6f906-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f906-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="6f906-129">Exemples de code écrits en C++.</span><span class="sxs-lookup"><span data-stu-id="6f906-129">Code examples written in C++.</span></span> <span data-ttu-id="6f906-130">Pour plus d’informations, consultez [noms dans IStorage](names-in-istorage.md), [en-tête de jeu de propriétés](property-set-header.md), [section](section.md), stockage des [jeux de propriétés](storing-property-sets.md)et [utilisation du stockage structuré](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="6f906-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6f906-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f906-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f906-132">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="6f906-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 

