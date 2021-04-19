---
title: Guide de programmation du SDK Windows Media format
description: Guide de programmation du SDK Windows Media format
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- Windows Media Format SDK, Guide de programmation
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), Guide de programmation
- ASF (format des systèmes avancés), Guide de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511116"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="767bb-107">Guide de programmation du SDK Windows Media format</span><span class="sxs-lookup"><span data-stu-id="767bb-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="767bb-108">Le Guide de programmation est destiné à vous aider à apprendre à utiliser le kit de développement logiciel (SDK) Microsoft Windows Media format pour créer des applications qui fonctionnent avec des fichiers à l’aide du format ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="767bb-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="767bb-109">Vous pouvez utiliser le kit de développement logiciel (SDK) Windows Media format pour créer des applications qui écrivent des flux multimédias numériques dans des fichiers ASF et les lisent.</span><span class="sxs-lookup"><span data-stu-id="767bb-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="767bb-110">Ce kit de développement logiciel prend également en charge la modification des métadonnées dans les fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="767bb-111">En outre, ce kit de développement logiciel (SDK) peut être utilisé pour lire et manipuler les métadonnées dans les fichiers MP3.</span><span class="sxs-lookup"><span data-stu-id="767bb-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="767bb-112">Les sections suivantes expliquent en détail les étapes requises pour écrire, lire et modifier des fichiers ASF à l’aide de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="767bb-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="767bb-113">Section</span><span class="sxs-lookup"><span data-stu-id="767bb-113">Section</span></span>                                                                            | <span data-ttu-id="767bb-114">Description</span><span class="sxs-lookup"><span data-stu-id="767bb-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="767bb-115">Prise en main</span><span class="sxs-lookup"><span data-stu-id="767bb-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="767bb-116">Fournit des informations générales sur la préparation à l’utilisation de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="767bb-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="767bb-117">Utilisation des méthodes de rappel</span><span class="sxs-lookup"><span data-stu-id="767bb-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="767bb-118">Décrit les méthodes de rappel utilisées dans de nombreuses tâches différentes.</span><span class="sxs-lookup"><span data-stu-id="767bb-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="767bb-119">Utilisation des profils</span><span class="sxs-lookup"><span data-stu-id="767bb-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="767bb-120">Décrit comment utiliser, modifier et créer des profils.</span><span class="sxs-lookup"><span data-stu-id="767bb-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="767bb-121">Écriture de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="767bb-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="767bb-122">Décrit comment utiliser l’objet Writer pour créer des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="767bb-123">Lecture des fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="767bb-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="767bb-124">Décrit comment recevoir du contenu à partir de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="767bb-125">Utilisation des métadonnées</span><span class="sxs-lookup"><span data-stu-id="767bb-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="767bb-126">Décrit comment gérer le contenu de la section d’en-tête d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="767bb-127">Utilisation des index</span><span class="sxs-lookup"><span data-stu-id="767bb-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="767bb-128">Décrit comment utiliser des index.</span><span class="sxs-lookup"><span data-stu-id="767bb-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="767bb-129">Utilisation des profils</span><span class="sxs-lookup"><span data-stu-id="767bb-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="767bb-130">Décrit comment utiliser, modifier et créer des profils.</span><span class="sxs-lookup"><span data-stu-id="767bb-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="767bb-131">Utilisation des commandes de script</span><span class="sxs-lookup"><span data-stu-id="767bb-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="767bb-132">Décrit comment utiliser des commandes de script dans vos fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="767bb-133">Copie de données d’un fichier vers un autre</span><span class="sxs-lookup"><span data-stu-id="767bb-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="767bb-134">Décrit comment copier des données d’un fichier ASF vers un autre, sans décodage ni encodage.</span><span class="sxs-lookup"><span data-stu-id="767bb-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="767bb-135">Activation de la prise en charge de DRM</span><span class="sxs-lookup"><span data-stu-id="767bb-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="767bb-136">Décrit comment activer la prise en charge de la lecture de fichiers ASF protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="767bb-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="767bb-137">Implémentation des fonctionnalités réseau</span><span class="sxs-lookup"><span data-stu-id="767bb-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="767bb-138">Décrit l’utilisation de ce kit de développement logiciel (SDK) pour effectuer les opérations réseau qui sont essentielles au succès de la diffusion de médias.</span><span class="sxs-lookup"><span data-stu-id="767bb-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="767bb-139">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="767bb-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="767bb-140">Décrit comment utiliser certaines fonctionnalités avancées de ce kit de développement logiciel (SDK) dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="767bb-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="767bb-141">DirectShow et Windows Media</span><span class="sxs-lookup"><span data-stu-id="767bb-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="767bb-142">Décrit comment vous pouvez utiliser Microsoft DirectShow pour créer et lire des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="767bb-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="767bb-143">Considérations relatives aux projets</span><span class="sxs-lookup"><span data-stu-id="767bb-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="767bb-144">Fournit des détails sur la finalisation et la distribution de vos applications.</span><span class="sxs-lookup"><span data-stu-id="767bb-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="767bb-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="767bb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="767bb-146">**À propos du kit de développement logiciel (SDK) Windows Media format**</span><span class="sxs-lookup"><span data-stu-id="767bb-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="767bb-147">**SDK Windows Media format 11**</span><span class="sxs-lookup"><span data-stu-id="767bb-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




