---
description: 'En savoir plus sur : OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527885"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="21f44-103">\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM</span><span class="sxs-lookup"><span data-stu-id="21f44-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="21f44-104">Obtient des informations sur un appareil High-Bandwidth Digital protection du contenu (HDCP) attaché à la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="21f44-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="21f44-105">Les informations suivantes sont retournées :</span><span class="sxs-lookup"><span data-stu-id="21f44-105">The following information is returned:</span></span>

-   <span data-ttu-id="21f44-106">Le vecteur de sélection de clé HDCP de l’appareil (KSV).</span><span class="sxs-lookup"><span data-stu-id="21f44-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="21f44-107">Indique si l’appareil est un répétiteur HDCP.</span><span class="sxs-lookup"><span data-stu-id="21f44-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="21f44-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f44-108">Requirement</span></span> | <span data-ttu-id="21f44-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f44-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f44-110">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="21f44-110">Request GUID</span></span> | <span data-ttu-id="21f44-111">\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM</span><span class="sxs-lookup"><span data-stu-id="21f44-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="21f44-112">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="21f44-112">Input data</span></span>   | <span data-ttu-id="21f44-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="21f44-113">None</span></span>                                                                                                    |
| <span data-ttu-id="21f44-114">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="21f44-114">Return data</span></span>  | <span data-ttu-id="21f44-115">Structure [**d' \_ \_ informations d' \_ appareil \_ HDCP connectée à OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)</span><span class="sxs-lookup"><span data-stu-id="21f44-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="21f44-116">Notes</span><span class="sxs-lookup"><span data-stu-id="21f44-116">Remarks</span></span>

<span data-ttu-id="21f44-117">Cette requête peut être utilisée uniquement avec le *mode d’émulation Copp*.</span><span class="sxs-lookup"><span data-stu-id="21f44-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="21f44-118">Si l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) utilise la sémantique de sortie Protection Manager (OPM), cette demande d’État n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="21f44-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="21f44-119">KSV est un identificateur fourni au fabricant de l’appareil et est utilisé dans le processus d’authentification et d’installation HDCP.</span><span class="sxs-lookup"><span data-stu-id="21f44-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="21f44-120">En mode émulation COPP, l’application utilise KSV pour déterminer si l’appareil HDCP est révoqué.</span><span class="sxs-lookup"><span data-stu-id="21f44-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="21f44-121">Si c’est le cas, l’application ne doit pas lire de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="21f44-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="21f44-122">En outre, l’application ne doit pas lire de contenu protégé si l’appareil est un répétiteur HDCP, car COPP ne prend pas en charge les répéteurs HDCP.</span><span class="sxs-lookup"><span data-stu-id="21f44-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="21f44-123">Cette requête n’est pas nécessaire lorsque la sémantique OPM est utilisée, car OPM prend en charge la révocation des appareils et les répéteurs HDCP.</span><span class="sxs-lookup"><span data-stu-id="21f44-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="21f44-124">Cette requête est équivalente à la \_ requête DXVA COPPQueryHDCPKeyData utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="21f44-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="21f44-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f44-125">Requirements</span></span>



| <span data-ttu-id="21f44-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f44-126">Requirement</span></span> | <span data-ttu-id="21f44-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f44-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21f44-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f44-128">Minimum supported client</span></span><br/> | <span data-ttu-id="21f44-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f44-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="21f44-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f44-130">Minimum supported server</span></span><br/> | <span data-ttu-id="21f44-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f44-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21f44-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="21f44-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f44-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f44-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f44-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f44-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f44-135">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="21f44-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="21f44-136">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="21f44-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




