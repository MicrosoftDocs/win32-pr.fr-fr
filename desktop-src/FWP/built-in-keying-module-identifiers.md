---
title: Identificateurs de module de génération de clé intégrés (Fwpmu. h)
description: Les identificateurs des modules de génération de clé intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9e6feb726a62de02130d64cef27cd9078395b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942797"
---
# <a name="built-in-keying-module-identifiers"></a><span data-ttu-id="3a925-103">Identificateurs de module de génération de clé intégrés</span><span class="sxs-lookup"><span data-stu-id="3a925-103">Built-in Keying Module Identifiers</span></span>

<span data-ttu-id="3a925-104">Les identificateurs des modules de génération de clé intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="3a925-104">The identifiers for the keying modules that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="3a925-105">Ces identificateurs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="3a925-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="3a925-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**\_module de génération de clés FWPM \_ \_ IKE**</span><span class="sxs-lookup"><span data-stu-id="3a925-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM\_KEYING\_MODULE\_IKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a925-107">Module de génération de clés protocole IKE (Internet Key Exchange) (IKE).</span><span class="sxs-lookup"><span data-stu-id="3a925-107">Internet Key Exchange (IKE) keying module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a925-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**\_Module de génération de clés FWPM \_ \_ IKEV2**</span><span class="sxs-lookup"><span data-stu-id="3a925-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM\_KEYING\_MODULE\_IKEV2**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a925-109">Module de génération de clés IKEv2 (protocole IKE (Internet Key Exchange) version 2).</span><span class="sxs-lookup"><span data-stu-id="3a925-109">Internet Key Exchange version 2 (IKEv2) keying module.</span></span>

> [!Note]  
> <span data-ttu-id="3a925-110">Disponible uniquement sur Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a925-110">Available only on Windows Server 2008 R2 and Windows 7.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a925-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**\_module de génération de clés FWPM \_ \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="3a925-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM\_KEYING\_MODULE\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a925-112">Module de génération de clés AuthIP.</span><span class="sxs-lookup"><span data-stu-id="3a925-112">AuthIP keying module.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a925-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a925-113">Requirements</span></span>



| <span data-ttu-id="3a925-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a925-114">Requirement</span></span> | <span data-ttu-id="3a925-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a925-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a925-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a925-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a925-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a925-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a925-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a925-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a925-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a925-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a925-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a925-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a925-121"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a925-121"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





