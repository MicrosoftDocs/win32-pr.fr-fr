---
description: Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201860"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="d4142-103">\_SRM Set \_ HDCP \_</span><span class="sxs-lookup"><span data-stu-id="d4142-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="d4142-104">Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).</span><span class="sxs-lookup"><span data-stu-id="d4142-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="d4142-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4142-105">Requirement</span></span> | <span data-ttu-id="d4142-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4142-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d4142-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="d4142-107">Command GUID</span></span> | <span data-ttu-id="d4142-108">\_SRM Set \_ HDCP \_</span><span class="sxs-lookup"><span data-stu-id="d4142-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="d4142-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="d4142-109">Input data</span></span>   | <span data-ttu-id="d4142-110">Une structure de [**\_ \_ \_ \_ paramètres SRM Set HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)</span><span class="sxs-lookup"><span data-stu-id="d4142-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="d4142-111">Le paramètre *pbAdditionalParameters* de [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) doit pointer vers une mémoire tampon qui contient le SRM.</span><span class="sxs-lookup"><span data-stu-id="d4142-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="d4142-112">Le format d’un SRM HDCP est documenté dans la spécification HDCP.</span><span class="sxs-lookup"><span data-stu-id="d4142-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="d4142-113">Définissez le paramètre *ulAdditionalParametersSize* sur la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="d4142-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4142-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d4142-114">Remarks</span></span>

<span data-ttu-id="d4142-115">Les SRMs sont utilisés pour mettre à jour la liste des appareils HDCP révoqués.</span><span class="sxs-lookup"><span data-stu-id="d4142-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="d4142-116">Les SRMs sont fournis avec le contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="d4142-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="d4142-117">Cette commande met à jour le SRM actuel de la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="d4142-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="d4142-118">Si la technologie HDCP est activée au moment de la commande, la sortie vidéo utilise le nouveau SRM pour vérifier si l’un des périphériques HDCP connectés est révoqué.</span><span class="sxs-lookup"><span data-stu-id="d4142-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="d4142-119">Si la sortie vidéo détecte un appareil révoqué, elle cesse d’afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d4142-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="d4142-120">Si vous envoyez cette commande alors que HDCP est désactivé, la sortie vidéo valide le SRM et le stocke.</span><span class="sxs-lookup"><span data-stu-id="d4142-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="d4142-121">Plus tard, si l’application active HDCP, la sortie vidéo utilise le nouveau SRM pour vérifier l’état de révocation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4142-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="d4142-122">Cette commande peut faire en sorte que la méthode **configure** retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="d4142-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="d4142-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4142-123">Return code</span></span>                                            | <span data-ttu-id="d4142-124">Description</span><span class="sxs-lookup"><span data-stu-id="d4142-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="d4142-125">ERREUR \_ Graphics de \_ \_ SRM non valide \_</span><span class="sxs-lookup"><span data-stu-id="d4142-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="d4142-126">Le SRM n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d4142-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="d4142-127">ERREUR \_ Graphics la \_ \_ sortie OPM \_ ne \_ \_ prend pas en charge \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="d4142-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="d4142-128">La sortie vidéo ne prend pas en charge HDCP.</span><span class="sxs-lookup"><span data-stu-id="d4142-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="d4142-129">Cette commande n’est pas prise en charge lorsque l’interface **IOPMVideoOutput** émule le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="d4142-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="d4142-130">Lorsque la sémantique COPP est utilisée, l’application est responsable de l’analyse de SRMs et de la vérification de l’état de révocation de l’appareil HDCP.</span><span class="sxs-lookup"><span data-stu-id="d4142-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="d4142-131">Utilisez la demande d’état des [ \_ \_ \_ \_ \_ informations sur l’appareil OPM obtenir une connexion HDCP](opm-get-connected-hdcp-device-information.md) pour obtenir le vecteur de sélection de clé de l’appareil (KSV), qui est nécessaire pour vérifier l’état de révocation.</span><span class="sxs-lookup"><span data-stu-id="d4142-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="d4142-132">Pour plus d’informations sur SRMs, reportez-vous à la spécification HDCP.</span><span class="sxs-lookup"><span data-stu-id="d4142-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4142-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4142-133">Requirements</span></span>



| <span data-ttu-id="d4142-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4142-134">Requirement</span></span> | <span data-ttu-id="d4142-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4142-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d4142-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4142-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d4142-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4142-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d4142-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4142-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d4142-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4142-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d4142-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4142-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4142-141"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4142-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4142-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4142-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4142-143">**IOPMVideoOutput :: configure**</span><span class="sxs-lookup"><span data-stu-id="d4142-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="d4142-144">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="d4142-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




