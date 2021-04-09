---
description: Retourne le niveau de protection global pour un mécanisme de protection spécifié.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034155"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="04929-103">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="04929-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="04929-104">Retourne le niveau de protection global pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="04929-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="04929-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04929-105">Requirement</span></span> | <span data-ttu-id="04929-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="04929-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04929-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="04929-107">Request GUID</span></span> | <span data-ttu-id="04929-108">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="04929-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="04929-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="04929-109">Input data</span></span>   | <span data-ttu-id="04929-110">Mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="04929-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="04929-111">La valeur est interprétée comme un membre des [indicateurs de type de protection OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="04929-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="04929-112">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="04929-112">Return data</span></span>  | <span data-ttu-id="04929-113">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="04929-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="04929-114">Notes</span><span class="sxs-lookup"><span data-stu-id="04929-114">Remarks</span></span>

<span data-ttu-id="04929-115">Le niveau de protection global est le niveau de protection en cours d’application sur le connecteur, quelle que soit la façon dont le pilote Graphics a été invité à appliquer la protection.</span><span class="sxs-lookup"><span data-stu-id="04929-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="04929-116">Par exemple, une application peut définir le niveau de protection ACP en appelant la fonction **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="04929-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="04929-117">Dans ce cas, le niveau de protection global reflète ce paramètre, même s’il n’a pas été demandé par le biais de Output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="04929-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="04929-118">Le niveau de protection est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="04929-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="04929-119">La signification de cette valeur dépend du mécanisme de protection qui est interrogé.</span><span class="sxs-lookup"><span data-stu-id="04929-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="04929-120">Pour chaque mécanisme de protection, la valeur de **ulInformation** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="04929-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="04929-121">Mécanisme de protection</span><span class="sxs-lookup"><span data-stu-id="04929-121">Protection mechanism</span></span> | <span data-ttu-id="04929-122">Énumération</span><span class="sxs-lookup"><span data-stu-id="04929-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04929-123">ACP</span><span class="sxs-lookup"><span data-stu-id="04929-123">ACP</span></span>                  | [<span data-ttu-id="04929-124">**niveau de protection de l' \_ ACP OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04929-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="04929-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="04929-125">CGMS-A</span></span>               | [<span data-ttu-id="04929-126">Indicateurs de protection de CGMS-A</span><span class="sxs-lookup"><span data-stu-id="04929-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="04929-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="04929-127">DPCP</span></span>                 | [<span data-ttu-id="04929-128">**\_niveau de \_ protection \_ DPCP OPM**</span><span class="sxs-lookup"><span data-stu-id="04929-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="04929-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="04929-129">HDCP</span></span>                 | [<span data-ttu-id="04929-130">**niveau de protection pour OPM \_ HDCP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04929-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="04929-131">Cette requête est équivalente à la \_ requête DXVA COPPQueryGlobalProtectionLevel utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="04929-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="04929-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04929-132">Requirements</span></span>



| <span data-ttu-id="04929-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04929-133">Requirement</span></span> | <span data-ttu-id="04929-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="04929-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="04929-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04929-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04929-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04929-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="04929-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04929-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04929-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04929-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="04929-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="04929-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04929-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="04929-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04929-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04929-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04929-142">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="04929-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="04929-143">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="04929-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="04929-144">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="04929-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




