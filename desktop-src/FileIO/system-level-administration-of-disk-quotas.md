---
description: L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume. L’administrateur peut également définir des quotas par défaut pour le volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administration au niveau du système des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201604"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="dc24e-104">Administration au niveau du système des quotas de disque</span><span class="sxs-lookup"><span data-stu-id="dc24e-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="dc24e-105">L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume.</span><span class="sxs-lookup"><span data-stu-id="dc24e-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="dc24e-106">L’administrateur peut également définir des quotas par défaut pour le volume.</span><span class="sxs-lookup"><span data-stu-id="dc24e-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="dc24e-107">Un nouvel utilisateur sur le volume reçoit le quota par défaut, sauf si l’administrateur a établi un quota spécifique pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc24e-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="dc24e-108">L’administrateur peut interroger le niveau de suivi et d’application du quota (ou les États de quota), les limites de quota par défaut et les informations de quota par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc24e-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="dc24e-109">Les informations de quota par utilisateur contiennent la limite de quota matériel de l’utilisateur, le seuil d’avertissement et l’utilisation du quota.</span><span class="sxs-lookup"><span data-stu-id="dc24e-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="dc24e-110">L’administrateur peut également activer ou désactiver l’application des quotas.</span><span class="sxs-lookup"><span data-stu-id="dc24e-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="dc24e-111">Il existe trois États de quota, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dc24e-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="dc24e-112">State</span><span class="sxs-lookup"><span data-stu-id="dc24e-112">State</span></span>          | <span data-ttu-id="dc24e-113">Description</span><span class="sxs-lookup"><span data-stu-id="dc24e-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc24e-114">Quota désactivé</span><span class="sxs-lookup"><span data-stu-id="dc24e-114">Quota disabled</span></span> | <span data-ttu-id="dc24e-115">Les modifications de l’utilisation du quota ne sont pas suivies, mais les limites de quota ne sont pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="dc24e-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="dc24e-116">Dans cet État, les performances ne sont pas affectées par les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="dc24e-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="dc24e-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dc24e-117">This is the default state.</span></span>                         |
| <span data-ttu-id="dc24e-118">Quota suivi</span><span class="sxs-lookup"><span data-stu-id="dc24e-118">Quota tracked</span></span>  | <span data-ttu-id="dc24e-119">Les modifications de l’utilisation du quota sont suivies, mais les limites de quota ne sont pas appliquées.</span><span class="sxs-lookup"><span data-stu-id="dc24e-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="dc24e-120">Dans cet État, aucun événement de violation de quota n’est généré et aucune opération de fichier ne réussit en raison de violations de quota de disque.</span><span class="sxs-lookup"><span data-stu-id="dc24e-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="dc24e-121">Quota appliqué</span><span class="sxs-lookup"><span data-stu-id="dc24e-121">Quota enforced</span></span> | <span data-ttu-id="dc24e-122">Les modifications de l’utilisation du quota sont suivies et les limites de quota sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="dc24e-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



