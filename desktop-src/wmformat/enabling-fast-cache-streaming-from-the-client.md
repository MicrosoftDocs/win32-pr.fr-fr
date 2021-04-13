---
title: Activation de la diffusion en continu du cache rapide à partir du client
description: Activation de la diffusion en continu du cache rapide à partir du client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK, activation de la diffusion en continu du cache rapide
- Windows Media Format SDK, Fast cache streaming
- ASF (Advanced Systems Format), activation de la diffusion en continu du cache rapide
- ASF (format avancé des systèmes), activation de la diffusion en continu du cache rapide
- ASF (Advanced Systems Format), diffusion en continu du cache rapide
- ASF (format de systèmes avancés), diffusion en continu de cache rapide
- flux, activation de la diffusion en continu du cache rapide
- Streaming de cache rapide, activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381500"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="f562c-111">Activation de la diffusion en continu du cache rapide à partir du client</span><span class="sxs-lookup"><span data-stu-id="f562c-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="f562c-112">Fast cache est une technologie de diffusion en continu dans laquelle le serveur associer façon opportuniste diffuse du contenu à un débit plus élevé que ce qui est nécessaire pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="f562c-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="f562c-113">Si la bande passante disponible est supérieure à la vitesse de transmission du contenu, le cache rapide diffuse à la vitesse supérieure et met en mémoire tampon le contenu.</span><span class="sxs-lookup"><span data-stu-id="f562c-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="f562c-114">Cela permet de réduire les interruptions ultérieurement si le réseau est encombré.</span><span class="sxs-lookup"><span data-stu-id="f562c-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="f562c-115">Si la bande passante réseau est inférieure à la vitesse de transmission du contenu, le cache rapide met en mémoire tampon une partie des données avant le démarrage de la lecture.</span><span class="sxs-lookup"><span data-stu-id="f562c-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="f562c-116">Le cache rapide est recommandé pour les réseaux non fiables, tels que les réseaux sans fil ou les réseaux qui subissent des fluctuations importantes du trafic réseau, telles que les modems câble.</span><span class="sxs-lookup"><span data-stu-id="f562c-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="f562c-117">Il est également recommandé pour le contenu VBR (variable bit rate).</span><span class="sxs-lookup"><span data-stu-id="f562c-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="f562c-118">Les exigences en matière de bande passante pour le contenu VBR ne sont pas constantes, et le cache rapide permet au lecteur de mettre le flux en mémoire tampon pendant les parties à débit inférieur.</span><span class="sxs-lookup"><span data-stu-id="f562c-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="f562c-119">La diffusion en continu du cache rapide est prise en charge uniquement pour le contenu à la demande.</span><span class="sxs-lookup"><span data-stu-id="f562c-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="f562c-120">En outre, le serveur doit être configuré pour utiliser la diffusion en continu du cache rapide.</span><span class="sxs-lookup"><span data-stu-id="f562c-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="f562c-121">Pour activer Fast cache dans l’objet Reader, appelez les méthodes [**IWMReaderNetworkConfig2 :: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) et [**IWMReaderNetworkConfig2 :: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="f562c-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="f562c-122">La première méthode permet au lecteur de mettre en cache le contenu diffusé en continu.</span><span class="sxs-lookup"><span data-stu-id="f562c-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="f562c-123">Le deuxième permet d’utiliser rapidement le cache en particulier.</span><span class="sxs-lookup"><span data-stu-id="f562c-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="f562c-124">Avec ces paramètres, le lecteur active le cache rapide par défaut si la bande passante réseau est sensiblement supérieure ou inférieure à la vitesse de transmission du contenu, et si le serveur le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f562c-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="f562c-125">L’utilisateur peut également contrôler si l’objet lecteur utilise Fast cache en ajoutant un ou plusieurs des modificateurs suivants à l’URL.</span><span class="sxs-lookup"><span data-stu-id="f562c-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="f562c-126">Modificateur</span><span class="sxs-lookup"><span data-stu-id="f562c-126">Modifier</span></span>         | <span data-ttu-id="f562c-127">Description</span><span class="sxs-lookup"><span data-stu-id="f562c-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f562c-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="f562c-128">WMCache</span></span>          | <span data-ttu-id="f562c-129">Si ce modificateur est présent, la valeur « 0 » désactive explicitement le cache rapide, tandis que la valeur « 1 » l’active explicitement.</span><span class="sxs-lookup"><span data-stu-id="f562c-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="f562c-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="f562c-130">WMBitrate</span></span>        | <span data-ttu-id="f562c-131">Ce modificateur spécifie la vitesse de transmission maximale du serveur.</span><span class="sxs-lookup"><span data-stu-id="f562c-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="f562c-132">Ce modificateur peut être utilisé pour limiter Fast cache à une certaine limite de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f562c-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="f562c-133">Ce modificateur est ignoré si une bande passante de connexion explicite est déjà définie à l’aide d’un appel à [**IWMReaderNetworkConfig :: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span><span class="sxs-lookup"><span data-stu-id="f562c-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="f562c-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="f562c-134">WMContentBitrate</span></span> | <span data-ttu-id="f562c-135">Ce modificateur spécifie la vitesse de transmission du contenu.</span><span class="sxs-lookup"><span data-stu-id="f562c-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="f562c-136">Le lecteur utilise ce modificateur, s’il est présent, lorsqu’il sélectionne des flux à partir d’un fichier de débit binaire multiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="f562c-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="f562c-137">Cela peut amener le lecteur à recevoir un contenu à débit élevé sur une connexion lente, ce qui se traduit par des temps de mise en mémoire tampon et des retards très longs.</span><span class="sxs-lookup"><span data-stu-id="f562c-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="f562c-138">Le modificateur WMCache = 1 force le lecteur à utiliser la diffusion en continu de cache rapide, quelle que soit la bande passante réseau ou la vitesse de transmission du contenu et quels que soient les appels précédents à **SetEnableFastCache**.</span><span class="sxs-lookup"><span data-stu-id="f562c-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="f562c-139">Toutefois, elle ne remplace pas le paramètre **SetEnableContentCaching** sur le lecteur ; il ne remplace pas non plus la configuration du serveur.</span><span class="sxs-lookup"><span data-stu-id="f562c-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="f562c-140">Les modificateurs d’URL se présentent sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f562c-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="f562c-141">*URL*? *modificateur* = *valeur*</span><span class="sxs-lookup"><span data-stu-id="f562c-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="f562c-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f562c-142">For example:</span></span>

<span data-ttu-id="f562c-143">mms://MyServer/MyVideo.wmv ? WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="f562c-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="f562c-144">Plusieurs modificateurs peuvent être spécifiés ; Utilisez une esperluette (&) pour les séparer :</span><span class="sxs-lookup"><span data-stu-id="f562c-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="f562c-145">mms://MyServer/MyVideo.wmv ? WMCache = 1&WMContentBitrate = 56000</span><span class="sxs-lookup"><span data-stu-id="f562c-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




