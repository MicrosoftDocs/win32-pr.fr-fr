---
title: Avantages du stockage structuré
description: COM fournit un ensemble de services, collectivement appelé stockage structuré.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Stockage structuré Strctd STG, avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671673"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="c098b-104">Avantages du stockage structuré</span><span class="sxs-lookup"><span data-stu-id="c098b-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="c098b-105">COM fournit un ensemble de services, collectivement appelé stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="c098b-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="c098b-106">Parmi les avantages de ces services, citons la réduction des pénalités de performances et de la surcharge associée au stockage d’objets distincts dans un fichier plat.</span><span class="sxs-lookup"><span data-stu-id="c098b-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="c098b-107">Au lieu d’un fichier plat, COM stocke les objets séparés dans un seul fichier structuré composé de deux éléments principaux : les objets de stockage et les objets de flux.</span><span class="sxs-lookup"><span data-stu-id="c098b-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="c098b-108">Ensemble, ils fonctionnent comme un système de fichiers dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c098b-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="c098b-109">Le stockage structuré résout les problèmes de performances en éliminant la nécessité de réécrire entièrement un fichier dans le stockage chaque fois qu’un nouvel objet est ajouté à un fichier composé, ou lorsque la taille d’un objet existant augmente.</span><span class="sxs-lookup"><span data-stu-id="c098b-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="c098b-110">Les nouvelles données sont écrites à l’emplacement suivant disponible dans le stockage permanent, et l’objet de stockage met à jour la table des pointeurs qu’elle gère pour suivre les emplacements de ses objets de stockage et de flux.</span><span class="sxs-lookup"><span data-stu-id="c098b-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="c098b-111">En même temps, le stockage structuré permet aux utilisateurs finaux d’interagir et de gérer un fichier composé comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.</span><span class="sxs-lookup"><span data-stu-id="c098b-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="c098b-112">Le stockage structuré présente également d’autres avantages :</span><span class="sxs-lookup"><span data-stu-id="c098b-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="c098b-113">**Accès incrémentiel**.</span><span class="sxs-lookup"><span data-stu-id="c098b-113">**Incremental access**.</span></span> <span data-ttu-id="c098b-114">Si un utilisateur a besoin d’accéder à un objet dans un fichier composé, il peut charger et enregistrer uniquement cet objet, plutôt que le fichier entier.</span><span class="sxs-lookup"><span data-stu-id="c098b-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="c098b-115">**Utilisation multiple**.</span><span class="sxs-lookup"><span data-stu-id="c098b-115">**Multiple use**.</span></span> <span data-ttu-id="c098b-116">Plusieurs utilisateurs finaux ou applications peuvent lire et écrire simultanément des informations dans le même fichier composé.</span><span class="sxs-lookup"><span data-stu-id="c098b-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="c098b-117">**Traitement des transactions**.</span><span class="sxs-lookup"><span data-stu-id="c098b-117">**Transaction processing**.</span></span> <span data-ttu-id="c098b-118">Les utilisateurs peuvent lire ou écrire dans les fichiers composés COM en mode transactionnel, où les modifications apportées au fichier sont mises en mémoire tampon et peuvent ensuite être validées dans le fichier ou inversées.</span><span class="sxs-lookup"><span data-stu-id="c098b-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="c098b-119">**Enregistrements de mémoire insuffisante**.</span><span class="sxs-lookup"><span data-stu-id="c098b-119">**Low-memory saves**.</span></span> <span data-ttu-id="c098b-120">Le stockage structuré fournit des fonctionnalités permettant d’enregistrer des fichiers dans des situations de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="c098b-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




