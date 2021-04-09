---
description: Définissez l’ensemble d’actions pour le \_ Code de contrôle de gestion des attributs du jeu de données du stockage IOCTL \_ \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861105"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="c84c7-103">ACTION de définition de la \_ gestion des données d’appareil \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c84c7-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="c84c7-104">Les valeurs constantes suivantes représentent l’ensemble des valeurs possibles pour le type d’action de définition de la gestion des données de l’appareil, qui est défini en tant que type **DWORD**. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c84c7-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="c84c7-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="c84c7-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-106">0</span><span class="sxs-lookup"><span data-stu-id="c84c7-106">0</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-107">Aucune action n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="c84c7-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-109">1</span><span class="sxs-lookup"><span data-stu-id="c84c7-109">1</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-110">Une action de suppression est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notification DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="c84c7-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-112">2 \| **DeviceDsmActionFlag non \_ destructif** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="c84c7-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-113">Une action de notification est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-113">A notification action is performed.</span></span> <span data-ttu-id="c84c7-114">Les paramètres se trouvent dans une structure de [**paramètres de notification de DSM d’appareil \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="c84c7-115">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**</span><span class="sxs-lookup"><span data-stu-id="c84c7-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-117">3 \| **DeviceDsmActionFlag non \_ destructif** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="c84c7-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-118">Une action de lecture de déchargement est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-118">An offload read action is performed.</span></span> <span data-ttu-id="c84c7-119">Les paramètres se trouvent dans une structure de [**\_ paramètres de \_ \_ lecture \_ de déchargement de DSM d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="c84c7-120">La sortie se trouve dans une structure de [**\_ sortie de \_ lecture \_ de déchargement de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="c84c7-121">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="c84c7-122">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**</span><span class="sxs-lookup"><span data-stu-id="c84c7-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-124">4</span><span class="sxs-lookup"><span data-stu-id="c84c7-124">4</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-125">Une action d’écriture de déchargement est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-125">An offload write action is performed.</span></span> <span data-ttu-id="c84c7-126">Les paramètres se trouvent dans une structure de [**\_ paramètres d' \_ \_ écriture \_ de déchargement de DSM d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="c84c7-127">La sortie se trouve dans une structure de [**\_ sortie d' \_ écriture \_ de déchargement de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="c84c7-128">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**\_Allocation DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="c84c7-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-130">5 \| **DeviceDsmActionFlag non \_ destructif** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="c84c7-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-131">Une bitmap d’allocation est retournée pour la première plage de jeux de données passée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="c84c7-132">La sortie est dans une structure d' [**\_ \_ \_ \_ \_ État de provisionnement du jeu de données d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) .</span><span class="sxs-lookup"><span data-stu-id="c84c7-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="c84c7-133">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="c84c7-134">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Réparation de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="c84c7-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-136">6 \| **DeviceDsmActionFlag non \_ destructif** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="c84c7-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-137">Une action de réparation est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-137">A repair action is performed.</span></span> <span data-ttu-id="c84c7-138">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="c84c7-139">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Nettoyage DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="c84c7-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-141">7 \| **DeviceDsmActionFlag non \_ destructif** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="c84c7-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-142">Une action de nettoyage est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-142">A scrub action is performed.</span></span> <span data-ttu-id="c84c7-143">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="c84c7-144">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c84c7-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Résilience DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="c84c7-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84c7-146">8 \| **DeviceDsmActionFlag non \_ destructif** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="c84c7-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="c84c7-147">Une action de résilience est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c84c7-147">A resiliency action is performed.</span></span> <span data-ttu-id="c84c7-148">Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.</span><span class="sxs-lookup"><span data-stu-id="c84c7-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="c84c7-149">**Windows 7 et Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c84c7-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c84c7-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c84c7-150">Requirements</span></span>



| <span data-ttu-id="c84c7-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c84c7-151">Requirement</span></span> | <span data-ttu-id="c84c7-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c84c7-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84c7-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c84c7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c84c7-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c84c7-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="c84c7-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c84c7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c84c7-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c84c7-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="c84c7-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="c84c7-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84c7-158"><dt>WinIoCtl. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c84c7-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




