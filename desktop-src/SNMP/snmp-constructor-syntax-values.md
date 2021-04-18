---
title: Valeurs de syntaxe du constructeur SNMP (SNMP. h)
description: Les valeurs de syntaxe du constructeur SNMP décrivent les types qui sont conformes à la norme d’encodage ASN. 1 (Abstract Syntax Notation One).
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103421"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="1ad77-103">Valeurs de syntaxe du constructeur SNMP</span><span class="sxs-lookup"><span data-stu-id="1ad77-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="1ad77-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1ad77-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ad77-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ad77-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1ad77-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="1ad77-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="1ad77-107">Les valeurs de syntaxe du constructeur SNMP décrivent les types qui sont conformes à la norme d’encodage ASN. 1 (Abstract Syntax Notation One).</span><span class="sxs-lookup"><span data-stu-id="1ad77-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="1ad77-108">Constante</span><span class="sxs-lookup"><span data-stu-id="1ad77-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="1ad77-109">Description</span><span class="sxs-lookup"><span data-stu-id="1ad77-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="1ad77-110"><dt>**\_séquence ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad77-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="1ad77-111">Indique que le message est une séquence ASN.</span><span class="sxs-lookup"><span data-stu-id="1ad77-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="1ad77-112"><dt>**\_SEQUENCEOF ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad77-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="1ad77-113">Consultez la \_ séquence ASN.</span><span class="sxs-lookup"><span data-stu-id="1ad77-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="1ad77-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ad77-114">Requirements</span></span>



| <span data-ttu-id="1ad77-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ad77-115">Requirement</span></span> | <span data-ttu-id="1ad77-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ad77-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1ad77-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ad77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad77-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ad77-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="1ad77-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ad77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad77-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ad77-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ad77-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ad77-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad77-122"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad77-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad77-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ad77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad77-124">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="1ad77-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="1ad77-125">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="1ad77-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="1ad77-126">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="1ad77-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

