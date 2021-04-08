---
title: À propos du stockage structuré
description: Les systèmes de fichiers traditionnels rencontrent des difficultés lorsqu’ils tentent de stocker efficacement plusieurs types d’objets dans un même document.
ms.assetid: a571f7c2-0490-463c-813e-de4a9fd12a2d
keywords:
- À propos du stockage structuré
- Stockage structuré Strctd STG, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d048907c196c871af943e5a15cc95b367724a31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672253"
---
# <a name="about-structured-storage"></a><span data-ttu-id="d420e-105">À propos du stockage structuré</span><span class="sxs-lookup"><span data-stu-id="d420e-105">About Structured Storage</span></span>

<span data-ttu-id="d420e-106">Les systèmes de fichiers traditionnels rencontrent des difficultés lorsqu’ils tentent de stocker efficacement plusieurs types d’objets dans un même document.</span><span class="sxs-lookup"><span data-stu-id="d420e-106">Traditional file systems encounter challenges when they attempt to store efficiently multiple kinds of objects in one document.</span></span> <span data-ttu-id="d420e-107">COM fournit une solution : un système de fichiers dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d420e-107">COM provides a solution: a file system within a file.</span></span> <span data-ttu-id="d420e-108">Le stockage structuré COM définit la manière de traiter une entité de fichier unique comme une collection structurée de deux types d’objets (stockages et flux) qui s’exécutent comme des répertoires et des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d420e-108">COM structured storage defines how to treat a single file entity as a structured collection of two types of objects—storages and streams—that perform like directories and files.</span></span> <span data-ttu-id="d420e-109">Ce schéma est appelé *stockage structuré*.</span><span class="sxs-lookup"><span data-stu-id="d420e-109">This scheme is called *structured storage*.</span></span> <span data-ttu-id="d420e-110">L’objectif du stockage structuré est de réduire les pénalités de performances et la surcharge associées au stockage d’objets distincts dans un fichier plat.</span><span class="sxs-lookup"><span data-stu-id="d420e-110">The purpose of structured storage is to reduce the performance penalties and overhead associated with storing separate objects in a flat file.</span></span>

<span data-ttu-id="d420e-111">Cette section contient une vue d’ensemble des avantages et des principes de base du stockage structuré, des jeux de propriétés et du stockage structuré asynchrone, ainsi qu’un aperçu de l’historique des systèmes de fichiers :</span><span class="sxs-lookup"><span data-stu-id="d420e-111">This section contains an overview of structured storage benefits and fundamentals, property sets and asynchronous structured storage as well as a historical look at file systems:</span></span>

-   <span data-ttu-id="d420e-112">Implémentation de fichier composé</span><span class="sxs-lookup"><span data-stu-id="d420e-112">Compound file implementation</span></span>
-   <span data-ttu-id="d420e-113">Implémentation du système de fichiers NTFS</span><span class="sxs-lookup"><span data-stu-id="d420e-113">NTFS file system implementation</span></span>
-   <span data-ttu-id="d420e-114">Implémentation autonome</span><span class="sxs-lookup"><span data-stu-id="d420e-114">Stand-alone implementation</span></span>

<span data-ttu-id="d420e-115">Cette section contient des liens vers [l’évolution des systèmes de fichiers](the-evolution-of-file-systems.md), des [stockages et des flux](storages-and-streams.md), des [fichiers composés](compound-files.md), des notions de base sur le [stockage structuré](structured-storage-fundamentals.md)et des [exemples de stockage structuré](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="d420e-115">This section includes links to [The Evolution of File Systems](the-evolution-of-file-systems.md), [Storages and Streams](storages-and-streams.md), [Compound Files](compound-files.md), [Structured Storage Fundamentals](structured-storage-fundamentals.md), and [Structured Storage Samples](using-structured-storage.md).</span></span>

 

 




