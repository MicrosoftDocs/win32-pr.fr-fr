---
title: Identificateurs de fournisseur intégrés (Fwpmu. h)
description: Les identificateurs des fournisseurs intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510558"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="c8b17-103">Identificateurs de fournisseur intégrés</span><span class="sxs-lookup"><span data-stu-id="c8b17-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="c8b17-104">Les identificateurs des fournisseurs intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="c8b17-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="c8b17-105">Ces identificateurs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="c8b17-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="c8b17-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_IKEEXT du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c8b17-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b17-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="c8b17-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="c8b17-108">Utilisé pour identifier tous les filtres ajoutés par IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c8b17-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8b17-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ \_ configuration dos IPSec du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c8b17-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b17-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="c8b17-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="c8b17-111">Permet d’identifier tous les filtres ajoutés par la protection DoS IPsec.</span><span class="sxs-lookup"><span data-stu-id="c8b17-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="c8b17-112">Disponible uniquement sur Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c8b17-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8b17-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ déchargement TCP \_ Chimney du fournisseur FWPM**</span><span class="sxs-lookup"><span data-stu-id="c8b17-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b17-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span><span class="sxs-lookup"><span data-stu-id="c8b17-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="c8b17-115">Utilisé pour identifier tous les filtres ajoutés par le déchargement TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="c8b17-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8b17-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ modèles TCP du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c8b17-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b17-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="c8b17-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="c8b17-118">Utilisé pour identifier tous les filtres ajoutés par les modèles TCP.</span><span class="sxs-lookup"><span data-stu-id="c8b17-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="c8b17-119">Disponible uniquement sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c8b17-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8b17-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8b17-120">Requirements</span></span>



| <span data-ttu-id="c8b17-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8b17-121">Requirement</span></span> | <span data-ttu-id="c8b17-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8b17-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b17-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8b17-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b17-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8b17-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c8b17-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8b17-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b17-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8b17-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c8b17-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8b17-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b17-128"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b17-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





