---
title: Formats d’interruption
description: Le format des PDU d’interruption est différent de celui des autres PDU. Le format des interruptions SNMPv1 et SNMPv2C est également différent.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028865"
---
# <a name="trap-formats"></a><span data-ttu-id="79b86-104">Formats d’interruption</span><span class="sxs-lookup"><span data-stu-id="79b86-104">Trap Formats</span></span>

<span data-ttu-id="79b86-105">Le format des PDU d’interruption est différent de celui des autres PDU.</span><span class="sxs-lookup"><span data-stu-id="79b86-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="79b86-106">Le format des interruptions SNMPv1 et SNMPv2C est également différent.</span><span class="sxs-lookup"><span data-stu-id="79b86-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="79b86-107">Dans l’infrastructure SNMPv2C, le format de l’interruption de la PDU est une liste de liaison variable de *n* entrées de liaison de variable organisées de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="79b86-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="79b86-108">La première entrée de liaison de variable contient un horodatage.</span><span class="sxs-lookup"><span data-stu-id="79b86-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="79b86-109">La deuxième entrée de liaison de variable est un identificateur d’objet qui identifie l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="79b86-110">Les troisième et *n* entrées de liaison de variable, le cas échéant, contiennent des informations supplémentaires associées à l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="79b86-111">Dans le cadre de l’infrastructure SNMPv1, le format d’interruption de la PDU est le suivant.</span><span class="sxs-lookup"><span data-stu-id="79b86-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="79b86-112">Champ</span><span class="sxs-lookup"><span data-stu-id="79b86-112">Field</span></span>                      | <span data-ttu-id="79b86-113">Description</span><span class="sxs-lookup"><span data-stu-id="79b86-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="79b86-114">enterprise</span><span class="sxs-lookup"><span data-stu-id="79b86-114">enterprise</span></span>                 | <span data-ttu-id="79b86-115">Identifie le type d’appareil qui a généré l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="79b86-116">ADR de l’agent</span><span class="sxs-lookup"><span data-stu-id="79b86-116">agent-addr</span></span>                 | <span data-ttu-id="79b86-117">Identifie l’adresse IP de l’appareil qui a généré l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="79b86-118">interruption générique/d’interruption spécifique</span><span class="sxs-lookup"><span data-stu-id="79b86-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="79b86-119">Identifie un type d’interruption prédéfini.</span><span class="sxs-lookup"><span data-stu-id="79b86-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="79b86-120">horodatage</span><span class="sxs-lookup"><span data-stu-id="79b86-120">time-stamp</span></span>                 | <span data-ttu-id="79b86-121">Identifie le moment où l’interruption a été générée.</span><span class="sxs-lookup"><span data-stu-id="79b86-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="79b86-122">liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="79b86-122">variable-bindings</span></span>          | <span data-ttu-id="79b86-123">Contient des informations supplémentaires associées à l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="79b86-124">La fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) retourne toujours un message au format SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="79b86-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="79b86-125">Si le message contient le type d' **opération \_ \_ interruption PDU SNMP**, l’application peut lire les entrées de liaison de variable du message et récupérer les informations associées à l’interruption.</span><span class="sxs-lookup"><span data-stu-id="79b86-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 




