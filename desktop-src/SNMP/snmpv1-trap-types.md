---
title: Types d’interruptions SNMPv1 (SNMP. h)
description: Les types d’interruptions SNMPv1 décrivent un ensemble prédéfini de types d’interruptions génériques mis en forme pour être conformes à la norme de l’IPDU de l’interruption SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844326"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="b280b-103">Types d’interruptions SNMPv1</span><span class="sxs-lookup"><span data-stu-id="b280b-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="b280b-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b280b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b280b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b280b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b280b-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b280b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b280b-107">Les types d’interruptions SNMPv1 décrivent un ensemble prédéfini de types d’interruptions génériques mis en forme pour être conformes à la norme de l’IPDU de l’interruption SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="b280b-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="b280b-108">Constante</span><span class="sxs-lookup"><span data-stu-id="b280b-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="b280b-109">Description</span><span class="sxs-lookup"><span data-stu-id="b280b-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="b280b-110"><dt>**\_COLDSTART GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="b280b-111">Indique une interruption de démarrage à froid.</span><span class="sxs-lookup"><span data-stu-id="b280b-111">Indicates a cold start trap.</span></span> <span data-ttu-id="b280b-112">L’agent initialise les entités de protocole sur le mode géré.</span><span class="sxs-lookup"><span data-stu-id="b280b-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="b280b-113">Il peut modifier les objets dans sa vue.</span><span class="sxs-lookup"><span data-stu-id="b280b-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="b280b-114"><dt>**\_WARMSTART GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="b280b-115">Indique une interruption de démarrage à chaud.</span><span class="sxs-lookup"><span data-stu-id="b280b-115">Indicates a warm start trap.</span></span> <span data-ttu-id="b280b-116">L’agent se réinitialise lui-même, mais il ne modifie pas les objets dans sa vue.</span><span class="sxs-lookup"><span data-stu-id="b280b-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="b280b-117"><dt>**\_LINKDOWN GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="b280b-118">Indique une interruption de liaison.</span><span class="sxs-lookup"><span data-stu-id="b280b-118">Indicates a link-down trap.</span></span> <span data-ttu-id="b280b-119">Une interface attachée est passée de l’état actif à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="b280b-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="b280b-120">La première variable de la liste liaisons de variables identifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="b280b-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="b280b-121"><dt>**\_LinkUp GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="b280b-122">Indique une interruption de liaison.</span><span class="sxs-lookup"><span data-stu-id="b280b-122">Indicates a link-up trap.</span></span> <span data-ttu-id="b280b-123">Une interface attachée est passée de l’état de démarrage à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="b280b-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="b280b-124">La première variable de la liste liaisons de variables identifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="b280b-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="b280b-125"><dt>**\_AUTHFAILURE GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="b280b-126">Indique une interruption d’échec d’authentification.</span><span class="sxs-lookup"><span data-stu-id="b280b-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="b280b-127">Une entité SNMP a envoyé un message SNMP, mais son appartenance à une communauté connue a été affirmée.</span><span class="sxs-lookup"><span data-stu-id="b280b-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="b280b-128"><dt>**\_EGPNEIGHLOSS GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="b280b-129">Indique un piège de perte de voisinage EGP.</span><span class="sxs-lookup"><span data-stu-id="b280b-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="b280b-130">Un homologue EGP est passé à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="b280b-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="b280b-131">La première variable de la liste liaisons de variables identifie l’adresse IP de l’homologue EGP.</span><span class="sxs-lookup"><span data-stu-id="b280b-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="b280b-132"><dt>**\_ENTERSPECIFIC GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="b280b-133">Indique une interruption spécifique à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b280b-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="b280b-134">Un événement extraordinaire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="b280b-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="b280b-135">Elle est identifiée dans le paramètre *specificTrap* par une valeur spécifique à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b280b-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="b280b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b280b-136">Requirements</span></span>



| <span data-ttu-id="b280b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b280b-137">Requirement</span></span> | <span data-ttu-id="b280b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b280b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b280b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b280b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b280b-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b280b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b280b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b280b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b280b-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b280b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b280b-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b280b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b280b-144"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b280b-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b280b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b280b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b280b-146">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="b280b-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="b280b-147">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="b280b-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="b280b-148">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="b280b-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

