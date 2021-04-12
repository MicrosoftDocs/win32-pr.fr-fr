---
title: Modification des flux
description: Modification des flux
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream fonction)
- EditStreamCut fonction)
- EditStreamCopy fonction)
- EditStreamPaste fonction)
- EditStreamClone fonction)
- EditStreamSetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462318"
---
# <a name="editing-streams"></a><span data-ttu-id="19174-109">Modification des flux</span><span class="sxs-lookup"><span data-stu-id="19174-109">Editing Streams</span></span>

<span data-ttu-id="19174-110">Vous pouvez créer un flux que vous pouvez modifier à l’aide de la fonction [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) .</span><span class="sxs-lookup"><span data-stu-id="19174-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="19174-111">Cette fonction initialise l’environnement pour la modification d’un flux.</span><span class="sxs-lookup"><span data-stu-id="19174-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="19174-112">Cela comprend la création d’une interface pour le nouveau flux et les tables de modification internes qui effectuent le suivi des modifications apportées au flux.</span><span class="sxs-lookup"><span data-stu-id="19174-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="19174-113">**CreateEditableStream** retourne un pointeur de flux vers un flux modifiable requis par d’autres fonctions de modification de flux.</span><span class="sxs-lookup"><span data-stu-id="19174-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="19174-114">Le pointeur de flux modifiable peut également être utilisé par d’autres fonctions AVIFile qui acceptent des pointeurs de flux.</span><span class="sxs-lookup"><span data-stu-id="19174-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="19174-115">Vous pouvez couper un ou plusieurs échantillons d’un flux modifiable à l’aide de la fonction [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) .</span><span class="sxs-lookup"><span data-stu-id="19174-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="19174-116">Pour supprimer des exemples du flux modifiable, cette fonction ajoute une entrée à la table de modification.</span><span class="sxs-lookup"><span data-stu-id="19174-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="19174-117">La fonction place ensuite une copie des exemples coupés dans un nouveau flux temporaire dont le pointeur d’interface est retourné dans une variable.</span><span class="sxs-lookup"><span data-stu-id="19174-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="19174-118">Vous pouvez copier un ou plusieurs échantillons d’un flux modifiable dans un flux temporaire à l’aide de la fonction [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) .</span><span class="sxs-lookup"><span data-stu-id="19174-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="19174-119">**EditStreamCopy** place des copies des exemples dans un nouveau flux temporaire dont le pointeur d’interface est retourné dans une variable.</span><span class="sxs-lookup"><span data-stu-id="19174-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="19174-120">Vous pouvez copier un ou plusieurs échantillons à partir d’un flux et les coller dans un flux modifiable à l’aide de la fonction [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) .</span><span class="sxs-lookup"><span data-stu-id="19174-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="19174-121">Pour insérer les exemples à la position spécifiée, cette fonction ajoute une entrée dans la table de modification du flux modifiable cible.</span><span class="sxs-lookup"><span data-stu-id="19174-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="19174-122">Vous pouvez dupliquer un flux modifiable à l’aide de la fonction [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) .</span><span class="sxs-lookup"><span data-stu-id="19174-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="19174-123">Cette fonction retourne un pointeur vers l’interface de flux du nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="19174-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="19174-124">Vous pouvez copier ces flux dans le presse-papiers ou les utiliser pour conserver une trace des modifications apportées à un flux.</span><span class="sxs-lookup"><span data-stu-id="19174-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="19174-125">Vous pouvez modifier plusieurs caractéristiques d’un flux modifiable à l’aide de la fonction [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) .</span><span class="sxs-lookup"><span data-stu-id="19174-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="19174-126">Cette fonction met à jour le paramètre de priorité, la langue, l’échelle et le taux, l’heure de début, le paramètre de qualité, les dimensions et les coordonnées du rectangle de destination, ainsi que la description textuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="19174-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="19174-127">Ces éléments sont stockés dans la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associée au flux modifiable.</span><span class="sxs-lookup"><span data-stu-id="19174-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="19174-128">Vous pouvez également modifier la description textuelle d’un flux modifiable à l’aide de la fonction [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) .</span><span class="sxs-lookup"><span data-stu-id="19174-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="19174-129">Cette fonction met à jour le membre **szName** de la structure **AVISTREAMINFO** associée au flux modifiable.</span><span class="sxs-lookup"><span data-stu-id="19174-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="19174-130">Les fonctions d’édition fonctionnent sur les flux.</span><span class="sxs-lookup"><span data-stu-id="19174-130">The editing functions work on streams.</span></span> <span data-ttu-id="19174-131">Vous devez couper et coller chaque flux individuellement, puis utiliser la fonction [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) pour créer un nouveau pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="19174-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="19174-132">La modification des tables dans un flux modifiable conserve toutes les modifications apportées à un flux.</span><span class="sxs-lookup"><span data-stu-id="19174-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="19174-133">Le flux source n’est jamais modifié.</span><span class="sxs-lookup"><span data-stu-id="19174-133">The source stream is never changed.</span></span>

 

 

 




