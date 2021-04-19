---
description: Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529723"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="780ad-103">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="780ad-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="780ad-104">Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="780ad-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="780ad-105">Le niveau de protection *virtuel* est le niveau demandé par l’application lors de la session de la sortie de protection actuelle (OPM).</span><span class="sxs-lookup"><span data-stu-id="780ad-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="780ad-106">Le pilote peut appliquer un niveau supérieur, en raison d’événements en dehors de cette session OPM.</span><span class="sxs-lookup"><span data-stu-id="780ad-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="780ad-107">Pour trouver le niveau de protection réel en vigueur, envoyez la requête [**d' \_ extraction \_ de \_ \_ niveau de protection OPM**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="780ad-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="780ad-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="780ad-108">Requirement</span></span> | <span data-ttu-id="780ad-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="780ad-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="780ad-110">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="780ad-110">Request GUID</span></span> | <span data-ttu-id="780ad-111">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="780ad-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="780ad-112">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="780ad-112">Input data</span></span>   | <span data-ttu-id="780ad-113">Mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="780ad-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="780ad-114">La valeur est interprétée comme un membre des [**indicateurs de type de protection OPM**](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="780ad-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="780ad-115">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="780ad-115">Return data</span></span>  | <span data-ttu-id="780ad-116">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="780ad-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="780ad-117">Notes</span><span class="sxs-lookup"><span data-stu-id="780ad-117">Remarks</span></span>

<span data-ttu-id="780ad-118">Le niveau de protection est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="780ad-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="780ad-119">La signification de cette valeur dépend du mécanisme de protection qui est interrogé.</span><span class="sxs-lookup"><span data-stu-id="780ad-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="780ad-120">Pour chaque mécanisme de protection, la valeur de **ulInformation** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="780ad-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="780ad-121">Mécanisme de protection</span><span class="sxs-lookup"><span data-stu-id="780ad-121">Protection mechanism</span></span> | <span data-ttu-id="780ad-122">Énumération</span><span class="sxs-lookup"><span data-stu-id="780ad-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="780ad-123">ACP</span><span class="sxs-lookup"><span data-stu-id="780ad-123">ACP</span></span>                  | [<span data-ttu-id="780ad-124">**niveau de protection de l' \_ ACP OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="780ad-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="780ad-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="780ad-125">CGMS-A</span></span>               | [<span data-ttu-id="780ad-126">**Indicateurs de protection de CGMS-A**</span><span class="sxs-lookup"><span data-stu-id="780ad-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="780ad-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="780ad-127">DPCP</span></span>                 | [<span data-ttu-id="780ad-128">**\_niveau de \_ protection \_ DPCP OPM**</span><span class="sxs-lookup"><span data-stu-id="780ad-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="780ad-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="780ad-129">HDCP</span></span>                 | [<span data-ttu-id="780ad-130">**niveau de protection pour OPM \_ HDCP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="780ad-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="780ad-131">Cette requête est équivalente à la \_ requête DXVA COPPQueryLocalProtectionLevel utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="780ad-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="780ad-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="780ad-132">Requirements</span></span>



| <span data-ttu-id="780ad-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="780ad-133">Requirement</span></span> | <span data-ttu-id="780ad-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="780ad-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="780ad-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="780ad-135">Minimum supported client</span></span><br/> | <span data-ttu-id="780ad-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="780ad-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="780ad-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="780ad-137">Minimum supported server</span></span><br/> | <span data-ttu-id="780ad-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="780ad-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="780ad-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="780ad-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="780ad-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="780ad-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780ad-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="780ad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780ad-142">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="780ad-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="780ad-143">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="780ad-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="780ad-144">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="780ad-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




