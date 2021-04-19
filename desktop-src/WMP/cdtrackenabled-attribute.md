---
title: Attribut CDTrackEnabled
description: L’attribut CDTrackEnabled indique si la piste est activée pour la lecture.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Attribut CDTrackEnabled lecteur Windows Media
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541755"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="48d52-104">Attribut CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="48d52-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="48d52-105">L’attribut **CDTrackEnabled** indique si la piste est activée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="48d52-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="48d52-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="48d52-106">Applies To</span></span>

-   [<span data-ttu-id="48d52-107">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="48d52-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="48d52-108">Notes</span><span class="sxs-lookup"><span data-stu-id="48d52-108">Remarks</span></span>

<span data-ttu-id="48d52-109">Cet attribut est stocké uniquement dans le cache de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="48d52-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="48d52-110">Lors de la lecture d’un CD dans le lecteur Windows Media, l’utilisateur peut sélectionner une piste et spécifier qu’elle ne doit pas être lue.</span><span class="sxs-lookup"><span data-stu-id="48d52-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="48d52-111">Cette valeur de cet attribut est true si la piste peut être lue, ou false si l’utilisateur a spécifié que la piste ne doit pas être lue.</span><span class="sxs-lookup"><span data-stu-id="48d52-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="48d52-112">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="48d52-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d52-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48d52-113">Requirements</span></span>



| <span data-ttu-id="48d52-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48d52-114">Requirement</span></span> | <span data-ttu-id="48d52-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d52-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="48d52-116">Version</span><span class="sxs-lookup"><span data-stu-id="48d52-116">Version</span></span><br/> | <span data-ttu-id="48d52-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="48d52-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48d52-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d52-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d52-119">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="48d52-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





