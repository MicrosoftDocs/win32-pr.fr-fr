---
description: Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517580"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="68388-103">Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_</span><span class="sxs-lookup"><span data-stu-id="68388-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="68388-104">Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="68388-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="68388-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68388-105">Requirement</span></span> | <span data-ttu-id="68388-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="68388-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="68388-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="68388-107">Request GUID</span></span> | <span data-ttu-id="68388-108">Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_</span><span class="sxs-lookup"><span data-stu-id="68388-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="68388-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="68388-109">Input data</span></span>   | <span data-ttu-id="68388-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="68388-110">None</span></span>                                                                        |
| <span data-ttu-id="68388-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="68388-111">Return data</span></span>  | <span data-ttu-id="68388-112">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="68388-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="68388-113">Notes</span><span class="sxs-lookup"><span data-stu-id="68388-113">Remarks</span></span>

<span data-ttu-id="68388-114">Si cette requête est réussie, le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contient le numéro de version de SRM, au format Little endian.</span><span class="sxs-lookup"><span data-stu-id="68388-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="68388-115">Les SRMs sont utilisés pour mettre à jour la liste des appareils révoqués High-Bandwidth Digital protection du contenu (HDCP).</span><span class="sxs-lookup"><span data-stu-id="68388-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="68388-116">Les SRMs sont fournis avec le contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="68388-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="68388-117">Pour définir le SRM, envoyez la commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="68388-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="68388-118">Cette requête peut provoquer la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) pour retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="68388-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="68388-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="68388-119">Return code</span></span>                                            | <span data-ttu-id="68388-120">Description</span><span class="sxs-lookup"><span data-stu-id="68388-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="68388-121">ERREUR \_ Graphics \_ OPM \_ HDCP \_ SRM \_ jamais \_ défini</span><span class="sxs-lookup"><span data-stu-id="68388-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="68388-122">L’application n’a pas défini de SRM.</span><span class="sxs-lookup"><span data-stu-id="68388-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="68388-123">ERREUR \_ Graphics la \_ \_ sortie OPM \_ ne \_ \_ prend pas en charge \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="68388-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="68388-124">La sortie vidéo ne prend pas en charge HDCP.</span><span class="sxs-lookup"><span data-stu-id="68388-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="68388-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68388-125">Requirements</span></span>



| <span data-ttu-id="68388-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68388-126">Requirement</span></span> | <span data-ttu-id="68388-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="68388-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="68388-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68388-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68388-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68388-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="68388-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68388-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68388-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68388-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="68388-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="68388-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="68388-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68388-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68388-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68388-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68388-135">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="68388-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="68388-136">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="68388-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




