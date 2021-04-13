---
title: Objet réseau
description: L’objet réseau fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Objet réseau lecteur Windows Media
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104381007"
---
# <a name="network-object"></a><span data-ttu-id="8e387-104">Objet réseau</span><span class="sxs-lookup"><span data-stu-id="8e387-104">Network Object</span></span>

<span data-ttu-id="8e387-105">L’objet **réseau** fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.</span><span class="sxs-lookup"><span data-stu-id="8e387-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="8e387-106">L’objet **réseau** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e387-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="8e387-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="8e387-107">Property</span></span>                                           | <span data-ttu-id="8e387-108">Description</span><span class="sxs-lookup"><span data-stu-id="8e387-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e387-109">La</span><span class="sxs-lookup"><span data-stu-id="8e387-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="8e387-110">Récupère la bande passante actuelle de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8e387-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="8e387-111">DEBIT</span><span class="sxs-lookup"><span data-stu-id="8e387-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="8e387-112">Récupère la vitesse de transmission actuelle en cours de réception.</span><span class="sxs-lookup"><span data-stu-id="8e387-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="8e387-113">bufferingCount</span><span class="sxs-lookup"><span data-stu-id="8e387-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="8e387-114">Récupère le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="8e387-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="8e387-115">bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="8e387-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="8e387-116">Récupère le pourcentage de la mise en mémoire tampon terminée.</span><span class="sxs-lookup"><span data-stu-id="8e387-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="8e387-117">bufferingTime</span><span class="sxs-lookup"><span data-stu-id="8e387-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="8e387-118">Spécifie ou récupère la quantité de temps de mise en mémoire tampon, en millisecondes, avant le début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="8e387-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="8e387-119">downloadProgress</span><span class="sxs-lookup"><span data-stu-id="8e387-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="8e387-120">Récupère le pourcentage de téléchargement effectué.</span><span class="sxs-lookup"><span data-stu-id="8e387-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="8e387-121">encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="8e387-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="8e387-122">Récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu.</span><span class="sxs-lookup"><span data-stu-id="8e387-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="8e387-123">Fréquence</span><span class="sxs-lookup"><span data-stu-id="8e387-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="8e387-124">Récupère la fréquence d’images vidéo actuelle.</span><span class="sxs-lookup"><span data-stu-id="8e387-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="8e387-125">framesSkipped</span><span class="sxs-lookup"><span data-stu-id="8e387-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="8e387-126">Récupère le nombre total de trames ignorées lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="8e387-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="8e387-127">lostPackets</span><span class="sxs-lookup"><span data-stu-id="8e387-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="8e387-128">Récupère le nombre de paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="8e387-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="8e387-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="8e387-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="8e387-130">Spécifie ou récupère la bande passante maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="8e387-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="8e387-131">maxBitRate</span><span class="sxs-lookup"><span data-stu-id="8e387-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="8e387-132">Récupère la vitesse de transmission vidéo maximale possible.</span><span class="sxs-lookup"><span data-stu-id="8e387-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="8e387-133">receivedPackets</span><span class="sxs-lookup"><span data-stu-id="8e387-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="8e387-134">Récupère le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="8e387-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="8e387-135">receptionQuality</span><span class="sxs-lookup"><span data-stu-id="8e387-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="8e387-136">Récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="8e387-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="8e387-137">recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="8e387-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="8e387-138">Récupère le nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="8e387-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="8e387-139">sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="8e387-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="8e387-140">Récupère le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="8e387-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="8e387-141">L’objet **réseau** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e387-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="8e387-142">Méthode</span><span class="sxs-lookup"><span data-stu-id="8e387-142">Method</span></span>                                                       | <span data-ttu-id="8e387-143">Description</span><span class="sxs-lookup"><span data-stu-id="8e387-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e387-144">getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="8e387-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="8e387-145">Récupère une valeur qui indique si le serveur proxy doit être ignoré si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="8e387-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="8e387-146">getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="8e387-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="8e387-147">Récupère la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="8e387-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="8e387-148">getProxyName</span><span class="sxs-lookup"><span data-stu-id="8e387-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="8e387-149">Récupère le nom d’un serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e387-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="8e387-150">getProxyPort</span><span class="sxs-lookup"><span data-stu-id="8e387-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="8e387-151">Récupère le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e387-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="8e387-152">getProxySettings</span><span class="sxs-lookup"><span data-stu-id="8e387-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="8e387-153">Récupère le paramètre de proxy pour un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="8e387-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="8e387-154">setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="8e387-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="8e387-155">Spécifie une valeur qui indique si le serveur proxy doit être ignoré si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="8e387-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="8e387-156">setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="8e387-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="8e387-157">Spécifie la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="8e387-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="8e387-158">setProxyName</span><span class="sxs-lookup"><span data-stu-id="8e387-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="8e387-159">Spécifie le nom d’un serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e387-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="8e387-160">setProxyPort</span><span class="sxs-lookup"><span data-stu-id="8e387-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="8e387-161">Spécifie le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e387-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="8e387-162">Setproxysettings n'</span><span class="sxs-lookup"><span data-stu-id="8e387-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="8e387-163">Spécifie le paramètre de proxy pour un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="8e387-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="8e387-164">L’accès à l’objet **réseau** s’effectue par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="8e387-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="8e387-165">Object</span><span class="sxs-lookup"><span data-stu-id="8e387-165">Object</span></span>                      | <span data-ttu-id="8e387-166">Propriété</span><span class="sxs-lookup"><span data-stu-id="8e387-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="8e387-167">Lecteur</span><span class="sxs-lookup"><span data-stu-id="8e387-167">Player</span></span>](player-object.md) | [<span data-ttu-id="8e387-168">network</span><span class="sxs-lookup"><span data-stu-id="8e387-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="8e387-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e387-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e387-170">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="8e387-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




