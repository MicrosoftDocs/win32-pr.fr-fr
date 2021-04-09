---
title: Jeu de commandes VCR
description: Jeu de commandes VCR
ms.assetid: e17ec75d-a98f-46ea-8bef-7e45e1696f43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6f84b4542b6ea87b5d05ae8d1cda2374fcac2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101541"
---
# <a name="vcr-command-set"></a><span data-ttu-id="e999d-103">Jeu de commandes VCR</span><span class="sxs-lookup"><span data-stu-id="e999d-103">VCR Command Set</span></span>

<span data-ttu-id="e999d-104">Les magnétoscopes prennent en charge l’ensemble de commandes suivant.</span><span class="sxs-lookup"><span data-stu-id="e999d-104">VCRs support the following set of commands.</span></span>



| <span data-ttu-id="e999d-105">Forme de chaîne</span><span class="sxs-lookup"><span data-stu-id="e999d-105">String form</span></span>                        | <span data-ttu-id="e999d-106">Formulaire de message</span><span class="sxs-lookup"><span data-stu-id="e999d-106">Message form</span></span>                                |
|------------------------------------|---------------------------------------------|
| [<span data-ttu-id="e999d-107">**saut**</span><span class="sxs-lookup"><span data-stu-id="e999d-107">**break**</span></span>](break.md)             | [<span data-ttu-id="e999d-108">**\_Pause MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-108">**MCI\_BREAK**</span></span>](mci-break.md)             |
| [<span data-ttu-id="e999d-109">**Faculté**</span><span class="sxs-lookup"><span data-stu-id="e999d-109">**capability**</span></span>](capability.md)   | [<span data-ttu-id="e999d-110">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-110">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)   |
| [<span data-ttu-id="e999d-111">**signal**</span><span class="sxs-lookup"><span data-stu-id="e999d-111">**cue**</span></span>](cue.md)                 | [<span data-ttu-id="e999d-112">**\_signal MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-112">**MCI\_CUE**</span></span>](mci-cue.md)                 |
| [<span data-ttu-id="e999d-113">**antigel**</span><span class="sxs-lookup"><span data-stu-id="e999d-113">**freeze**</span></span>](freeze.md)           | [<span data-ttu-id="e999d-114">**\_blocage MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-114">**MCI\_FREEZE**</span></span>](mci-freeze.md)           |
| [<span data-ttu-id="e999d-115">**évaluer**</span><span class="sxs-lookup"><span data-stu-id="e999d-115">**index**</span></span>](./windows-multimedia-start-page.md)             | [<span data-ttu-id="e999d-116">**\_index MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-116">**MCI\_INDEX**</span></span>](mci-index.md)             |
| [<span data-ttu-id="e999d-117">**méta**</span><span class="sxs-lookup"><span data-stu-id="e999d-117">**info**</span></span>](info.md)               | [<span data-ttu-id="e999d-118">**\_infos MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-118">**MCI\_INFO**</span></span>](mci-info.md)               |
| [<span data-ttu-id="e999d-119">**tarifs**</span><span class="sxs-lookup"><span data-stu-id="e999d-119">**list**</span></span>](list.md)               | [<span data-ttu-id="e999d-120">**\_liste MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-120">**MCI\_LIST**</span></span>](mci-list.md)               |
| [<span data-ttu-id="e999d-121">**marque**</span><span class="sxs-lookup"><span data-stu-id="e999d-121">**mark**</span></span>](mark.md)               | [<span data-ttu-id="e999d-122">**\_marque MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-122">**MCI\_MARK**</span></span>](mci-mark.md)               |
| [<span data-ttu-id="e999d-123">**suspen**</span><span class="sxs-lookup"><span data-stu-id="e999d-123">**pause**</span></span>](pause.md)             | [<span data-ttu-id="e999d-124">**\_Pause MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-124">**MCI\_PAUSE**</span></span>](mci-pause.md)             |
| [<span data-ttu-id="e999d-125">**répétition**</span><span class="sxs-lookup"><span data-stu-id="e999d-125">**play**</span></span>](play.md)               | [<span data-ttu-id="e999d-126">**\_lecture MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-126">**MCI\_PLAY**</span></span>](mci-play.md)               |
| [<span data-ttu-id="e999d-127">**enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e999d-127">**record**</span></span>](record.md)           | [<span data-ttu-id="e999d-128">**\_enregistrement MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-128">**MCI\_RECORD**</span></span>](mci-record.md)           |
| [<span data-ttu-id="e999d-129">**sort**</span><span class="sxs-lookup"><span data-stu-id="e999d-129">**resume**</span></span>](resume.md)           | [<span data-ttu-id="e999d-130">**\_reprise MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-130">**MCI\_RESUME**</span></span>](mci-resume.md)           |
| [<span data-ttu-id="e999d-131">**Demandez**</span><span class="sxs-lookup"><span data-stu-id="e999d-131">**seek**</span></span>](seek.md)               | [<span data-ttu-id="e999d-132">**\_recherche MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-132">**MCI\_SEEK**</span></span>](mci-seek.md)               |
| [<span data-ttu-id="e999d-133">**définie**</span><span class="sxs-lookup"><span data-stu-id="e999d-133">**set**</span></span>](set.md)                 | [<span data-ttu-id="e999d-134">**jeu de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e999d-134">**MCI\_SET**</span></span>](mci-set.md)                 |
| [<span data-ttu-id="e999d-135">**setaudio**</span><span class="sxs-lookup"><span data-stu-id="e999d-135">**setaudio**</span></span>](setaudio.md)       | [<span data-ttu-id="e999d-136">**\_SETAUDIO MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-136">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)       |
| [<span data-ttu-id="e999d-137">**settimecode**</span><span class="sxs-lookup"><span data-stu-id="e999d-137">**settimecode**</span></span>](settimecode.md) | [<span data-ttu-id="e999d-138">**\_SETTIMECODE MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-138">**MCI\_SETTIMECODE**</span></span>](mci-settimecode.md) |
| [<span data-ttu-id="e999d-139">**settuner**</span><span class="sxs-lookup"><span data-stu-id="e999d-139">**settuner**</span></span>](settuner.md)       | [<span data-ttu-id="e999d-140">**\_SETTUNER MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-140">**MCI\_SETTUNER**</span></span>](mci-settuner.md)       |
| [<span data-ttu-id="e999d-141">**setvideo**</span><span class="sxs-lookup"><span data-stu-id="e999d-141">**setvideo**</span></span>](setvideo.md)       | [<span data-ttu-id="e999d-142">**\_SETVIDEO MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-142">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)       |
| [<span data-ttu-id="e999d-143">**status**</span><span class="sxs-lookup"><span data-stu-id="e999d-143">**status**</span></span>](status.md)           | [<span data-ttu-id="e999d-144">**\_État MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-144">**MCI\_STATUS**</span></span>](mci-status.md)           |
| [<span data-ttu-id="e999d-145">**première**</span><span class="sxs-lookup"><span data-stu-id="e999d-145">**step**</span></span>](step.md)               | [<span data-ttu-id="e999d-146">**\_étape MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-146">**MCI\_STEP**</span></span>](mci-step.md)               |
| [<span data-ttu-id="e999d-147">**erreur**</span><span class="sxs-lookup"><span data-stu-id="e999d-147">**stop**</span></span>](stop.md)               | [<span data-ttu-id="e999d-148">**\_arrêt MCI**</span><span class="sxs-lookup"><span data-stu-id="e999d-148">**MCI\_STOP**</span></span>](mci-stop.md)               |
| [<span data-ttu-id="e999d-149">sysinfo</span><span class="sxs-lookup"><span data-stu-id="e999d-149">sysinfo</span></span>](sysinfo.md)             | [<span data-ttu-id="e999d-150">**MCI \_ sysinfo**</span><span class="sxs-lookup"><span data-stu-id="e999d-150">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)         |
| [<span data-ttu-id="e999d-151">**libérer**</span><span class="sxs-lookup"><span data-stu-id="e999d-151">**unfreeze**</span></span>](unfreeze.md)       | [<span data-ttu-id="e999d-152">**MCI- \_ libérer**</span><span class="sxs-lookup"><span data-stu-id="e999d-152">**MCI\_UNFREEZE**</span></span>](mci-unfreeze.md)       |



 

 

 