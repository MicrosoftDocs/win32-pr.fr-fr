---
title: Configuration de types de flux arbitraires
description: Configuration de types de flux arbitraires
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flux, configuration de types de flux arbitraires
- codecs, configuration de types de flux arbitraires
- flux, GenProfile
- codecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511825"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="c2b8d-108">Configuration de types de flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="c2b8d-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="c2b8d-109">La plupart des types de flux arbitraires ont simplement besoin d’une vitesse de transmission, d’une fenêtre de mémoire tampon et d’un type de média majeur approprié dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c2b8d-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="c2b8d-110">Toutefois, certains types arbitraires nécessitent une configuration supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="c2b8d-111">Si vous avez des difficultés à configurer un flux, reportez-vous à l’exemple d’application appelé GenProfile, qui est inclus dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c2b8d-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="c2b8d-112">La bibliothèque définie dans GenProfile contient le code pour l’inclusion de tous les types de flux.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="c2b8d-113">Pour plus d’informations sur GenProfile et les autres exemples, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c2b8d-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="c2b8d-114">Les sections suivantes décrivent comment configurer des types de flux arbitraires.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="c2b8d-115">Section</span><span class="sxs-lookup"><span data-stu-id="c2b8d-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="c2b8d-116">Description</span><span class="sxs-lookup"><span data-stu-id="c2b8d-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2b8d-117">Configuration de flux de script</span><span class="sxs-lookup"><span data-stu-id="c2b8d-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="c2b8d-118">Décrit comment configurer des flux de script.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="c2b8d-119">Configuration des flux de transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="c2b8d-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="c2b8d-120">Décrit comment configurer des flux de transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="c2b8d-121">Configuration de flux Web</span><span class="sxs-lookup"><span data-stu-id="c2b8d-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="c2b8d-122">Décrit comment configurer des flux Web.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="c2b8d-123">Configuration de flux de texte</span><span class="sxs-lookup"><span data-stu-id="c2b8d-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="c2b8d-124">Décrit comment configurer des flux de texte.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="c2b8d-125">Configuration de flux arbitraires personnalisés</span><span class="sxs-lookup"><span data-stu-id="c2b8d-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="c2b8d-126">Décrit comment configurer des flux pour des types de flux arbitraires personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="c2b8d-127">Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="c2b8d-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="c2b8d-128">Décrit comment calculer la vitesse de transmission et les paramètres de fenêtre de mémoire tampon pour un flux arbitraire.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c2b8d-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2b8d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2b8d-130">**Flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="c2b8d-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="c2b8d-131">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="c2b8d-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




