---
description: Cette classe est la classe parente pour les événements de configuration matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869289"
---
# <a name="systemconfig-class"></a><span data-ttu-id="8902b-104">SystemConfig, classe</span><span class="sxs-lookup"><span data-stu-id="8902b-104">SystemConfig class</span></span>

<span data-ttu-id="8902b-105">Cette classe est la classe parente pour les événements de configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="8902b-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="8902b-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="8902b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8902b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8902b-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="8902b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8902b-108">Members</span></span>

<span data-ttu-id="8902b-109">La classe **SystemConfig** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="8902b-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8902b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8902b-110">Remarks</span></span>

<span data-ttu-id="8902b-111">Ces événements fournissent la configuration matérielle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8902b-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="8902b-112">Contrairement aux autres événements de journalisation de noyau NT, la session de noyau génère automatiquement des événements de configuration matérielle. vous n’activez pas ces événements lors du démarrage de la session du journal de noyau NT.</span><span class="sxs-lookup"><span data-stu-id="8902b-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="8902b-113">Pour les événements de configuration matérielle sur Windows XP, consultez la classe [HWConfig](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="8902b-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="8902b-114">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de configuration matérielle en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="8902b-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="8902b-115">Utilisez les types d’événements suivants pour identifier l’événement de configuration matérielle réel lors de l’utilisation d’événements.</span><span class="sxs-lookup"><span data-stu-id="8902b-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="8902b-116">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="8902b-116">Event type</span></span>                                                                      | <span data-ttu-id="8902b-117">Description</span><span class="sxs-lookup"><span data-stu-id="8902b-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8902b-118">**Événement \_ \_ \_ Configuration \_ du type de suivi processeur**(la valeur du type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="8902b-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="8902b-119">Événement de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="8902b-119">CPU configuration event.</span></span> <span data-ttu-id="8902b-120">Les classes MOF de l' [**\_ UC SystemConfig**](systemconfig-cpu.md) définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="8902b-121">**Événement \_ Type de TRACE \_ \_ configuration \_ IDECHANNEL**(la valeur type d’événement est 23)</span><span class="sxs-lookup"><span data-stu-id="8902b-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="8902b-122">Événement de configuration de canal IDE principal et secondaire.</span><span class="sxs-lookup"><span data-stu-id="8902b-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="8902b-123">La classe MOF des classes MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8902b-124">**Événement \_ Configuration du type de TRACE \_ \_ \_ IRQ**(la valeur du type d’événement est 21)</span><span class="sxs-lookup"><span data-stu-id="8902b-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="8902b-125">Événement de requête d’interruption (IRQ).</span><span class="sxs-lookup"><span data-stu-id="8902b-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="8902b-126">La classe MOF des classes MOF [**SystemConfig \_ IRQ**](systemconfig-irq.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="8902b-127">**Événement \_ \_Type de \_ trace \_ disque logique**(la valeur du type d’événement est 12)</span><span class="sxs-lookup"><span data-stu-id="8902b-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="8902b-128">Événement de configuration de disque logique.</span><span class="sxs-lookup"><span data-stu-id="8902b-128">Logical disk configuration event.</span></span> <span data-ttu-id="8902b-129">La classe MOF des classes MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="8902b-130">**Événement \_ Configuration du type de TRACE \_ \_ \_ NetInfo**(la valeur du type d’événement est 17)</span><span class="sxs-lookup"><span data-stu-id="8902b-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="8902b-131">Événement réseau iformation.</span><span class="sxs-lookup"><span data-stu-id="8902b-131">Network iformation event.</span></span> <span data-ttu-id="8902b-132">La classe MOF du [**\_ réseau SystemConfig**](systemconfig-network.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="8902b-133">**Événement \_ Configuration du type de TRACE \_ \_ \_ carte réseau**(la valeur du type d’événement est 13)</span><span class="sxs-lookup"><span data-stu-id="8902b-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="8902b-134">Événement de configuration de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8902b-134">NIC configuration event.</span></span> <span data-ttu-id="8902b-135">Les classes SystemConfig de la [**\_ carte d’interface réseau de l’interface réseau**](systemconfig-nic.md) définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="8902b-136">**Événement \_ Configuration du type de TRACE \_ \_ \_ PHYSICALDISK**(la valeur du type d’événement est 11)</span><span class="sxs-lookup"><span data-stu-id="8902b-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="8902b-137">Événement de configuration de disque physique.</span><span class="sxs-lookup"><span data-stu-id="8902b-137">Physical disk configuration event.</span></span> <span data-ttu-id="8902b-138">Les classes [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF définissent les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="8902b-139">**Événement \_ Configuration du type de TRACE \_ \_ \_ PNP**(la valeur du type d’événement est 22)</span><span class="sxs-lookup"><span data-stu-id="8902b-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="8902b-140">Événement Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="8902b-140">Plug and play event.</span></span> <span data-ttu-id="8902b-141">La classe MOF des classes MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="8902b-142">**Événement \_ \_Mise en \_ \_ marche** de la configuration du type de trace (la valeur du type d’événement est 16)</span><span class="sxs-lookup"><span data-stu-id="8902b-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="8902b-143">Événement de configuration de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8902b-143">Power configuration event.</span></span> <span data-ttu-id="8902b-144">La classe [**SystemConfig \_ Power**](systemconfig-power.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="8902b-145">**Événement \_ \_Services de \_ configuration \_ du type de trace**(la valeur du type d’événement est 15)</span><span class="sxs-lookup"><span data-stu-id="8902b-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="8902b-146">Événement de configuration des services.</span><span class="sxs-lookup"><span data-stu-id="8902b-146">Services configuration event.</span></span> <span data-ttu-id="8902b-147">La classe MOF des [**\_ services SystemConfig**](systemconfig-services.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="8902b-148">**Événement \_ \_Vidéo de \_ configuration \_ du type de trace**(la valeur du type d’événement est 14)</span><span class="sxs-lookup"><span data-stu-id="8902b-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="8902b-149">Événement de configuration de la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="8902b-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="8902b-150">La classe MOF [**\_ Video SystemConfig**](systemconfig-video.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8902b-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="8902b-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8902b-151">Requirements</span></span>



| <span data-ttu-id="8902b-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8902b-152">Requirement</span></span> | <span data-ttu-id="8902b-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="8902b-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8902b-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8902b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8902b-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8902b-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8902b-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8902b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8902b-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8902b-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8902b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8902b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8902b-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="8902b-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="8902b-160">**\_Processeur SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="8902b-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="8902b-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="8902b-162">**SystemConfig \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="8902b-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="8902b-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="8902b-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="8902b-164">**\_Réseau SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="8902b-165">**\_Carte réseau SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="8902b-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="8902b-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="8902b-167">**\_PNP SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="8902b-168">**SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="8902b-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="8902b-169">**\_Services SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="8902b-170">**\_Vidéo SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8902b-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="8902b-171">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8902b-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
