---
title: Flux Web
description: Flux Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK, flux Web
- ASF (Advanced Systems Format), flux Web
- ASF (format de systèmes avancés), flux Web
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- Flux Web, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029139"
---
# <a name="web-streams"></a><span data-ttu-id="4e70c-110">Flux Web</span><span class="sxs-lookup"><span data-stu-id="4e70c-110">Web Streams</span></span>

<span data-ttu-id="4e70c-111">Un flux Web est semblable à un flux de fichier, car il contient des fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="4e70c-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="4e70c-112">Dans un flux Web, ces fichiers sont généralement des pages HTML et des graphiques associés au format GIF ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="4e70c-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="4e70c-113">Les flux Web peuvent être particulièrement utiles pour les fichiers ASF utilisés comme présentations.</span><span class="sxs-lookup"><span data-stu-id="4e70c-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="4e70c-114">Avant la prise en charge des flux Web, les présentations auraient des URL dans les flux de script dans un fichier afin qu’une page Web se chargeait à une heure prédéterminée.</span><span class="sxs-lookup"><span data-stu-id="4e70c-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="4e70c-115">La difficulté était que la congestion du réseau pouvait entraîner des retards et créer une expérience d’affichage médiocre.</span><span class="sxs-lookup"><span data-stu-id="4e70c-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="4e70c-116">Avec les flux Web, les parties constitutives des pages Web peuvent être incluses dans le fichier ASF sous forme de flux.</span><span class="sxs-lookup"><span data-stu-id="4e70c-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="4e70c-117">À mesure que les fichiers sont reçus, ils peuvent être mis en cache afin que, quand la commande pour afficher (ou rendre) une URL soit remise, elle peut être accessible instantanément par un navigateur.</span><span class="sxs-lookup"><span data-stu-id="4e70c-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="4e70c-118">Cela permet une lecture fluide et homogène.</span><span class="sxs-lookup"><span data-stu-id="4e70c-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="4e70c-119">La commande Render est fournie dans le flux Web lui-même, et non pas comme une commande de script dans un flux distinct.</span><span class="sxs-lookup"><span data-stu-id="4e70c-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="4e70c-120">Il est recommandé que les flux Web créés à l’aide du kit de développement logiciel (SDK) Windows Media Format 9 Series ou version ultérieure reçoivent le numéro de version 1.</span><span class="sxs-lookup"><span data-stu-id="4e70c-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="4e70c-121">Cette valeur est spécifiée dans la structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) dans le membre **wVersion** .</span><span class="sxs-lookup"><span data-stu-id="4e70c-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="4e70c-122">Le kit de développement logiciel (SDK) lui-même ne fait rien pour appliquer cette version.</span><span class="sxs-lookup"><span data-stu-id="4e70c-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="4e70c-123">Lors de la connexion à des flux de diffusion en direct qui ont des flux Web, il est possible que l’utilisateur puisse recevoir une commande de rendu avant que le fichier spécifié soit réellement dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="4e70c-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="4e70c-124">À moins que votre application ne gère cette condition, le navigateur affichera une erreur « page introuvable ».</span><span class="sxs-lookup"><span data-stu-id="4e70c-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4e70c-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e70c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e70c-126">**Flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="4e70c-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="4e70c-127">**Configuration de flux Web**</span><span class="sxs-lookup"><span data-stu-id="4e70c-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




