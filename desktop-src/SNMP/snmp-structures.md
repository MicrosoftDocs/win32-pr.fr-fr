---
title: Structures SNMP
description: Le tableau suivant répertorie les structures utilisées avec SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de structures SNMP
- Structures SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382612"
---
# <a name="snmp-structures"></a><span data-ttu-id="1043a-105">Structures SNMP</span><span class="sxs-lookup"><span data-stu-id="1043a-105">SNMP Structures</span></span>

<span data-ttu-id="1043a-106">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1043a-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1043a-107">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1043a-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1043a-108">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="1043a-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="1043a-109">Le tableau suivant répertorie les structures utilisées avec SNMP.</span><span class="sxs-lookup"><span data-stu-id="1043a-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="1043a-110">Structure SNMP</span><span class="sxs-lookup"><span data-stu-id="1043a-110">SNMP Structure</span></span>                                         | <span data-ttu-id="1043a-111">Description</span><span class="sxs-lookup"><span data-stu-id="1043a-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1043a-112">**AsnAny**</span><span class="sxs-lookup"><span data-stu-id="1043a-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="1043a-113">Décrit le type et la valeur d’une variable SNMP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1043a-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="1043a-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1043a-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="1043a-115">Contient un compteur 64 bits qui est spécifié par deux valeurs décrivant ses bits de poids faible et de poids fort.</span><span class="sxs-lookup"><span data-stu-id="1043a-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="1043a-116">**AsnObjectIdentifier**</span><span class="sxs-lookup"><span data-stu-id="1043a-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="1043a-117">Décrit un identificateur d’objet (OID).</span><span class="sxs-lookup"><span data-stu-id="1043a-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="1043a-118">**AsnOctetString**</span><span class="sxs-lookup"><span data-stu-id="1043a-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="1043a-119">Représente une chaîne d’octets, généralement en valeurs d’octets.</span><span class="sxs-lookup"><span data-stu-id="1043a-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="1043a-120">**SnmpVarBind**</span><span class="sxs-lookup"><span data-stu-id="1043a-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="1043a-121">Décrit une liaison de variable SNMP.</span><span class="sxs-lookup"><span data-stu-id="1043a-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="1043a-122">**SnmpVarBindList**</span><span class="sxs-lookup"><span data-stu-id="1043a-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="1043a-123">Contient une liste de liaisons de variable SNMP.</span><span class="sxs-lookup"><span data-stu-id="1043a-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 