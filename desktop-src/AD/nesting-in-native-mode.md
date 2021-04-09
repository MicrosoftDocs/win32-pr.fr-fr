---
title: Imbrication en mode natif
description: La liste suivante décrit ce qui peut être contenu dans un groupe qui existe dans un domaine en mode natif.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Imbrication dans AD en mode natif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839282"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="2e67a-104">Imbrication en mode natif</span><span class="sxs-lookup"><span data-stu-id="2e67a-104">Nesting in Native Mode</span></span>

<span data-ttu-id="2e67a-105">La liste suivante décrit ce qui peut être contenu dans un groupe qui existe dans un domaine en mode natif.</span><span class="sxs-lookup"><span data-stu-id="2e67a-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="2e67a-106">Cette même liste s’applique également aux groupes de distribution dans les domaines en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="2e67a-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="2e67a-107">L’étendue du groupe détermine ces règles de relation contenant-contenu.</span><span class="sxs-lookup"><span data-stu-id="2e67a-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="2e67a-108">Un groupe universel peut contenir d’autres groupes universels, groupes globaux et comptes issus de n’importe quel domaine de la forêt dans laquelle ce groupe universel réside.</span><span class="sxs-lookup"><span data-stu-id="2e67a-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="2e67a-109">Un groupe global peut contenir d’autres groupes globaux et comptes du même domaine auquel le groupe appartient.</span><span class="sxs-lookup"><span data-stu-id="2e67a-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="2e67a-110">Un groupe global ne peut pas contenir de groupes universels, ni de groupe global ou de compte d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="2e67a-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="2e67a-111">Un groupe de domaine local peut contenir des groupes universels, des groupes globaux et des comptes d’un domaine ou d’une forêt.</span><span class="sxs-lookup"><span data-stu-id="2e67a-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="2e67a-112">Un groupe de domaine local peut également contenir d’autres groupes locaux de domaine du même domaine auquel le groupe appartient.</span><span class="sxs-lookup"><span data-stu-id="2e67a-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="2e67a-113">Un groupe de domaine local ne peut pas contenir d’autres groupes locaux de domaine de n’importe quel autre domaine ou forêt.</span><span class="sxs-lookup"><span data-stu-id="2e67a-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




