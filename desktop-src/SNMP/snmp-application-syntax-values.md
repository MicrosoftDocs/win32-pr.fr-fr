---
title: Valeurs de la syntaxe de l’application SNMP (SNMP. h)
description: Les valeurs de syntaxe d’application SNMP sont utilisées par les applications de gestion qui utilisent l’API de gestion SNMP de Microsoft.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103424"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="b61ae-103">Valeurs de la syntaxe de l’application SNMP</span><span class="sxs-lookup"><span data-stu-id="b61ae-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="b61ae-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b61ae-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b61ae-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b61ae-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b61ae-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b61ae-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b61ae-107">Les valeurs de syntaxe d’application SNMP sont utilisées par les applications de gestion qui utilisent l’API de gestion SNMP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b61ae-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="b61ae-108">Constante</span><span class="sxs-lookup"><span data-stu-id="b61ae-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="b61ae-109">Description</span><span class="sxs-lookup"><span data-stu-id="b61ae-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="b61ae-110"><dt>**\_adresse IP ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="b61ae-111">Indique une variable d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="b61ae-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="b61ae-112"><dt>**\_COUNTER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="b61ae-113">Indique une variable de compteur.</span><span class="sxs-lookup"><span data-stu-id="b61ae-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="b61ae-114"><dt>**\_Gauge32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="b61ae-115">Indique une variable de jauge.</span><span class="sxs-lookup"><span data-stu-id="b61ae-115">Indicates a gauge variable.</span></span> <span data-ttu-id="b61ae-116">Cette variable décrit un type Unsigned32 conforme à la norme RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="b61ae-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="b61ae-117"><dt>**\_graduations ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="b61ae-118">Indique une variable graduations.</span><span class="sxs-lookup"><span data-stu-id="b61ae-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="b61ae-119"><dt>**ASN \_ opaque**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="b61ae-120">Indique une variable opaque.</span><span class="sxs-lookup"><span data-stu-id="b61ae-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="b61ae-121"><dt>**\_COUNTER64 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="b61ae-122">Indique une variable de compteur qui augmente jusqu’à ce qu’elle atteigne la valeur maximale (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="b61ae-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="b61ae-123"><dt>**\_UINTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="b61ae-124">Indique une variable de type entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b61ae-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="b61ae-125">Cette variable décrit un type UInteger32 conforme à la norme RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="b61ae-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="b61ae-126"><dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="b61ae-127">Voir ASN \_ gauge32.</span><span class="sxs-lookup"><span data-stu-id="b61ae-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="b61ae-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b61ae-128">Requirements</span></span>



| <span data-ttu-id="b61ae-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b61ae-129">Requirement</span></span> | <span data-ttu-id="b61ae-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b61ae-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b61ae-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b61ae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b61ae-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b61ae-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b61ae-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b61ae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b61ae-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b61ae-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b61ae-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b61ae-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b61ae-136"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61ae-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b61ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61ae-138">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="b61ae-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="b61ae-139">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="b61ae-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="b61ae-140">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="b61ae-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

