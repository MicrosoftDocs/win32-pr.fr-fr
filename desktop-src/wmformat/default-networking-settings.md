---
title: Paramètres réseau par défaut
description: Paramètres réseau par défaut
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, paramètres de mise en réseau par défaut
- ASF (Advanced Systems Format), paramètres de mise en réseau par défaut
- ASF (format des systèmes avancés), paramètres de mise en réseau par défaut
- Windows Media Format SDK, paramètres de mise en réseau
- ASF (Advanced Systems Format), paramètres de mise en réseau
- ASF (format des systèmes avancés), paramètres de mise en réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840809"
---
# <a name="default-networking-settings"></a><span data-ttu-id="64496-109">Paramètres réseau par défaut</span><span class="sxs-lookup"><span data-stu-id="64496-109">Default Networking Settings</span></span>

<span data-ttu-id="64496-110">Les tableaux suivants décrivent les paramètres par défaut des paramètres de mise en réseau dans le kit de développement logiciel (SDK) de format Windows Media, regroupés par interface.</span><span class="sxs-lookup"><span data-stu-id="64496-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="64496-111">IWMReaderNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="64496-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="64496-112">Paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="64496-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="64496-113">Temps de mise en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="64496-113">Buffering time</span></span>                        | <span data-ttu-id="64496-114">5 secondes</span><span class="sxs-lookup"><span data-stu-id="64496-114">5 seconds</span></span>                    |
| <span data-ttu-id="64496-115">UseFixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="64496-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="64496-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="64496-116">FALSE</span></span>                        |
| <span data-ttu-id="64496-117">FixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="64496-117">FixedUDPPort</span></span>                          | <span data-ttu-id="64496-118">0 (non valide)</span><span class="sxs-lookup"><span data-stu-id="64496-118">0 (not valid)</span></span>                |
| <span data-ttu-id="64496-119">ProxySetting : HTTP</span><span class="sxs-lookup"><span data-stu-id="64496-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="64496-120">\_navigateur des \_ paramètres \_ proxy WMT</span><span class="sxs-lookup"><span data-stu-id="64496-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="64496-121">ProxySetting : MMS</span><span class="sxs-lookup"><span data-stu-id="64496-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="64496-122">\_paramètre de proxy WMT \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="64496-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="64496-123">ProxySetting : RTSP</span><span class="sxs-lookup"><span data-stu-id="64496-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="64496-124">\_paramètre de proxy WMT \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="64496-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="64496-125">ProxyHostName (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="64496-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="64496-126">""</span><span class="sxs-lookup"><span data-stu-id="64496-126">""</span></span>                           |
| <span data-ttu-id="64496-127">ProxyPort : HTTP</span><span class="sxs-lookup"><span data-stu-id="64496-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="64496-128">80</span><span class="sxs-lookup"><span data-stu-id="64496-128">80</span></span>                           |
| <span data-ttu-id="64496-129">ProxyPort : MMS</span><span class="sxs-lookup"><span data-stu-id="64496-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="64496-130">1755</span><span class="sxs-lookup"><span data-stu-id="64496-130">1755</span></span>                         |
| <span data-ttu-id="64496-131">ProxtPort : RTSP</span><span class="sxs-lookup"><span data-stu-id="64496-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="64496-132">554</span><span class="sxs-lookup"><span data-stu-id="64496-132">554</span></span>                          |
| <span data-ttu-id="64496-133">ProxyExceptionList (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="64496-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="64496-134">""</span><span class="sxs-lookup"><span data-stu-id="64496-134">""</span></span>                           |
| <span data-ttu-id="64496-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="64496-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="64496-136">FALSE</span><span class="sxs-lookup"><span data-stu-id="64496-136">FALSE</span></span>                        |
| <span data-ttu-id="64496-137">ForceRerunAutoDetection</span><span class="sxs-lookup"><span data-stu-id="64496-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="64496-138">FALSE</span><span class="sxs-lookup"><span data-stu-id="64496-138">FALSE</span></span>                        |
| <span data-ttu-id="64496-139">EnableMulticast</span><span class="sxs-lookup"><span data-stu-id="64496-139">EnableMulticast</span></span>                       | <span data-ttu-id="64496-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-140">TRUE</span></span>                         |
| <span data-ttu-id="64496-141">EnableHTTP</span><span class="sxs-lookup"><span data-stu-id="64496-141">EnableHTTP</span></span>                            | <span data-ttu-id="64496-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-142">TRUE</span></span>                         |
| <span data-ttu-id="64496-143">EnableTCP</span><span class="sxs-lookup"><span data-stu-id="64496-143">EnableTCP</span></span>                             | <span data-ttu-id="64496-144">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-144">TRUE</span></span>                         |
| <span data-ttu-id="64496-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="64496-145">EnableUDP</span></span>                             | <span data-ttu-id="64496-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-146">TRUE</span></span>                         |
| <span data-ttu-id="64496-147">Bande passante de connexion</span><span class="sxs-lookup"><span data-stu-id="64496-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="64496-148">0 (détection automatique)</span><span class="sxs-lookup"><span data-stu-id="64496-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="64496-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="64496-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="64496-150">Paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="64496-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="64496-151">Durée de diffusion en continu accélérée</span><span class="sxs-lookup"><span data-stu-id="64496-151">Accelerated streaming duration</span></span> | <span data-ttu-id="64496-152">100 millions (10 secondes)</span><span class="sxs-lookup"><span data-stu-id="64496-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="64496-153">Activer la mise en cache du contenu</span><span class="sxs-lookup"><span data-stu-id="64496-153">Enable content caching</span></span>         | <span data-ttu-id="64496-154">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-154">TRUE</span></span>                   |
| <span data-ttu-id="64496-155">Activer le cache rapide</span><span class="sxs-lookup"><span data-stu-id="64496-155">Enable fast cache</span></span>              | <span data-ttu-id="64496-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-156">TRUE</span></span>                   |
| <span data-ttu-id="64496-157">Activer les renvois</span><span class="sxs-lookup"><span data-stu-id="64496-157">Enable resends</span></span>                 | <span data-ttu-id="64496-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-158">TRUE</span></span>                   |
| <span data-ttu-id="64496-159">Activer le réglage de la largeur du contenu</span><span class="sxs-lookup"><span data-stu-id="64496-159">Enable content thinning</span></span>        | <span data-ttu-id="64496-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="64496-160">TRUE</span></span>                   |
| <span data-ttu-id="64496-161">Limite de reconnexion</span><span class="sxs-lookup"><span data-stu-id="64496-161">Reconnect limit</span></span>                | <span data-ttu-id="64496-162">25</span><span class="sxs-lookup"><span data-stu-id="64496-162">25</span></span>                     |



 



| <span data-ttu-id="64496-163">IWMWriterNetworkSink</span><span class="sxs-lookup"><span data-stu-id="64496-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="64496-164">Paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="64496-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="64496-165">Nombre maximum de clients</span><span class="sxs-lookup"><span data-stu-id="64496-165">Maximum clients</span></span>      | <span data-ttu-id="64496-166">5</span><span class="sxs-lookup"><span data-stu-id="64496-166">5</span></span>                       |
| <span data-ttu-id="64496-167">Protocole réseau</span><span class="sxs-lookup"><span data-stu-id="64496-167">Network protocol</span></span>     | <span data-ttu-id="64496-168">0 ( \_ protocole WMT \_ http)</span><span class="sxs-lookup"><span data-stu-id="64496-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="64496-169">URL de l’hôte</span><span class="sxs-lookup"><span data-stu-id="64496-169">Host URL</span></span>             | <span data-ttu-id="64496-170">0 (non valide)</span><span class="sxs-lookup"><span data-stu-id="64496-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="64496-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="64496-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="64496-172">Paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="64496-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="64496-173">Taille maximale des paquets</span><span class="sxs-lookup"><span data-stu-id="64496-173">Maximum packet size</span></span> | <span data-ttu-id="64496-174">1400</span><span class="sxs-lookup"><span data-stu-id="64496-174">1400</span></span>                        |
| <span data-ttu-id="64496-175">ID de client du journal</span><span class="sxs-lookup"><span data-stu-id="64496-175">Log client ID</span></span>       | <span data-ttu-id="64496-176">FALSE</span><span class="sxs-lookup"><span data-stu-id="64496-176">FALSE</span></span>                       |
| <span data-ttu-id="64496-177">Mode de lecture</span><span class="sxs-lookup"><span data-stu-id="64496-177">Play mode</span></span>           | <span data-ttu-id="64496-178">\_sélection d' \_ autosélectionner le mode de lecture WMT \_</span><span class="sxs-lookup"><span data-stu-id="64496-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="64496-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64496-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64496-180">**Implémentation des fonctionnalités réseau**</span><span class="sxs-lookup"><span data-stu-id="64496-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




