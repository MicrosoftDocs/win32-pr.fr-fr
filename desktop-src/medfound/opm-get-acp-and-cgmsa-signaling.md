---
description: 'En savoir plus sur : OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536344"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="80f5e-103">\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM</span><span class="sxs-lookup"><span data-stu-id="80f5e-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="80f5e-104">Retourne les informations suivantes sur une sortie vidéo :</span><span class="sxs-lookup"><span data-stu-id="80f5e-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="80f5e-105">Liste des normes de protection de la télévision prises en charge par le pilote.</span><span class="sxs-lookup"><span data-stu-id="80f5e-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="80f5e-106">Norme actuellement active.</span><span class="sxs-lookup"><span data-stu-id="80f5e-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="80f5e-107">Proportions actuelles ou autres données de signalisation.</span><span class="sxs-lookup"><span data-stu-id="80f5e-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="80f5e-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80f5e-108">Requirement</span></span> | <span data-ttu-id="80f5e-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="80f5e-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80f5e-110">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="80f5e-110">Request GUID</span></span> | <span data-ttu-id="80f5e-111">\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM</span><span class="sxs-lookup"><span data-stu-id="80f5e-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="80f5e-112">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="80f5e-112">Input data</span></span>   | <span data-ttu-id="80f5e-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="80f5e-113">None</span></span>                                                                                |
| <span data-ttu-id="80f5e-114">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="80f5e-114">Return data</span></span>  | <span data-ttu-id="80f5e-115">Une [**structure \_ \_ de \_ \_ signalisation ACP et CGMSA OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)</span><span class="sxs-lookup"><span data-stu-id="80f5e-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80f5e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="80f5e-116">Remarks</span></span>

<span data-ttu-id="80f5e-117">Cette requête est équivalente à la \_ requête DXVA COPPQuerySignaling utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="80f5e-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="80f5e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80f5e-118">Requirements</span></span>



| <span data-ttu-id="80f5e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80f5e-119">Requirement</span></span> | <span data-ttu-id="80f5e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="80f5e-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80f5e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80f5e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80f5e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80f5e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="80f5e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80f5e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80f5e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80f5e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="80f5e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="80f5e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f5e-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80f5e-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80f5e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80f5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f5e-128">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="80f5e-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="80f5e-129">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="80f5e-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="80f5e-130">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="80f5e-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




