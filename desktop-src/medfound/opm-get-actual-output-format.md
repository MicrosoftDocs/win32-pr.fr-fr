---
description: Retourne une description du signal vidéo qui est transmis sur le connecteur.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318745"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="fdf5c-103">\_format de \_ \_ sortie OPM \_ obtenu</span><span class="sxs-lookup"><span data-stu-id="fdf5c-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="fdf5c-104">Retourne une description du signal vidéo qui est transmis sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="fdf5c-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdf5c-105">Requirement</span></span> | <span data-ttu-id="fdf5c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdf5c-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fdf5c-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="fdf5c-107">Request GUID</span></span> | <span data-ttu-id="fdf5c-108">\_format de \_ \_ sortie OPM \_ obtenu</span><span class="sxs-lookup"><span data-stu-id="fdf5c-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="fdf5c-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="fdf5c-109">Input data</span></span>   | <span data-ttu-id="fdf5c-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="fdf5c-110">None</span></span>                                                                         |
| <span data-ttu-id="fdf5c-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="fdf5c-111">Return data</span></span>  | <span data-ttu-id="fdf5c-112">Structure [**de \_ \_ \_ format de sortie réel OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)</span><span class="sxs-lookup"><span data-stu-id="fdf5c-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fdf5c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fdf5c-113">Remarks</span></span>

<span data-ttu-id="fdf5c-114">Le signal vidéo transmis sur le connecteur n’a pas nécessairement le même format que le mode d’affichage du bureau.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="fdf5c-115">Par exemple, le mode d’affichage du Bureau peut être de 1024 x 768 pixels à 85 Hz, tandis que le connecteur peut être un connecteur S-Video qui transmet un signal vidéo à 720 x 480 pixels, 60/1.01 Hz entrelacé.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="fdf5c-116">Dans ce cas, le pilote retourne la résolution du signal S-Video, et non la résolution du bureau.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="fdf5c-117">Cette requête est équivalente à la \_ requête DXVA COPPQueryDisplayData utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="fdf5c-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf5c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdf5c-118">Requirements</span></span>



| <span data-ttu-id="fdf5c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdf5c-119">Requirement</span></span> | <span data-ttu-id="fdf5c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdf5c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf5c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdf5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf5c-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdf5c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fdf5c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdf5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf5c-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdf5c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fdf5c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdf5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf5c-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf5c-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf5c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdf5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf5c-128">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="fdf5c-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="fdf5c-129">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="fdf5c-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="fdf5c-130">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="fdf5c-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




