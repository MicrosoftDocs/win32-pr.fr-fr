---
description: Les lecteurs sont des appareils standard dans un système de carte à puce. Ils sont contrôlés par des pilotes et sont introduits et supprimés du système via Plug-and-Play ou via l’élément périphériques du panneau de configuration.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lecteurs de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523347"
---
# <a name="smart-card-readers"></a><span data-ttu-id="c3605-104">Lecteurs de carte à puce</span><span class="sxs-lookup"><span data-stu-id="c3605-104">Smart Card Readers</span></span>

<span data-ttu-id="c3605-105">Les lecteurs sont des appareils standard dans un système de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c3605-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="c3605-106">Ils sont contrôlés par des pilotes et sont introduits et supprimés du système via Plug-and-Play ou via l’élément périphériques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="c3605-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="c3605-107">Chaque lecteur doit être défini pour être utilisé par le [*sous-système de carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3605-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c3605-108">Le sous-système n’est pas responsable des lecteurs qui ne lui sont pas spécifiquement attribués.</span><span class="sxs-lookup"><span data-stu-id="c3605-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="c3605-109">Les lecteurs de carte à puce peuvent être divisés en groupes logiques appelés groupes de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="c3605-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="c3605-110">Ces groupes peuvent être définis par le sous-système, ainsi que par les administrateurs et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c3605-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="c3605-111">Un lecteur peut appartenir à plusieurs groupes de lecteurs</span><span class="sxs-lookup"><span data-stu-id="c3605-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="c3605-112">Le sous-système de carte à puce définit les groupes suivants.</span><span class="sxs-lookup"><span data-stu-id="c3605-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="c3605-113">Groupe</span><span class="sxs-lookup"><span data-stu-id="c3605-113">Group</span></span>                | <span data-ttu-id="c3605-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3605-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3605-115">Cicatrice $ AllReaders</span><span class="sxs-lookup"><span data-stu-id="c3605-115">SCard$AllReaders</span></span>     | <span data-ttu-id="c3605-116">Ce groupe contient tous les lecteurs du système.</span><span class="sxs-lookup"><span data-stu-id="c3605-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="c3605-117">Un nouveau lecteur donné au sous-système de la carte à puce est automatiquement inclus dans le groupe de lecteurs à l’ensemble du système, à raison d’un cicatrice $ AllReaders.</span><span class="sxs-lookup"><span data-stu-id="c3605-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="c3605-118">Cicatrice $ DefaultReaders</span><span class="sxs-lookup"><span data-stu-id="c3605-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="c3605-119">Ce groupe par défaut, un pour chaque [*Terminal*](../secgloss/t-gly.md), contient tous les lecteurs attribués au terminal et qui ne sont pas réservés à une utilisation spécifique.</span><span class="sxs-lookup"><span data-stu-id="c3605-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
