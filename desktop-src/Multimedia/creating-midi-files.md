---
title: Création de fichiers MIDI
description: Création de fichiers MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Multimédia Windows, création de fichiers MIDI
- multimédia, création de fichiers MIDI
- audio multimédia, création de fichiers MIDI
- audio, création de fichiers MIDI
- Interface MIDI (Musical Instrument Digital Interface), création de fichiers
- MIDI (Musical Instrument Digital Interface), création de fichiers
- création de fichiers MIDI, à propos de
- L’Association de fabricants MIDI (MMA)
- MMA (Association de fabricants MIDI)
- Spécification détaillée MIDI
- Spécification des fichiers MIDI standard
- Spécification générale MIDI (GM)
- Spécification GM (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028930"
---
# <a name="creating-midi-files"></a><span data-ttu-id="7de26-116">Création de fichiers MIDI</span><span class="sxs-lookup"><span data-stu-id="7de26-116">Creating MIDI Files</span></span>

<span data-ttu-id="7de26-117">Les spécifications MIDI (Musical Instrument Digital Interface) sont publiées par et sont des documents protégés par des droits d’auteur de l’Association de fabricants MIDI (MMA).</span><span class="sxs-lookup"><span data-stu-id="7de26-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="7de26-118">La liste suivante décrit les spécifications qui présentent le plus grand intérêt général :</span><span class="sxs-lookup"><span data-stu-id="7de26-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="7de26-119">Spécification détaillée MIDI</span><span class="sxs-lookup"><span data-stu-id="7de26-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="7de26-120">La spécification détaillée MIDI explique les protocoles matériels et logiciels MIDI.</span><span class="sxs-lookup"><span data-stu-id="7de26-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="7de26-121">Cela est utile pour les applications de développement multimédia qui implémentent la prise en charge MIDI en utilisant des fonctions MIDI pour enregistrer, modifier et/ou lire des données MIDI.</span><span class="sxs-lookup"><span data-stu-id="7de26-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="7de26-122">Fichiers MIDI standard 1,0</span><span class="sxs-lookup"><span data-stu-id="7de26-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="7de26-123">La spécification de fichiers MIDI standard définit un moyen d’échanger des données MIDI horodatées entre différentes applications sur des plateformes matérielles identiques ou différentes.</span><span class="sxs-lookup"><span data-stu-id="7de26-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="7de26-124">Cela est utile pour les développeurs qui écrivent des applications qui lisent et analysent les fichiers de disque contenant des données MIDI et/ou écrivent des fichiers de données MIDI sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7de26-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="7de26-125">Système MIDI général-niveau 1</span><span class="sxs-lookup"><span data-stu-id="7de26-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="7de26-126">La spécification standard MIDI (GM) définit une configuration MIDI minimale d’un « système MIDI général ».</span><span class="sxs-lookup"><span data-stu-id="7de26-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="7de26-127">Ce système se compose d’une classe spécifique de périphériques de lecture MIDI et présente un intérêt pour les développeurs multimédias qui créent des fichiers MIDI.</span><span class="sxs-lookup"><span data-stu-id="7de26-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="7de26-128">La plupart des cartes son et des synthétiseurs MIDI fabriqués aujourd’hui sont compatibles avec la spécification GM.</span><span class="sxs-lookup"><span data-stu-id="7de26-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="7de26-129">Les fichiers MIDI qui sont créés dans la spécification GM doivent généralement sembler tels qu’ils étaient prévus, quel que soit l’appareil compatible GM sur lequel ils sont lus.</span><span class="sxs-lookup"><span data-stu-id="7de26-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="7de26-130">Pour que les fichiers MIDI soient un format viable pour représenter de la musique dans un environnement informatique multimédia, Windows suit la spécification General MIDI System Level 1.</span><span class="sxs-lookup"><span data-stu-id="7de26-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="7de26-131">Les rubriques suivantes fournissent des instructions de création MIDI supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="7de26-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="7de26-132">Instructions de création pour les fichiers MIDI</span><span class="sxs-lookup"><span data-stu-id="7de26-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="7de26-133">Attributions de correctifs MIDI standard</span><span class="sxs-lookup"><span data-stu-id="7de26-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="7de26-134">Attributions de clés MIDI standard</span><span class="sxs-lookup"><span data-stu-id="7de26-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 




