---
title: Structures du fournisseur protocole RDP (Remote Desktop Protocol)
description: L’API de protocole distant personnalisé prend en charge les structures suivantes.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541580"
---
# <a name="remote-desktop-protocol-provider-structures"></a><span data-ttu-id="6438c-103">Structures du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="6438c-103">Remote Desktop Protocol Provider Structures</span></span>

<span data-ttu-id="6438c-104">L’API de protocole distant personnalisé prend en charge les structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="6438c-104">The custom remote protocol API supports the following structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6438c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6438c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6438c-106">**\_ \_ données de support TSMF \_ dans**</span><span class="sxs-lookup"><span data-stu-id="6438c-106">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> <dd>

<span data-ttu-id="6438c-107">Contient des informations sur les formats multimédias.</span><span class="sxs-lookup"><span data-stu-id="6438c-107">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-108">**TSMF \_ prennent en charge \_ \_ les données sortantes**</span><span class="sxs-lookup"><span data-stu-id="6438c-108">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> <dd>

<span data-ttu-id="6438c-109">Contient des informations sur les formats multimédias.</span><span class="sxs-lookup"><span data-stu-id="6438c-109">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-110">**TSMF \_ prend en charge \_ NODEDATA \_ dans**</span><span class="sxs-lookup"><span data-stu-id="6438c-110">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> <dd>

<span data-ttu-id="6438c-111">Utilisé à l’intérieur des [**\_ \_ données \_ de prise en charge TSMF dans**](tsmf-support-data-in.md) la structure pour contenir des informations sur les formats multimédias pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6438c-111">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-112">**TSMF \_ support \_ NODEDATA \_ out**</span><span class="sxs-lookup"><span data-stu-id="6438c-112">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> <dd>

<span data-ttu-id="6438c-113">Utilisé dans la structure de [**données de prise en charge de TSMF pour contenir des informations sur \_ \_ \_ les**](tsmf-support-data-out.md) formats multimédias pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6438c-113">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-114">**\_paramètres de connexion Wrds \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-114">**WRDS\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

<span data-ttu-id="6438c-115">Contient les informations de paramètres de connexion pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-115">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-116">**\_Paramètres de connexion Wrds \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6438c-116">**WRDS\_CONNECTION\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

<span data-ttu-id="6438c-117">Contient les informations de paramètres de connexion pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-117">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-118">**\_ \_ \_ informations sur les fuseaux horaires dynamiques Wrds \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-118">**WRDS\_DYNAMIC\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

<span data-ttu-id="6438c-119">Contient des informations sur les fuseaux horaires dynamiques.</span><span class="sxs-lookup"><span data-stu-id="6438c-119">Contains dynamic time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-120">**paramètres de l' \_ écouteur Wrds \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-120">**WRDS\_LISTENER\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

<span data-ttu-id="6438c-121">Contient les informations de paramètre de l’écouteur pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-121">Contains listener setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-122">**Paramètres de l' \_ écouteur Wrds \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6438c-122">**WRDS\_LISTENER\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

<span data-ttu-id="6438c-123">Contient les paramètres d’écouteur pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-123">Contains listener settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-124">**\_paramètres Wrds**</span><span class="sxs-lookup"><span data-stu-id="6438c-124">**WRDS\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

<span data-ttu-id="6438c-125">Contient des informations de paramètre relatives à la stratégie pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-125">Contains policy-related setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-126">**\_Paramètres Wrds \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6438c-126">**WRDS\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

<span data-ttu-id="6438c-127">Contient les paramètres liés à la stratégie pour une session à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-127">Contains policy-related settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-128">**\_statistiques du cache WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-128">**WTS\_CACHE\_STATS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

<span data-ttu-id="6438c-129">Contient des statistiques de cache de protocole.</span><span class="sxs-lookup"><span data-stu-id="6438c-129">Contains protocol cache statistics.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-130">**WTS \_ afficher l' \_ IOCTL**</span><span class="sxs-lookup"><span data-stu-id="6438c-130">**WTS\_DISPLAY\_IOCTL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

<span data-ttu-id="6438c-131">Contient des informations sur l’affichage du client.</span><span class="sxs-lookup"><span data-stu-id="6438c-131">Contains information about the client display.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-132">**\_données du client WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-132">**WTS\_CLIENT\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

<span data-ttu-id="6438c-133">Contient des informations sur la connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="6438c-133">Contains information about the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-134">**\_fonctionnalités de licence WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-134">**WTS\_LICENSE\_CAPABILITIES**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

<span data-ttu-id="6438c-135">Contient des informations sur les fonctionnalités de licence du client.</span><span class="sxs-lookup"><span data-stu-id="6438c-135">Contains information about the licensing capabilities of the client.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-136">**\_données de stratégie WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-136">**WTS\_POLICY\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

<span data-ttu-id="6438c-137">Contient les informations de stratégie transmises par le service Services Bureau à distance au protocole.</span><span class="sxs-lookup"><span data-stu-id="6438c-137">Contains policy information that is passed by the Remote Desktop Services service to the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-138">**valeur de la \_ propriété WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-138">**WTS\_PROPERTY\_VALUE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

<span data-ttu-id="6438c-139">Contient des informations sur une valeur de propriété à récupérer à partir du protocole.</span><span class="sxs-lookup"><span data-stu-id="6438c-139">Contains information about a property value to retrieve from the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-140">**\_cache de protocole WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-140">**WTS\_PROTOCOL\_CACHE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

<span data-ttu-id="6438c-141">Contient le nombre de lectures du cache et de présences dans le cache.</span><span class="sxs-lookup"><span data-stu-id="6438c-141">Contains the number of cache reads and cache hits.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-142">**\_compteurs de protocole WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-142">**WTS\_PROTOCOL\_COUNTERS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

<span data-ttu-id="6438c-143">Contient des compteurs de performance de protocole.</span><span class="sxs-lookup"><span data-stu-id="6438c-143">Contains protocol performance counters.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-144">**\_État du protocole WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-144">**WTS\_PROTOCOL\_STATUS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

<span data-ttu-id="6438c-145">Contient des informations sur l’état du protocole.</span><span class="sxs-lookup"><span data-stu-id="6438c-145">Contains information about the status of the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-146">**\_État du service WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-146">**WTS\_SERVICE\_STATE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

<span data-ttu-id="6438c-147">Contient des informations sur les modifications de l’état du service Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="6438c-147">Contains information about changes in the state of the Remote Desktop Services service.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-148">**\_ID de session WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-148">**WTS\_SESSION\_ID**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

<span data-ttu-id="6438c-149">Contient un **GUID** qui identifie de façon unique une session.</span><span class="sxs-lookup"><span data-stu-id="6438c-149">Contains a **GUID** that uniquely identifies a session.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-150">**WTS \_ petit \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="6438c-150">**WTS\_SMALL\_RECT**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

<span data-ttu-id="6438c-151">Contient les coordonnées de la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="6438c-151">Contains client window coordinates.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-152">**WTS \_ sockaddr**</span><span class="sxs-lookup"><span data-stu-id="6438c-152">**WTS\_SOCKADDR**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

<span data-ttu-id="6438c-153">Contient une adresse de Socket.</span><span class="sxs-lookup"><span data-stu-id="6438c-153">Contains a socket address.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-154">**WTS \_ SystemTime**</span><span class="sxs-lookup"><span data-stu-id="6438c-154">**WTS\_SYSTEMTIME**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

<span data-ttu-id="6438c-155">Spécifie les informations de date et d’heure pour les transitions entre l’heure d’hiver et l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="6438c-155">Specifies date and time information for transitions between standard time and daylight saving time.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-156">**WTS \_ les \_ informations de fuseau horaire \_**</span><span class="sxs-lookup"><span data-stu-id="6438c-156">**WTS\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

<span data-ttu-id="6438c-157">Contient des informations sur les fuseaux horaires du client.</span><span class="sxs-lookup"><span data-stu-id="6438c-157">Contains client time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-158">**\_ \_ informations d’identification de l’utilisateur WTS**</span><span class="sxs-lookup"><span data-stu-id="6438c-158">**WTS\_USER\_CREDENTIAL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

<span data-ttu-id="6438c-159">Contient les informations d’identification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6438c-159">Contains credential information for a user.</span></span>

</dd> <dt>

[<span data-ttu-id="6438c-160">**\_données utilisateur \_ WTS**</span><span class="sxs-lookup"><span data-stu-id="6438c-160">**WTS\_USER\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

<span data-ttu-id="6438c-161">Contient des valeurs de propriété de client sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="6438c-161">Contains select client property values.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6438c-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6438c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6438c-163">Référence du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="6438c-163">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="6438c-164">Énumérations du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="6438c-164">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="6438c-165">Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="6438c-165">Remote Desktop Protocol Provider Interfaces</span></span>](custom-remote-protocol-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6438c-166">Unions de fournisseurs protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="6438c-166">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




