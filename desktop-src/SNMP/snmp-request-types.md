---
title: Types de demandes SNMP (SNMP. h)
description: Les types de demandes SNMP sont utilisés pour décrire l’opération que le service SNMP demande à l’agent d’extension d’effectuer.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466450"
---
# <a name="snmp-request-types"></a><span data-ttu-id="190b4-103">Types de demandes SNMP</span><span class="sxs-lookup"><span data-stu-id="190b4-103">SNMP Request Types</span></span>

<span data-ttu-id="190b4-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="190b4-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="190b4-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="190b4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="190b4-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="190b4-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="190b4-107">Les types de demandes SNMP sont utilisés pour décrire l’opération que le service SNMP demande à l’agent d’extension d’effectuer.</span><span class="sxs-lookup"><span data-stu-id="190b4-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="190b4-108">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="190b4-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="190b4-109">Description</span><span class="sxs-lookup"><span data-stu-id="190b4-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="190b4-110"><dt>**Protocole SNMP \_ récupération \_**</dt> de l’extension du <dt> \_ PDU \_ SNMP</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="190b4-111">Récupère la valeur des valeurs des variables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="190b4-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="190b4-112"><dt>**Protocole SNMP \_ EXTENSION \_ d' \_ extraction**</dt> de la <dt> \_ \_ PDU SNMP</dt> suivante</span><span class="sxs-lookup"><span data-stu-id="190b4-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="190b4-113">Récupère la ou les valeurs du successeur lexicographique des variables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="190b4-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="190b4-114"><dt>**Protocole SNMP \_ EXTENSION \_ récupération \_ en bloc**</dt> de la <dt> \_ PDU SNMP \_ GETBULK</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="190b4-115">Recherchez et récupérez plusieurs valeurs à l’aide d’une seule requête.</span><span class="sxs-lookup"><span data-stu-id="190b4-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="190b4-116"><dt>**\_test de \_ groupe d’extensions SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="190b4-117">Validez les valeurs des variables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="190b4-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="190b4-118">Cette opération maximise la probabilité d’une opération d’écriture réussie pendant la demande de validation.</span><span class="sxs-lookup"><span data-stu-id="190b4-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="190b4-119">Pour plus d’informations, consultez la fonction [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="190b4-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="190b4-120"><dt>**Protocole SNMP \_ \_ \_**</dt> ensemble d’extensions <dt> \_ PDU SNMP \_</dt> de validation de jeu d’extensions</span><span class="sxs-lookup"><span data-stu-id="190b4-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="190b4-121">Écrit les nouvelles valeurs dans les variables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="190b4-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="190b4-122"><dt>**\_annulation du \_ jeu d’extensions SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="190b4-123">Réinitialisez les valeurs des variables spécifiées à leurs valeurs avant la demande de validation.</span><span class="sxs-lookup"><span data-stu-id="190b4-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="190b4-124"><dt>**\_nettoyage du \_ jeu d’extensions SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="190b4-125">Libère les ressources allouées dans les requêtes et les opérations précédentes.</span><span class="sxs-lookup"><span data-stu-id="190b4-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="190b4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="190b4-126">Requirements</span></span>



| <span data-ttu-id="190b4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="190b4-127">Requirement</span></span> | <span data-ttu-id="190b4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="190b4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="190b4-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="190b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="190b4-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="190b4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="190b4-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="190b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="190b4-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="190b4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="190b4-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="190b4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="190b4-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="190b4-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="190b4-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="190b4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190b4-136">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="190b4-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="190b4-137">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="190b4-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="190b4-138">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="190b4-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

