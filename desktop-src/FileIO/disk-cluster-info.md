---
description: Représente les informations conservées sur le gestionnaire de partition sur un disque qui fait partie d’un cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Structure DISK_CLUSTER_INFO (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545819"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="2e256-103">Structure des informations de \_ cluster de disque \_</span><span class="sxs-lookup"><span data-stu-id="2e256-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="2e256-104">Représente les informations conservées sur le gestionnaire de partition sur un disque qui fait partie d’un cluster.</span><span class="sxs-lookup"><span data-stu-id="2e256-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e256-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e256-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="2e256-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2e256-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e256-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="2e256-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2e256-108">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="2e256-108">The version number.</span></span> <span data-ttu-id="2e256-109">Cette valeur doit être définie sur la taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="2e256-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e256-110">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="2e256-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2e256-111">Combinaison d’indicateurs liés aux disques et aux clusters.</span><span class="sxs-lookup"><span data-stu-id="2e256-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="2e256-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e256-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="2e256-113">Signification</span><span class="sxs-lookup"><span data-stu-id="2e256-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="2e256-114"><dt>**Disque \_ Indicateur de CLUSTER \_ \_ activé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e256-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="2e256-115">Le disque est utilisé dans le cadre du service de cluster.</span><span class="sxs-lookup"><span data-stu-id="2e256-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="2e256-116"><dt>**Disque \_ Indicateur de CLUSTER \_ \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e256-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="2e256-117">Les volumes sur le disque sont exposés par CSVFS sur tous les nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="2e256-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="2e256-118"><dt>**Disque \_ \_Indicateur \_ de cluster dans la \_ maintenance**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2e256-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="2e256-119">La ressource de cluster associée à ce disque est en mode maintenance.</span><span class="sxs-lookup"><span data-stu-id="2e256-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="2e256-120"><dt>**Disque \_ Indicateur de CLUSTER d' \_ \_ \_ arrivée PNP \_ terminé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2e256-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="2e256-121">Le pilote de disque en cluster pour le mode noyau (ClusDisk) a reçu une notification PnP de l’arrivée du disque.</span><span class="sxs-lookup"><span data-stu-id="2e256-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e256-122">**FlagsMask**</span><span class="sxs-lookup"><span data-stu-id="2e256-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="2e256-123">Indicateurs qui sont modifiés dans le membre **Flags** .</span><span class="sxs-lookup"><span data-stu-id="2e256-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="2e256-124">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="2e256-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="2e256-125">**True** pour envoyer une notification de modification de la disposition ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2e256-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e256-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e256-126">Requirements</span></span>



| <span data-ttu-id="2e256-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e256-127">Requirement</span></span> | <span data-ttu-id="2e256-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e256-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e256-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e256-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e256-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e256-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="2e256-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e256-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e256-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e256-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e256-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e256-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e256-134"><dt>NTDDDISK. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e256-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e256-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e256-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e256-136">Structures de gestion des disques</span><span class="sxs-lookup"><span data-stu-id="2e256-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="2e256-137">**\_informations de \_ cluster d’extraction de disque IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e256-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="2e256-138">**\_informations de \_ cluster d’ensemble de disques IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e256-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




