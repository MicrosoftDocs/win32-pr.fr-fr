---
title: Components
description: Composants
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL sur Windows, composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512265"
---
# <a name="components"></a><span data-ttu-id="74568-104">Composants</span><span class="sxs-lookup"><span data-stu-id="74568-104">Components</span></span>

<span data-ttu-id="74568-105">L’implémentation de OpenGL par Microsoft dans Windows comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="74568-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="74568-106">Ensemble complet des commandes OpenGL actuelles</span><span class="sxs-lookup"><span data-stu-id="74568-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="74568-107">OpenGL contient une bibliothèque de fonctions principales pour les opérations de graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="74568-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="74568-108">Ces fonctions de base sont utilisées pour gérer la description de la forme de l’objet, la transformation de matrice, l’éclairage, la coloration, la texture, le découpage, les bitmaps, le brouillard et l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="74568-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="74568-109">Les noms de ces fonctions principales ont un préfixe « GL ».</span><span class="sxs-lookup"><span data-stu-id="74568-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="74568-110">La plupart des commandes OpenGL ont plusieurs variantes, qui diffèrent du nombre et du type de leurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="74568-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="74568-111">En comptant toutes les variantes, il y a plus de 300 commandes OpenGL.</span><span class="sxs-lookup"><span data-stu-id="74568-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="74568-112">La bibliothèque OpenGL Utility (GLU)</span><span class="sxs-lookup"><span data-stu-id="74568-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="74568-113">Cette bibliothèque de fonctions auxiliaires complète les fonctions OpenGL principales.</span><span class="sxs-lookup"><span data-stu-id="74568-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="74568-114">Les commandes gèrent la prise en charge de la texture, la transformation des coordonnées, le pavage polygonal, les sphères de rendu, les cylindres et les disques, les courbes et les surfaces NURBS (non-uniform rational B-spline) et la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="74568-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="74568-115">Bibliothèque auxiliaire du Guide de programmation OpenGL</span><span class="sxs-lookup"><span data-stu-id="74568-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="74568-116">Il s’agit d’une bibliothèque simple, indépendante de la plate-forme, de fonctions pour gérer Windows, gérer des événements d’entrée, dessiner des objets 3D classiques, gérer un processus en arrière-plan et exécuter un programme.</span><span class="sxs-lookup"><span data-stu-id="74568-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="74568-117">Les routines de gestion et d’entrée des fenêtres fournissent un niveau de base de fonctionnalité qui vous permet de commencer rapidement la programmation dans OpenGL.</span><span class="sxs-lookup"><span data-stu-id="74568-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="74568-118">Toutefois, ne les utilisez pas dans une application de production.</span><span class="sxs-lookup"><span data-stu-id="74568-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="74568-119">Voici quelques raisons pour cet avertissement :</span><span class="sxs-lookup"><span data-stu-id="74568-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="74568-120">La boucle de message se trouve dans le code de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="74568-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="74568-121">Il n’existe aucun moyen d’ajouter des gestionnaires pour des \* messages WM supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="74568-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="74568-122">Il y a très peu de prise en charge des palettes logiques.</span><span class="sxs-lookup"><span data-stu-id="74568-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="74568-123">La bibliothèque est décrite et utilisée dans le *Guide de programmation OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="74568-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="74568-124">Fonctions WGL</span><span class="sxs-lookup"><span data-stu-id="74568-124">The WGL functions</span></span>

    <span data-ttu-id="74568-125">Cet ensemble de fonctions connecte OpenGL au système de fenêtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="74568-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="74568-126">Les fonctions gèrent les contextes de rendu, les listes d’affichage, les fonctions d’extension et les bitmaps de police.</span><span class="sxs-lookup"><span data-stu-id="74568-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="74568-127">Les fonctions WGL sont analogues aux extensions GLX qui connectent OpenGL au système de fenêtres X.</span><span class="sxs-lookup"><span data-stu-id="74568-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="74568-128">Les noms de ces fonctions ont un préfixe « WGL ».</span><span class="sxs-lookup"><span data-stu-id="74568-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="74568-129">Nouvelles fonctions Windows pour les formats de pixel et la double mise en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="74568-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="74568-130">Ces fonctions prennent en charge les formats de pixel par fenêtre et la double mise en mémoire tampon (pour les modifications d’images lisses) de Windows.</span><span class="sxs-lookup"><span data-stu-id="74568-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="74568-131">Ces nouvelles fonctions s’appliquent uniquement aux fenêtres graphiques OpenGL.</span><span class="sxs-lookup"><span data-stu-id="74568-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




