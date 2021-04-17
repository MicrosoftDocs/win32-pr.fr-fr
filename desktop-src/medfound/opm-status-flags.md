---
description: Les indicateurs figurant dans le tableau suivant spécifient l’état d’une session Protection Manager (OPM) de sortie.
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Indicateurs d’État OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527873"
---
# <a name="opm-status-flags"></a><span data-ttu-id="1ae76-103">Indicateurs d’État OPM</span><span class="sxs-lookup"><span data-stu-id="1ae76-103">OPM Status Flags</span></span>

<span data-ttu-id="1ae76-104">Les indicateurs figurant dans le tableau suivant spécifient l’état d’une session Protection Manager (OPM) de sortie.</span><span class="sxs-lookup"><span data-stu-id="1ae76-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1ae76-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="1ae76-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1ae76-106">Description</span><span class="sxs-lookup"><span data-stu-id="1ae76-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="1ae76-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="1ae76-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1ae76-108">État normal.</span><span class="sxs-lookup"><span data-stu-id="1ae76-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="1ae76-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="1ae76-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1ae76-110">L’intégrité de la connexion a été compromise.</span><span class="sxs-lookup"><span data-stu-id="1ae76-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="1ae76-111">Voici quelques exemples d’événements qui obligent le pilote à définir cet indicateur :</span><span class="sxs-lookup"><span data-stu-id="1ae76-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="1ae76-112">Le pilote ne peut plus appliquer le niveau de protection actuel.</span><span class="sxs-lookup"><span data-stu-id="1ae76-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="1ae76-113">Le pilote a détecté une erreur d’intégrité interne.</span><span class="sxs-lookup"><span data-stu-id="1ae76-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="1ae76-114">Le connecteur entre l’ordinateur et le périphérique d’affichage a été débranché.</span><span class="sxs-lookup"><span data-stu-id="1ae76-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="1ae76-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="1ae76-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1ae76-116">La configuration de la connexion a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="1ae76-116">The connection configuration has changed.</span></span> <span data-ttu-id="1ae76-117">Par exemple, l’utilisateur a modifié le mode d’affichage du bureau.</span><span class="sxs-lookup"><span data-stu-id="1ae76-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="1ae76-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="1ae76-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1ae76-119">La carte graphique ou le pilote a été falsifié.</span><span class="sxs-lookup"><span data-stu-id="1ae76-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="1ae76-120">Cet indicateur n’est pas utilisé en <em>mode émulation Copp</em>.</span><span class="sxs-lookup"><span data-stu-id="1ae76-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="1ae76-121">Au lieu de cela, la sortie vidéo définit l’indicateur OPM_STATUS_LINK_LOST s’il détecte une falsification.</span><span class="sxs-lookup"><span data-stu-id="1ae76-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="1ae76-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="1ae76-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1ae76-123">Un appareil révoqué High-Bandwidth Digital protection du contenu (HDCP) est attaché à la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="1ae76-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="1ae76-124">Cet indicateur d’État peut être retourné à partir d’une requête <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> ou <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> .</span><span class="sxs-lookup"><span data-stu-id="1ae76-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="1ae76-125">L’appareil révoqué peut être directement attaché à la sortie vidéo ou indirectement par le biais d’un Repeater HDCP.</span><span class="sxs-lookup"><span data-stu-id="1ae76-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="1ae76-126">Une sortie vidéo est nécessaire pour détecter cette condition alors que HDCP est activé, mais pas dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1ae76-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="1ae76-127">Cet indicateur n’est pas utilisé en <em>mode émulation Copp</em>, car la sortie vidéo ne détecte pas les appareils révoqués dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="1ae76-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="1ae76-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1ae76-128">Remarks</span></span>

<span data-ttu-id="1ae76-129">Certaines de ces constantes sont équivalentes aux valeurs de l’énumération **Copp \_ StatusFlags** utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="1ae76-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae76-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ae76-130">Requirements</span></span>



| <span data-ttu-id="1ae76-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ae76-131">Requirement</span></span> | <span data-ttu-id="1ae76-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ae76-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae76-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae76-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae76-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ae76-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1ae76-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae76-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae76-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ae76-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ae76-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ae76-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae76-138"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae76-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae76-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae76-140">Énumérations OPM</span><span class="sxs-lookup"><span data-stu-id="1ae76-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




