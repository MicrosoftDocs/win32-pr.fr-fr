---
title: Interpolation de frame
description: Interpolation de frame
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, interpolation de trame
- codecs, interpolation de trame
- interpolation de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030806"
---
# <a name="frame-interpolation"></a><span data-ttu-id="7e915-106">Interpolation de frame</span><span class="sxs-lookup"><span data-stu-id="7e915-106">Frame Interpolation</span></span>

<span data-ttu-id="7e915-107">L’interpolation de frames est le processus de création de trames vidéo intermédiaires basées sur les données dans deux images consécutives de la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="7e915-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="7e915-108">En effet, l’interpolation de frame augmente la [*fréquence d’images*](wmformat-glossary.md) de la vidéo encodée au moment du décodage.</span><span class="sxs-lookup"><span data-stu-id="7e915-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="7e915-109">Vous pouvez utiliser l’interpolation de frames pour améliorer la fluidité de la lecture des flux vidéo avec des fréquences d’images faibles.</span><span class="sxs-lookup"><span data-stu-id="7e915-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="7e915-110">Comme il s’agit d’une fonctionnalité de décodage, elle n’implique aucune option d’encodage spéciale et n’ajoute aucune surcharge au contenu.</span><span class="sxs-lookup"><span data-stu-id="7e915-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="7e915-111">L’interpolation de frame est spécifiée en tant que paramètre de sortie dans l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="7e915-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="7e915-112">Seul le codec Windows Media Video 9 prend en charge l’interpolation de trame.</span><span class="sxs-lookup"><span data-stu-id="7e915-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e915-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e915-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e915-114">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="7e915-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="7e915-115">**IWMReaderAdvanced2::SetOutputSetting**</span><span class="sxs-lookup"><span data-stu-id="7e915-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="7e915-116">**Paramètres de sortie**</span><span class="sxs-lookup"><span data-stu-id="7e915-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




