---
description: Normalement, les informations de débogage sont stockées dans un fichier de symboles distinct de l’exécutable.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Fichiers de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110203"
---
# <a name="symbol-files"></a><span data-ttu-id="25a23-103">Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="25a23-103">Symbol Files</span></span>

<span data-ttu-id="25a23-104">Normalement, les informations de débogage sont stockées dans un fichier de symboles distinct de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="25a23-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="25a23-105">L’implémentation de ces informations de débogage a changé au cours des années, et la documentation suivante fournit des conseils sur ces différentes implémentations.</span><span class="sxs-lookup"><span data-stu-id="25a23-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="25a23-106">fichiers PDB</span><span class="sxs-lookup"><span data-stu-id="25a23-106">PDB files</span></span>

<span data-ttu-id="25a23-107">Toutes les versions modernes des compilateurs Microsoft stockent les informations de débogage relatives à un exécutable compilé dans un fichier *de base de données du programme* (. pdb) distinct.</span><span class="sxs-lookup"><span data-stu-id="25a23-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="25a23-108">Ce fichier est communément appelé *PDB*.</span><span class="sxs-lookup"><span data-stu-id="25a23-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="25a23-109">Les données sont stockées dans un fichier distinct de l’exécutable pour limiter la taille de l’exécutable, ce qui permet d’économiser de l’espace de stockage sur disque et de réduire le temps nécessaire au chargement des données.</span><span class="sxs-lookup"><span data-stu-id="25a23-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="25a23-110">Cette méthode permet également de distribuer l’exécutable sans divulguer ces informations importantes, ce qui peut rendre le programme plus facile à rétroconcevoir.</span><span class="sxs-lookup"><span data-stu-id="25a23-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="25a23-111">Pour créer un fichier PDB, générez votre fichier exécutable avec des informations de débogage en fonction des instructions de vos outils de génération.</span><span class="sxs-lookup"><span data-stu-id="25a23-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="25a23-112">L’API DbgHelp peut utiliser des fichiers PDB pour obtenir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="25a23-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="25a23-113">public et exportations</span><span class="sxs-lookup"><span data-stu-id="25a23-113">publics and exports</span></span>
-   <span data-ttu-id="25a23-114">symboles globaux</span><span class="sxs-lookup"><span data-stu-id="25a23-114">global symbols</span></span>
-   <span data-ttu-id="25a23-115">symboles locaux</span><span class="sxs-lookup"><span data-stu-id="25a23-115">local symbols</span></span>
-   <span data-ttu-id="25a23-116">données de type</span><span class="sxs-lookup"><span data-stu-id="25a23-116">type data</span></span>
-   <span data-ttu-id="25a23-117">fichiers sources</span><span class="sxs-lookup"><span data-stu-id="25a23-117">source files</span></span>
-   <span data-ttu-id="25a23-118">numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="25a23-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="25a23-119">Fichiers DBG et informations de débogage incorporés</span><span class="sxs-lookup"><span data-stu-id="25a23-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="25a23-120">Les versions précédentes de l’ensemble d’outils Microsoft utilisaient pour incorporer les informations de débogage dans le fichier exécutable, mais il serait normalement éliminé dans un fichier distinct avec une extension. dbg.</span><span class="sxs-lookup"><span data-stu-id="25a23-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="25a23-121">C’est ce qu’on appelle communément un fichier *dbg* .</span><span class="sxs-lookup"><span data-stu-id="25a23-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="25a23-122">Les fichiers DBG utilisent le même format de fichier PE que les exécutables.</span><span class="sxs-lookup"><span data-stu-id="25a23-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="25a23-123">La prise en charge de l’API DbgHelp pour DBGs et les informations de débogage intégrées est limitée et comprend les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="25a23-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="25a23-124">public et exportations</span><span class="sxs-lookup"><span data-stu-id="25a23-124">publics and exports</span></span>
-   <span data-ttu-id="25a23-125">symboles globaux</span><span class="sxs-lookup"><span data-stu-id="25a23-125">global symbols</span></span>

 

 



