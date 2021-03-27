---
description: La classe HWConfig est la classe parente pour les événements de configuration matérielle sur Windows XP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868918"
---
# <a name="hwconfig-class"></a><span data-ttu-id="977b8-104">HWConfig, classe</span><span class="sxs-lookup"><span data-stu-id="977b8-104">HWConfig class</span></span>

<span data-ttu-id="977b8-105">La classe **HWConfig** est la classe parente pour les événements de configuration matérielle sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="977b8-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="977b8-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="977b8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="977b8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="977b8-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="977b8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="977b8-108">Members</span></span>

<span data-ttu-id="977b8-109">La classe **HWConfig** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="977b8-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="977b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="977b8-110">Remarks</span></span>

<span data-ttu-id="977b8-111">Ces événements fournissent la configuration matérielle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="977b8-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="977b8-112">Contrairement aux autres événements de journalisation de noyau NT, la session de noyau génère automatiquement des événements de configuration matérielle. vous n’activez pas ces événements lors du démarrage de la session du journal de noyau NT.</span><span class="sxs-lookup"><span data-stu-id="977b8-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="977b8-113">**Windows 2000 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="977b8-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="977b8-114">Pour les événements de configuration matérielle sur Windows Vista et Windows Server 2003, consultez la classe [SystemConfig](systemconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="977b8-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="977b8-115">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de configuration matérielle en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="977b8-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="977b8-116">Utilisez les types d’événements suivants pour identifier l’événement de configuration matérielle réel lors de l’utilisation d’événements.</span><span class="sxs-lookup"><span data-stu-id="977b8-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="977b8-117">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="977b8-117">Event type</span></span>                                                                      | <span data-ttu-id="977b8-118">Description</span><span class="sxs-lookup"><span data-stu-id="977b8-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="977b8-119">**Événement \_ \_ \_ Configuration \_ du type de suivi processeur**(la valeur du type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="977b8-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="977b8-120">Événement de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="977b8-120">CPU configuration event.</span></span> <span data-ttu-id="977b8-121">Les classes MOF de l' [**\_ UC HWConfig**](hwconfig-cpu.md) définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="977b8-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="977b8-122">**Événement \_ \_Type de \_ trace \_ disque logique**(la valeur du type d’événement est 12)</span><span class="sxs-lookup"><span data-stu-id="977b8-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="977b8-123">Événement de configuration de disque logique.</span><span class="sxs-lookup"><span data-stu-id="977b8-123">Logical disk configuration event.</span></span> <span data-ttu-id="977b8-124">La classe MOF des classes MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="977b8-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="977b8-125">**Événement \_ Configuration du type de TRACE \_ \_ \_ carte réseau**(la valeur du type d’événement est 13)</span><span class="sxs-lookup"><span data-stu-id="977b8-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="977b8-126">Événement de configuration de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="977b8-126">NIC configuration event.</span></span> <span data-ttu-id="977b8-127">Les classes HWConfig de la [**\_ carte d’interface réseau de l’interface réseau**](hwconfig-nic.md) définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="977b8-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="977b8-128">**Événement \_ Configuration du type de TRACE \_ \_ \_ PHYSICALDISK**(la valeur du type d’événement est 11)</span><span class="sxs-lookup"><span data-stu-id="977b8-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="977b8-129">Événement de configuration de disque physique.</span><span class="sxs-lookup"><span data-stu-id="977b8-129">Physical disk configuration event.</span></span> <span data-ttu-id="977b8-130">Les classes [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="977b8-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="977b8-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="977b8-131">Requirements</span></span>



| <span data-ttu-id="977b8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="977b8-132">Requirement</span></span> | <span data-ttu-id="977b8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="977b8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="977b8-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="977b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="977b8-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="977b8-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="977b8-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="977b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="977b8-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="977b8-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="977b8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="977b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977b8-139">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="977b8-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="977b8-140">**\_Processeur HWConfig**</span><span class="sxs-lookup"><span data-stu-id="977b8-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="977b8-141">**HWConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="977b8-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="977b8-142">**\_Carte réseau HWConfig**</span><span class="sxs-lookup"><span data-stu-id="977b8-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="977b8-143">**HWConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="977b8-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
