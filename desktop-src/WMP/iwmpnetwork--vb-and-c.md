---
title: Interface IWMPNetwork (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau. L’interface IWMPNetwork expose les propriétés suivantes.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB et C) interface Windows Media Player
- Interface IWMPNetwork (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540455"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="ddf83-105">Interface IWMPNetwork (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="ddf83-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="ddf83-106">Fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.</span><span class="sxs-lookup"><span data-stu-id="ddf83-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="ddf83-107">L’interface **IWMPNetwork** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddf83-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="ddf83-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ddf83-108">Members</span></span>

<span data-ttu-id="ddf83-109">L’interface **IWMPNetwork (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddf83-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="ddf83-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddf83-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddf83-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddf83-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddf83-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddf83-112">Methods</span></span>

<span data-ttu-id="ddf83-113">L’interface **IWMPNetwork (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ddf83-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="ddf83-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ddf83-114">Method</span></span>                                                                                           | <span data-ttu-id="ddf83-115">Description</span><span class="sxs-lookup"><span data-stu-id="ddf83-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddf83-116">**getProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="ddf83-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="ddf83-117">Retourne une valeur indiquant si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="ddf83-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="ddf83-118">**getProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="ddf83-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="ddf83-119">Retourne la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="ddf83-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="ddf83-120">**getProxyName**</span><span class="sxs-lookup"><span data-stu-id="ddf83-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="ddf83-121">Retourne le nom du serveur proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="ddf83-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="ddf83-122">**getProxyPort**</span><span class="sxs-lookup"><span data-stu-id="ddf83-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="ddf83-123">Retourne le port du proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="ddf83-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="ddf83-124">**getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="ddf83-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="ddf83-125">Retourne des informations sur les paramètres de proxy pour un protocole.</span><span class="sxs-lookup"><span data-stu-id="ddf83-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="ddf83-126">**setProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="ddf83-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="ddf83-127">Spécifie si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="ddf83-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="ddf83-128">**setProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="ddf83-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="ddf83-129">Spécifie la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="ddf83-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="ddf83-130">**setProxyName**</span><span class="sxs-lookup"><span data-stu-id="ddf83-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="ddf83-131">Spécifie le nom du serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ddf83-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="ddf83-132">**setProxyPort**</span><span class="sxs-lookup"><span data-stu-id="ddf83-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="ddf83-133">Spécifie le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ddf83-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="ddf83-134">**Setproxysettings n'**</span><span class="sxs-lookup"><span data-stu-id="ddf83-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="ddf83-135">Spécifie les paramètres de proxy pour un protocole.</span><span class="sxs-lookup"><span data-stu-id="ddf83-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="ddf83-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddf83-136">Properties</span></span>

<span data-ttu-id="ddf83-137">L’interface **IWMPNetwork (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddf83-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="ddf83-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="ddf83-138">Property</span></span>                                                                                          | <span data-ttu-id="ddf83-139">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="ddf83-139">Access type</span></span>           | <span data-ttu-id="ddf83-140">Description</span><span class="sxs-lookup"><span data-stu-id="ddf83-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddf83-141">**La**</span><span class="sxs-lookup"><span data-stu-id="ddf83-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="ddf83-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-142">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-143">Obtient la bande passante actuelle de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="ddf83-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="ddf83-144">**DEBIT**</span><span class="sxs-lookup"><span data-stu-id="ddf83-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="ddf83-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-145">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-146">Obtient la vitesse de transmission actuelle en cours de réception.</span><span class="sxs-lookup"><span data-stu-id="ddf83-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="ddf83-147">**bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="ddf83-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="ddf83-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-148">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-149">Obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="ddf83-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="ddf83-150">**bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="ddf83-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="ddf83-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-151">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-152">Obtient le pourcentage de la mise en mémoire tampon terminée.</span><span class="sxs-lookup"><span data-stu-id="ddf83-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="ddf83-153">**bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="ddf83-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="ddf83-154">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddf83-154">Read/write</span></span><br/> | <span data-ttu-id="ddf83-155">Obtient ou définit la quantité de temps de mise en mémoire tampon, en millisecondes, avant le début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ddf83-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="ddf83-156">**downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="ddf83-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="ddf83-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-157">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-158">Obtient le pourcentage de téléchargement terminé.</span><span class="sxs-lookup"><span data-stu-id="ddf83-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="ddf83-159">**encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="ddf83-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="ddf83-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-160">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-161">Obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.</span><span class="sxs-lookup"><span data-stu-id="ddf83-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="ddf83-162">**Fréquence**</span><span class="sxs-lookup"><span data-stu-id="ddf83-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="ddf83-163">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-163">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-164">Obtient la fréquence d’images vidéo actuelle.</span><span class="sxs-lookup"><span data-stu-id="ddf83-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="ddf83-165">**framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="ddf83-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="ddf83-166">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-166">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-167">Obtient le nombre total de trames ignorées lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ddf83-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="ddf83-168">**lostPackets**</span><span class="sxs-lookup"><span data-stu-id="ddf83-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="ddf83-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-169">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-170">Obtient le nombre de paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="ddf83-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="ddf83-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="ddf83-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="ddf83-172">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddf83-172">Read/write</span></span><br/> | <span data-ttu-id="ddf83-173">Obtient ou définit la bande passante maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="ddf83-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="ddf83-174">**maxBitRate**</span><span class="sxs-lookup"><span data-stu-id="ddf83-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="ddf83-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-175">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-176">Obtient la vitesse de transmission vidéo maximale possible.</span><span class="sxs-lookup"><span data-stu-id="ddf83-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="ddf83-177">**receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="ddf83-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="ddf83-178">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-178">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-179">Obtient le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="ddf83-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="ddf83-180">**receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="ddf83-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="ddf83-181">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-181">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-182">Obtient le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="ddf83-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="ddf83-183">**recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="ddf83-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="ddf83-184">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-184">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-185">Obtient le nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="ddf83-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="ddf83-186">**sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="ddf83-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="ddf83-187">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddf83-187">Read-only</span></span><br/>  | <span data-ttu-id="ddf83-188">Obtient le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="ddf83-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="ddf83-189">Procurez-vous une interface **IWMPNetwork** à l’aide de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="ddf83-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="ddf83-190">Object</span><span class="sxs-lookup"><span data-stu-id="ddf83-190">Object</span></span>                                                                   | <span data-ttu-id="ddf83-191">Propriété</span><span class="sxs-lookup"><span data-stu-id="ddf83-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ddf83-192">Objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ddf83-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="ddf83-193">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="ddf83-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="ddf83-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddf83-194">Requirements</span></span>



| <span data-ttu-id="ddf83-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddf83-195">Requirement</span></span> | <span data-ttu-id="ddf83-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddf83-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ddf83-197">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddf83-197">Header</span></span><br/> | <dl> <span data-ttu-id="ddf83-198"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf83-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf83-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddf83-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf83-200">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="ddf83-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





