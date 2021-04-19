---
title: Structure DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ \_ \_ structure des niveaux de protection de sortie minimum DRM \_ contient les niveaux de protection de sortie minimum (OPLs) pour la lecture de différents types de contenu. Un appareil doit prendre en charge la OPL minimale pour qu’un type de données reçoive ce type de données à partir du lecteur.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Structure DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541262"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="ff1b5-106">\_Structure des \_ niveaux de protection de sortie DRM minimum \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff1b5-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="ff1b5-107">La structure des **\_ niveaux de \_ \_ protection \_ de sortie minimum DRM** contient les niveaux de protection de sortie minimum (OPLs) pour la lecture de différents types de contenu.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="ff1b5-108">Un appareil doit prendre en charge la OPL minimale pour qu’un type de données reçoive ce type de données à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1b5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff1b5-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="ff1b5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ff1b5-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff1b5-111">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b5-112">OPL minimale requise pour recevoir la vidéo numérique compressée.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="ff1b5-113">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b5-114">OPL minimal requis pour recevoir une vidéo numérique non compressée.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="ff1b5-115">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b5-116">OPL minimal requis pour recevoir la vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="ff1b5-117">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b5-118">OPL minimal requis pour la réception de données audio numériques compressées.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="ff1b5-119">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b5-120">OPL minimal requis pour recevoir des données audio numériques non compressées.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff1b5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ff1b5-121">Remarks</span></span>

<span data-ttu-id="ff1b5-122">Cette structure est utilisée en tant que membre de la structure de [**\_ lecture DRM \_ OPL**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1b5-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1b5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff1b5-123">Requirements</span></span>



| <span data-ttu-id="ff1b5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff1b5-124">Requirement</span></span> | <span data-ttu-id="ff1b5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff1b5-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff1b5-126">Header</span></span><br/> | <dl> <span data-ttu-id="ff1b5-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1b5-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff1b5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1b5-129">**Structures**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





