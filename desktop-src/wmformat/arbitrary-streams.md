---
title: Flux arbitraires
description: Flux arbitraires
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, flux arbitraires
- ASF (Advanced Systems Format), flux arbitraires
- ASF (Advanced Systems Format), flux arbitraires
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux arbitraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671446"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="a4fb2-110">Flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="a4fb2-110">Arbitrary Streams</span></span>

<span data-ttu-id="a4fb2-111">En plus des flux audio et vidéo et des flux d’images, un fichier ASF peut accueillir des flux contenant une variété de données.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="a4fb2-112">Les objets du kit de développement logiciel (SDK) du format Windows Media prennent en charge les flux de script, les flux de transfert de fichiers, les flux Web et les flux de données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="a4fb2-113">Tous ces types de flux sont arbitraires, ce qui signifie qu’aucune validation de données n’est effectuée par l’objet de lecture.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="a4fb2-114">Lorsque vous incluez des flux de ces types dans vos fichiers, assurez-vous que l’application de lecture effectue la validation ou la vérification des données pour vous assurer que votre contenu n’a pas été endommagé ou déformé intentionnellement par un tiers malveillant.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="a4fb2-115">Bien que les objets de ce kit de développement logiciel ne vérifient pas ou ne valident pas les données dans des flux arbitraires, plusieurs types de flux arbitraires sont pris en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="a4fb2-116">Le tableau suivant répertorie les types de flux arbitraires prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="a4fb2-117">Les flux de script sont également pris en charge, mais sont décrits séparément dans la section [commandes de script](script-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="a4fb2-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="a4fb2-118">Pour plus d’informations sur la création de types personnalisés, consultez [flux de données arbitraires personnalisés](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="a4fb2-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="a4fb2-119">Type arbitraire</span><span class="sxs-lookup"><span data-stu-id="a4fb2-119">Arbitrary type</span></span>                   | <span data-ttu-id="a4fb2-120">Description</span><span class="sxs-lookup"><span data-stu-id="a4fb2-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="a4fb2-121">Flux de texte</span><span class="sxs-lookup"><span data-stu-id="a4fb2-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="a4fb2-122">Contiennent des chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="a4fb2-123">Flux de fichiers</span><span class="sxs-lookup"><span data-stu-id="a4fb2-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="a4fb2-124">Contiennent un ou plusieurs fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="a4fb2-125">Flux Web</span><span class="sxs-lookup"><span data-stu-id="a4fb2-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="a4fb2-126">Contiennent des fichiers de données équivalents à la version mise en cache des pages Web.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a4fb2-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4fb2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4fb2-128">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="a4fb2-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="a4fb2-129">**Flux audio et vidéo**</span><span class="sxs-lookup"><span data-stu-id="a4fb2-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="a4fb2-130">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="a4fb2-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




