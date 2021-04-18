---
title: Modification de la synchronisation de Sequencer
description: Modification de la synchronisation de Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "106520207"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="b92a8-104">Modification de la synchronisation de Sequencer</span><span class="sxs-lookup"><span data-stu-id="b92a8-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="b92a8-105">Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="b92a8-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="b92a8-106">Dans ce document, il existe des références au mot « esclave ».</span><span class="sxs-lookup"><span data-stu-id="b92a8-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="b92a8-107">Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="b92a8-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="b92a8-108">Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="b92a8-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="b92a8-109">Pour des fins de cohérence, ce document contient ce mot.</span><span class="sxs-lookup"><span data-stu-id="b92a8-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="b92a8-110">Lorsque ce mot est supprimé du logiciel, nous allons corriger ce document pour qu’il soit aligné.</span><span class="sxs-lookup"><span data-stu-id="b92a8-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="b92a8-111">Pour modifier le mode de synchronisation d’un périphérique Sequencer, utilisez le message de commande [**\_ Set MCI**](mci-set.md) avec les \_ indicateurs MCI Seq \_ Set \_ Master et MCI \_ Seq \_ Set \_ esclave.</span><span class="sxs-lookup"><span data-stu-id="b92a8-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="b92a8-112">Deux membres de la structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) , **dwMaster** et **dwSlave**, sont utilisés pour spécifier les modes de synchronisation maître et subordonné.</span><span class="sxs-lookup"><span data-stu-id="b92a8-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="b92a8-113">Le mode de synchronisation maître contrôle les informations de synchronisation envoyées par Sequencer à un port de sortie.</span><span class="sxs-lookup"><span data-stu-id="b92a8-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="b92a8-114">Voici les constantes pour le membre **dwMaster** et les modes de synchronisation principaux correspondants.</span><span class="sxs-lookup"><span data-stu-id="b92a8-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="b92a8-115">Constante</span><span class="sxs-lookup"><span data-stu-id="b92a8-115">Constant</span></span>        | <span data-ttu-id="b92a8-116">Mode de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b92a8-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92a8-117">MCI \_ Seq \_ midi</span><span class="sxs-lookup"><span data-stu-id="b92a8-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="b92a8-118">Synchronisation MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-118">MIDI Synchronization.</span></span> <span data-ttu-id="b92a8-119">Envoyer les informations de minutage au port de sortie à l’aide des messages d’horloge de minutage MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="b92a8-120">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="b92a8-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="b92a8-121">Synchronisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="b92a8-121">SMPTE Synchronization.</span></span> <span data-ttu-id="b92a8-122">Envoyer les informations de minutage au port de sortie à l’aide de messages MIDI quart-Frame.</span><span class="sxs-lookup"><span data-stu-id="b92a8-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="b92a8-123">MCI \_ Seq \_ aucun</span><span class="sxs-lookup"><span data-stu-id="b92a8-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="b92a8-124">Aucune synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b92a8-124">No Synchronization.</span></span> <span data-ttu-id="b92a8-125">Ne pas envoyer d’informations de minutage.</span><span class="sxs-lookup"><span data-stu-id="b92a8-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="b92a8-126">Le mode de synchronisation subordonné détermine où Sequencer obtient ses informations de minutage pour lire un fichier MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="b92a8-127">Voici les constantes pour le membre **dwSlave** et les modes de synchronisation subordonnés correspondants.</span><span class="sxs-lookup"><span data-stu-id="b92a8-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="b92a8-128">Constante</span><span class="sxs-lookup"><span data-stu-id="b92a8-128">Constant</span></span>        | <span data-ttu-id="b92a8-129">Mode de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b92a8-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92a8-130">\_fichier séquence \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b92a8-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="b92a8-131">Synchronisation de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b92a8-131">File Synchronization.</span></span> <span data-ttu-id="b92a8-132">Obtient les informations de minutage à partir du fichier MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="b92a8-133">MCI \_ Seq \_ midi</span><span class="sxs-lookup"><span data-stu-id="b92a8-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="b92a8-134">Synchronisation MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-134">MIDI Synchronization.</span></span> <span data-ttu-id="b92a8-135">Obtient les informations de minutage à partir du port d’entrée à l’aide des messages d’horloge de minutage MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="b92a8-136">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="b92a8-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="b92a8-137">Synchronisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="b92a8-137">SMPTE Synchronization.</span></span> <span data-ttu-id="b92a8-138">Obtient les informations de minutage à partir du port d’entrée à l’aide de messages MIDI quart-Frame.</span><span class="sxs-lookup"><span data-stu-id="b92a8-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="b92a8-139">MCI \_ Seq \_ aucun</span><span class="sxs-lookup"><span data-stu-id="b92a8-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="b92a8-140">Aucune synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b92a8-140">No Synchronization.</span></span> <span data-ttu-id="b92a8-141">Récupérez les informations de minutage des commandes MCI uniquement et ignorez les informations de minutage (telles que les changements de tempo) qui se trouvent dans le fichier MIDI.</span><span class="sxs-lookup"><span data-stu-id="b92a8-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="b92a8-142">Actuellement, pour la synchronisation principale, MCI MIDI Sequencer ne prend en charge que le mode sans synchronisation (MCI \_ Seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="b92a8-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="b92a8-143">Pour la synchronisation subordonnée, elle prend en charge uniquement le mode de synchronisation de fichiers ( \_ fichier MCI Seq \_ ) et le mode sans synchronisation (MCI \_ Seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="b92a8-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




