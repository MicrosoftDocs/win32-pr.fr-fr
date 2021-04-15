---
title: Valeurs de type de PDU (SNMP. h)
description: Les valeurs de type de PDU sont utilisées dans le champ type d’unité d’alimentation (PDU) \_ de l’unité d’alimentation pour décrire son type.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466451"
---
# <a name="pdu-type-values"></a><span data-ttu-id="7919a-103">Valeurs de type d’unité d’alimentation</span><span class="sxs-lookup"><span data-stu-id="7919a-103">PDU Type Values</span></span>

<span data-ttu-id="7919a-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7919a-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7919a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7919a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7919a-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="7919a-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7919a-107">Les valeurs de type de PDU sont utilisées dans le champ **\_ type d’unité** d’alimentation (PDU) de l’unité d’alimentation pour décrire son type.</span><span class="sxs-lookup"><span data-stu-id="7919a-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="7919a-108">Constante</span><span class="sxs-lookup"><span data-stu-id="7919a-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="7919a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7919a-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="7919a-110"><dt>**\_récupération du PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="7919a-111">Recherchez et récupérez une valeur d’une variable SNMP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7919a-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="7919a-112"><dt>**\_PDU SNMP \_ GetNext**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="7919a-113">Recherchez et récupérez la valeur d’une variable SNMP sans connaître le nom exact de la variable.</span><span class="sxs-lookup"><span data-stu-id="7919a-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="7919a-114"><dt>**\_réponse PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="7919a-115">Répondez à une \_ demande d’alimentation de PDU SNMP \_ ou à une \_ demande d’alimentation PDU SNMP \_ .</span><span class="sxs-lookup"><span data-stu-id="7919a-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="7919a-116"><dt>**\_ensemble d’PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="7919a-117">Stocke une valeur dans une variable SNMP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7919a-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="7919a-118"><dt>**\_V1TRAP PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="7919a-119">Indique que l’interruption de la PDU est mise en forme pour être conforme à la norme SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="7919a-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="7919a-120"><dt>**\_GETBULK PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="7919a-121">Recherchez et récupérez plusieurs valeurs à l’aide d’une seule requête.</span><span class="sxs-lookup"><span data-stu-id="7919a-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="7919a-122"><dt>**\_avis du PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="7919a-123">Indique un PDU de demande d’information.</span><span class="sxs-lookup"><span data-stu-id="7919a-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="7919a-124"><dt>**interruption de l' \_ PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="7919a-125">Signale au système de gestion un événement extraordinaire sous SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="7919a-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="7919a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7919a-126">Requirements</span></span>



| <span data-ttu-id="7919a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7919a-127">Requirement</span></span> | <span data-ttu-id="7919a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7919a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7919a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7919a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7919a-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7919a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7919a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7919a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7919a-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7919a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7919a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7919a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7919a-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="7919a-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7919a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7919a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7919a-136">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="7919a-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="7919a-137">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="7919a-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="7919a-138">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="7919a-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

