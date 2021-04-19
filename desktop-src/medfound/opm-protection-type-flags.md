---
description: Les indicateurs figurant dans le tableau suivant spécifient les mécanismes de protection de sortie pour la sortie de la protection des informations (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Indicateurs de type de protection OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532095"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="b24ff-103">Indicateurs de type de protection OPM</span><span class="sxs-lookup"><span data-stu-id="b24ff-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="b24ff-104">Les indicateurs figurant dans le tableau suivant spécifient les mécanismes de protection de sortie pour la sortie de la protection des informations (OPM).</span><span class="sxs-lookup"><span data-stu-id="b24ff-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="b24ff-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="b24ff-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="b24ff-106">Description</span><span class="sxs-lookup"><span data-stu-id="b24ff-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="b24ff-107"><dt>**OPM \_ TYPE de PROTECTION \_ \_ autre**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="b24ff-108">Mécanisme de protection inconnu.</span><span class="sxs-lookup"><span data-stu-id="b24ff-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="b24ff-109"><dt>**OPM \_ TYPE de PROTECTION \_ \_ aucun**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="b24ff-110">Aucun mécanisme de protection.</span><span class="sxs-lookup"><span data-stu-id="b24ff-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="b24ff-111"><dt>**OPM \_ TYPE de PROTECTION \_ \_ Copp \_ compatible avec \_**</dt> la technologie HDCP <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="b24ff-112">High-Bandwidth protection du contenu numérique (HDCP).</span><span class="sxs-lookup"><span data-stu-id="b24ff-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="b24ff-113">Cet indicateur est utilisé lors de l’émulation du protocole COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="b24ff-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="b24ff-114">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b24ff-114">For more information, see Remarks.</span></span> <span data-ttu-id="b24ff-115">Cet indicateur n’est pas pris en charge pour la sémantique OPM.</span><span class="sxs-lookup"><span data-stu-id="b24ff-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="b24ff-116"><dt>**OPM \_ TYPE de PROTECTION \_ \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="b24ff-117">Protection contre la copie analogique (ACP).</span><span class="sxs-lookup"><span data-stu-id="b24ff-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="b24ff-118"><dt>**OPM \_ TYPE de PROTECTION \_ \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="b24ff-119">Système de gestion de la génération de copie — analogique (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="b24ff-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="b24ff-120"><dt>**OPM \_ TYPE de PROTECTION \_ \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="b24ff-121">HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-121">HDCP.</span></span> <span data-ttu-id="b24ff-122">Cet indicateur est utilisé lorsque l’objet OPM a une sémantique OPM.</span><span class="sxs-lookup"><span data-stu-id="b24ff-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="b24ff-123">Elle n’est pas prise en charge pour la sémantique COPP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="b24ff-124"><dt>**OPM \_ TYPE de PROTECTION \_ \_ DPCP**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="b24ff-125">DisplayPort protection du contenu (DPCP).</span><span class="sxs-lookup"><span data-stu-id="b24ff-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="b24ff-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b24ff-126">Remarks</span></span>

<span data-ttu-id="b24ff-127">Ces indicateurs sont utilisés dans les commandes et les demandes d’État OPM suivantes.</span><span class="sxs-lookup"><span data-stu-id="b24ff-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="b24ff-128">niveau de protection de l' \_ ensemble OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="b24ff-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="b24ff-129">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="b24ff-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="b24ff-130">\_niveau de \_ \_ protection \_ de l’offre OPM</span><span class="sxs-lookup"><span data-stu-id="b24ff-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="b24ff-131">HDCP</span><span class="sxs-lookup"><span data-stu-id="b24ff-131">HDCP</span></span>

<span data-ttu-id="b24ff-132">Les deux indicateurs suivants sont définis pour HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="b24ff-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24ff-133">Value</span></span>                                         | <span data-ttu-id="b24ff-134">Description</span><span class="sxs-lookup"><span data-stu-id="b24ff-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b24ff-135">\_type de protection OPM \_ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="b24ff-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="b24ff-136">Utilisez cet indicateur si le pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) a été créé avec la sémantique OPM.</span><span class="sxs-lookup"><span data-stu-id="b24ff-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="b24ff-137">\_type de protection OPM \_ \_ \_ compatible avec le \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="b24ff-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="b24ff-138">Utilisez cet indicateur si le pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) a été créé avec la sémantique COPP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="b24ff-139">Cet indicateur correspond à l' \_ indicateur ProtectionType \_ HDCP de COPP dans COPP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="b24ff-140">Les deux modes (sémantique OPM et sémantique COPP) prennent en charge les opérations suivantes pour HDCP :</span><span class="sxs-lookup"><span data-stu-id="b24ff-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="b24ff-141">Activez ou désactivez HDCP à l’aide de la commande [OPM \_ Set \_ protection \_ Level](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="b24ff-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="b24ff-142">Demandez si HDCP est activé à l’aide de la demande d’état de [ \_ \_ \_ protection virtuelle \_ ](opm-get-virtual-protection-level.md) ou de niveau de protection OPM obtenir le niveau de [ \_ \_ \_ protection \_ ](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="b24ff-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="b24ff-143">La sémantique OPM prend également en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b24ff-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="b24ff-144">Répéteurs HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-144">HDCP repeaters.</span></span> <span data-ttu-id="b24ff-145">Un *répétiteur HDCP* est un appareil HDCP qui peut recevoir du contenu HDCP et également rechiffrer et transmettre le même contenu.</span><span class="sxs-lookup"><span data-stu-id="b24ff-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="b24ff-146">Révocation HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-146">HDCP revocation.</span></span> <span data-ttu-id="b24ff-147">Si un appareil HDCP révoqué est attaché à la sortie vidéo OPM, la sortie vidéo ne transmet pas la vidéo.</span><span class="sxs-lookup"><span data-stu-id="b24ff-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="b24ff-148">L’application n’a pas besoin d’analyser les messages de renouvellement du système HDCP (SRMs) ou de déterminer si le périphérique de sortie a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="b24ff-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="b24ff-149">Pour plus d’informations, consultez la commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="b24ff-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="b24ff-150">Lorsque la sémantique COPP est utilisée, l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) ne prend pas en charge les répéteurs HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="b24ff-151">En outre, elle ne gère pas la révocation HDCP.</span><span class="sxs-lookup"><span data-stu-id="b24ff-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="b24ff-152">Au lieu de cela, l’application doit analyser le SRM pour déterminer si un appareil HDCP a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="b24ff-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24ff-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b24ff-153">Requirements</span></span>



| <span data-ttu-id="b24ff-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b24ff-154">Requirement</span></span> | <span data-ttu-id="b24ff-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24ff-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b24ff-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b24ff-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b24ff-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b24ff-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b24ff-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b24ff-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b24ff-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b24ff-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b24ff-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="b24ff-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="b24ff-161"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b24ff-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b24ff-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b24ff-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24ff-163">Énumérations OPM</span><span class="sxs-lookup"><span data-stu-id="b24ff-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




