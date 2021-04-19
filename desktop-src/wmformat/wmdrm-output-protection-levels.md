---
title: Structure WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ structure des \_ niveaux de protection de sortie WMDRM \_ contient les niveaux de protection de sortie (OPLs) requis par une licence pour effectuer diverses actions.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Structure WMDRM_OUTPUT_PROTECTION_LEVELS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523555"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="0fc7d-105">\_Structure des \_ niveaux de protection de sortie WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="0fc7d-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="0fc7d-106">La structure des **\_ niveaux de \_ protection \_ de sortie WMDRM** contient les niveaux de protection de sortie (OPLs) requis par une licence pour effectuer diverses actions.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc7d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fc7d-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="0fc7d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0fc7d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fc7d-109">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-110">OPL minimale requise pour recevoir la vidéo numérique compressée.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="0fc7d-111">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-112">OPL minimal requis pour recevoir une vidéo numérique non compressée.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="0fc7d-113">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-114">OPL minimal requis pour recevoir la vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="0fc7d-115">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-116">OPL minimal requis pour la réception de données audio numériques compressées.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="0fc7d-117">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-118">OPL minimal requis pour recevoir des données audio numériques non compressées.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="0fc7d-119">**wMinimumCopyProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="0fc7d-120">OPL minimal requis pour copier le contenu.</span><span class="sxs-lookup"><span data-stu-id="0fc7d-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fc7d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0fc7d-121">Remarks</span></span>

<span data-ttu-id="0fc7d-122">Cette structure est utilisée par la méthode [**IWMDRMLicense :: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .</span><span class="sxs-lookup"><span data-stu-id="0fc7d-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc7d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fc7d-123">Requirements</span></span>



| <span data-ttu-id="0fc7d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fc7d-124">Requirement</span></span> | <span data-ttu-id="0fc7d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fc7d-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc7d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fc7d-126">Header</span></span><br/> | <dl> <span data-ttu-id="0fc7d-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fc7d-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc7d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fc7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc7d-129">**Structures**</span><span class="sxs-lookup"><span data-stu-id="0fc7d-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





