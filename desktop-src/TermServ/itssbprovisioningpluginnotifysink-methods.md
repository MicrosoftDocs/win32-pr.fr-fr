---
title: Méthodes ITsSbProvisioningPluginNotifySink
description: Les interfaces ITsSbProvisioningPluginNotifySink exposent les méthodes suivantes.
ms.assetid: 85215405-298E-4413-A026-509A9FDA171F
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326a3cf0e5bc5adc7ff3cecd8acb9df7601b0c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310413"
---
# <a name="itssbprovisioningpluginnotifysink-methods"></a><span data-ttu-id="2d3b3-103">Méthodes ITsSbProvisioningPluginNotifySink</span><span class="sxs-lookup"><span data-stu-id="2d3b3-103">ITsSbProvisioningPluginNotifySink Methods</span></span>

<span data-ttu-id="2d3b3-104">Les interfaces [**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink) exposent les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-104">The [**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink) interfaces exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2d3b3-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2d3b3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2d3b3-106">**Méthode LockVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-106">**LockVirtualMachine method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-lockvirtualmachine)
</dt> <dd>

<span data-ttu-id="2d3b3-107">Avertit Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) que l’ordinateur virtuel est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-107">Notifies Remote Desktop Connection Broker (RD Connection Broker) that the virtual machine is locked.</span></span>

</dd> <dt>

[<span data-ttu-id="2d3b3-108">**Méthode OnJobCancelled**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-108">**OnJobCancelled method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcancelled)
</dt> <dd>

<span data-ttu-id="2d3b3-109">Indique au service Broker pour les connexions Bureau à distance que le travail est annulé.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-109">Notifies RD Connection Broker that the job is cancelled.</span></span>

</dd> <dt>

[<span data-ttu-id="2d3b3-110">**Méthode OnJobCompleted**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-110">**OnJobCompleted method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcompleted)
</dt> <dd>

<span data-ttu-id="2d3b3-111">Indique au service Broker pour les connexions Bureau à distance que le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-111">Notifies RD Connection Broker that the job is complete.</span></span>

</dd> <dt>

[<span data-ttu-id="2d3b3-112">**Méthode OnJobCreated**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-112">**OnJobCreated method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcreated)
</dt> <dd>

<span data-ttu-id="2d3b3-113">Avertit le Service Broker pour les connexions Bureau à la création d’un travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-113">Notifies RD Connection Broker that a provisioning job is created.</span></span>

</dd> <dt>

[<span data-ttu-id="2d3b3-114">**Méthode OnVirtualMachineHostStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-114">**OnVirtualMachineHostStatusChanged method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onvirtualmachinehoststatuschanged)
</dt> <dd>

<span data-ttu-id="2d3b3-115">Notifie le Service Broker pour les connexions Bureau à distance que l’état de l’hôte d’un ordinateur virtuel est modifié.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-115">Notifies RD Connection Broker that the status of the host of a virtual machine is changed.</span></span>

</dd> <dt>

[<span data-ttu-id="2d3b3-116">**Méthode OnVirtualMachineStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="2d3b3-116">**OnVirtualMachineStatusChanged method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onvirtualmachinestatuschanged)
</dt> <dd>

<span data-ttu-id="2d3b3-117">Notifie le Service Broker pour les connexions Bureau à distance que l’état d’un ordinateur virtuel a été modifié.</span><span class="sxs-lookup"><span data-stu-id="2d3b3-117">Notifies RD Connection Broker that the status of a virtual machine is changed.</span></span>

</dd> </dl>

 

 




