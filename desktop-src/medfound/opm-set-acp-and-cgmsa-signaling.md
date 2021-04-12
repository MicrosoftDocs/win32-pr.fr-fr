---
description: Spécifie des informations sur le signal vidéo, autres que le niveau de protection.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527874"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="8a108-103">\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM</span><span class="sxs-lookup"><span data-stu-id="8a108-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="8a108-104">Spécifie des informations sur le signal vidéo, autres que le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="8a108-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="8a108-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a108-105">Requirement</span></span> | <span data-ttu-id="8a108-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a108-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a108-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="8a108-107">Command GUID</span></span> | <span data-ttu-id="8a108-108">\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM</span><span class="sxs-lookup"><span data-stu-id="8a108-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="8a108-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="8a108-109">Input data</span></span>   | <span data-ttu-id="8a108-110">Une [**structure \_ \_ \_ de \_ \_ \_ paramètres de signalisation ACP et CGMSA de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)</span><span class="sxs-lookup"><span data-stu-id="8a108-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8a108-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8a108-111">Remarks</span></span>

<span data-ttu-id="8a108-112">Cette commande est équivalente à la \_ commande DXVA COPPSetSignaling utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="8a108-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="8a108-113">Pour CGMS-A, certaines normes de protection requièrent que le signal de télévision contienne des informations dans les mêmes paquets de forme d’onde VBI que les bits CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="8a108-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="8a108-114">Ces informations incluent, entre autres, les proportions de l’image.</span><span class="sxs-lookup"><span data-stu-id="8a108-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="8a108-115">Les télévisions peuvent s’afficher mal si les informations sur les proportions ne sont pas cohérentes avec le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a108-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="8a108-116">L’application peut utiliser cette commande pour spécifier les proportions afin que le pilote Graphics puisse générer les paquets VBI appropriés.</span><span class="sxs-lookup"><span data-stu-id="8a108-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a108-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a108-117">Requirements</span></span>



| <span data-ttu-id="8a108-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a108-118">Requirement</span></span> | <span data-ttu-id="8a108-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a108-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a108-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a108-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a108-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a108-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8a108-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a108-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a108-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a108-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8a108-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a108-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a108-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a108-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a108-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a108-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a108-127">**IOPMVideoOutput :: configure**</span><span class="sxs-lookup"><span data-stu-id="8a108-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="8a108-128">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="8a108-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




