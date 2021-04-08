---
title: Paramètres de Registre du port du pare-feu
description: Paramètres de Registre du port du pare-feu
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, paramètres de Registre du port de pare-feu
- Lecteur Windows Media, paramètres de Registre du port
- Lecteur Windows Media, registre
- Registre, paramètres de port de pare-feu
- Registre, paramètres de port
- Registre, paramètres pour le lecteur Windows Media
- paramètres de Registre du port du pare-feu
- paramètres du registre de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839449"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="b2ea4-111">Paramètres de Registre du port du pare-feu</span><span class="sxs-lookup"><span data-stu-id="b2ea4-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="b2ea4-112">Le lecteur Windows Media place des entrées dans le registre afin que les pare-feu puissent déterminer s’il faut ouvrir ou fermer les ports utilisés par le partage de bibliothèque multimédia.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="b2ea4-113">**Entrée de Registre AcceptedEULA**</span><span class="sxs-lookup"><span data-stu-id="b2ea4-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="b2ea4-114">Le lecteur Windows Media utilise l’entrée de Registre suivante pour indiquer si l’utilisateur a accepté le contrat de licence utilisateur final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="b2ea4-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="b2ea4-115">La valeur 1 indique que l’utilisateur a accepté le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="b2ea4-116">La valeur 0 indique que l’utilisateur n’a pas accepté le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="b2ea4-117">**Entrée de Registre WMPNSSFirewallPortsOpen**</span><span class="sxs-lookup"><span data-stu-id="b2ea4-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="b2ea4-118">Le lecteur Windows Media utilise l’entrée de Registre suivante pour indiquer si l’utilisateur a choisi de partager sa bibliothèque multimédia avec d’autres ordinateurs sur un réseau privé.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="b2ea4-119">La valeur 1 indique que l’utilisateur a choisi de partager la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="b2ea4-120">La valeur 0 indique que l’utilisateur a choisi de ne pas partager la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="b2ea4-121">**Ports associés au partage de bibliothèque multimédia**</span><span class="sxs-lookup"><span data-stu-id="b2ea4-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="b2ea4-122">Sur Windows Vista, si l’entrée de Registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="b2ea4-123">Port</span><span class="sxs-lookup"><span data-stu-id="b2ea4-123">Port</span></span>          | <span data-ttu-id="b2ea4-124">Protocol</span><span class="sxs-lookup"><span data-stu-id="b2ea4-124">Protocol</span></span>                  | <span data-ttu-id="b2ea4-125">Process</span><span class="sxs-lookup"><span data-stu-id="b2ea4-125">Process</span></span>                         | <span data-ttu-id="b2ea4-126">Sens</span><span class="sxs-lookup"><span data-stu-id="b2ea4-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="b2ea4-127">554</span><span class="sxs-lookup"><span data-stu-id="b2ea4-127">554</span></span>           | <span data-ttu-id="b2ea4-128">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-128">TCP RTSP</span></span>                  | <span data-ttu-id="b2ea4-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-130">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-130">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="b2ea4-131">8554 - 8558</span></span>   | <span data-ttu-id="b2ea4-132">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-132">TCP RTSP</span></span>                  | <span data-ttu-id="b2ea4-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-134">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-134">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="b2ea4-135">5004, 5005</span></span>    | <span data-ttu-id="b2ea4-136">PROTOCOLE RTCP/RTP UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="b2ea4-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-138">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-138">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="b2ea4-139">50004 - 50013</span></span> | <span data-ttu-id="b2ea4-140">PROTOCOLE RTCP/RTP UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="b2ea4-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-142">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-142">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-143">1900</span><span class="sxs-lookup"><span data-stu-id="b2ea4-143">1900</span></span>          | <span data-ttu-id="b2ea4-144">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-144">UDP SSDP</span></span>                  | <span data-ttu-id="b2ea4-145">SSDPsrv dans svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="b2ea4-146">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-146">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-147">2869</span><span class="sxs-lookup"><span data-stu-id="b2ea4-147">2869</span></span>          | <span data-ttu-id="b2ea4-148">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="b2ea4-149">SSDPsrv/UPnPHost dans svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="b2ea4-150">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-150">inbound</span></span>              |
| <span data-ttu-id="b2ea4-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="b2ea4-151">10280 - 10284</span></span> | <span data-ttu-id="b2ea4-152">Enregistrement UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="b2ea4-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="b2ea4-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-154">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-154">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-155">10243</span><span class="sxs-lookup"><span data-stu-id="b2ea4-155">10243</span></span>         | <span data-ttu-id="b2ea4-156">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-156">TCP HTTP</span></span>                  | <span data-ttu-id="b2ea4-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-158">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-158">inbound</span></span>              |
| <span data-ttu-id="b2ea4-159">2177</span><span class="sxs-lookup"><span data-stu-id="b2ea4-159">2177</span></span>          | <span data-ttu-id="b2ea4-160">TCP UDP qWAVE</span><span class="sxs-lookup"><span data-stu-id="b2ea4-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="b2ea4-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-161">svchost.exe</span></span>                     | <span data-ttu-id="b2ea4-162">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-162">inbound and outbound</span></span> |



 

<span data-ttu-id="b2ea4-163">Sur Windows Vista, si l’entrée de Registre **AcceptedEULA** a la valeur 1, les ports suivants doivent être ouverts.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="b2ea4-164">Port</span><span class="sxs-lookup"><span data-stu-id="b2ea4-164">Port</span></span>          | <span data-ttu-id="b2ea4-165">Protocol</span><span class="sxs-lookup"><span data-stu-id="b2ea4-165">Protocol</span></span>       | <span data-ttu-id="b2ea4-166">Process</span><span class="sxs-lookup"><span data-stu-id="b2ea4-166">Process</span></span>                         | <span data-ttu-id="b2ea4-167">Sens</span><span class="sxs-lookup"><span data-stu-id="b2ea4-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="b2ea4-168">Tous les ports UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-168">All UDP ports</span></span> | <span data-ttu-id="b2ea4-169">RTP UDP, MSB</span><span class="sxs-lookup"><span data-stu-id="b2ea4-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="b2ea4-170">wmplayer.exe, n’importe quel sous-réseau</span><span class="sxs-lookup"><span data-stu-id="b2ea4-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="b2ea4-171">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-171">inbound</span></span>              |
| <span data-ttu-id="b2ea4-172">1900</span><span class="sxs-lookup"><span data-stu-id="b2ea4-172">1900</span></span>          | <span data-ttu-id="b2ea4-173">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-173">UDP SSDP</span></span>       | <span data-ttu-id="b2ea4-174">SSDPsrv/UPnPHost dans svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="b2ea4-175">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-175">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-176">2869</span><span class="sxs-lookup"><span data-stu-id="b2ea4-176">2869</span></span>          | <span data-ttu-id="b2ea4-177">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="b2ea4-178">SSDPsrv, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="b2ea4-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="b2ea4-179">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-179">inbound</span></span>              |



 

<span data-ttu-id="b2ea4-180">Sur Microsoft Windows XP, si l’entrée de Registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.</span><span class="sxs-lookup"><span data-stu-id="b2ea4-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="b2ea4-181">Port</span><span class="sxs-lookup"><span data-stu-id="b2ea4-181">Port</span></span>          | <span data-ttu-id="b2ea4-182">Protocol</span><span class="sxs-lookup"><span data-stu-id="b2ea4-182">Protocol</span></span>                  | <span data-ttu-id="b2ea4-183">Process</span><span class="sxs-lookup"><span data-stu-id="b2ea4-183">Process</span></span>                         | <span data-ttu-id="b2ea4-184">Sens</span><span class="sxs-lookup"><span data-stu-id="b2ea4-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="b2ea4-185">1900</span><span class="sxs-lookup"><span data-stu-id="b2ea4-185">1900</span></span>          | <span data-ttu-id="b2ea4-186">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-186">UDP SSDP</span></span>                  | <span data-ttu-id="b2ea4-187">SSDPsrv dans svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="b2ea4-188">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-188">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-189">2869</span><span class="sxs-lookup"><span data-stu-id="b2ea4-189">2869</span></span>          | <span data-ttu-id="b2ea4-190">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="b2ea4-191">SSDPsrv/UPnPHost dans svchost.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="b2ea4-192">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-192">inbound</span></span>              |
| <span data-ttu-id="b2ea4-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="b2ea4-193">10280 - 10284</span></span> | <span data-ttu-id="b2ea4-194">Enregistrement UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="b2ea4-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="b2ea4-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-196">entrant et sortant</span><span class="sxs-lookup"><span data-stu-id="b2ea4-196">inbound and outbound</span></span> |
| <span data-ttu-id="b2ea4-197">10243</span><span class="sxs-lookup"><span data-stu-id="b2ea4-197">10243</span></span>         | <span data-ttu-id="b2ea4-198">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="b2ea4-198">TCP HTTP</span></span>                  | <span data-ttu-id="b2ea4-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="b2ea4-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="b2ea4-200">Vers l’intérieur de la ville</span><span class="sxs-lookup"><span data-stu-id="b2ea4-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="b2ea4-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2ea4-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2ea4-202">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="b2ea4-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




