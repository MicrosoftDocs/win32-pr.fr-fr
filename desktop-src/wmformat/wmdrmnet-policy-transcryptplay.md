---
title: Structure WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: La \_ structure TRANSCRYPTPLAY de la stratégie WMDRMNET \_ contient les informations de stratégie pour la diffusion de contenu à l’aide de Windows Media DRM pour les périphériques réseau.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Structure WMDRMNET_POLICY_TRANSCRYPTPLAY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528393"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="c0713-105">\_ \_ Structure TRANSCRYPTPLAY de la stratégie WMDRMNET</span><span class="sxs-lookup"><span data-stu-id="c0713-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="c0713-106">La **structure \_ \_ TRANSCRYPTPLAY de la stratégie WMDRMNET** contient les informations de stratégie pour la diffusion de contenu à l’aide de Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="c0713-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0713-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0713-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="c0713-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c0713-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0713-109">**Globals**</span><span class="sxs-lookup"><span data-stu-id="c0713-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="c0713-110">Structure de stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="c0713-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0713-111">**playOPLs**</span><span class="sxs-lookup"><span data-stu-id="c0713-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="c0713-112">Niveaux de protection de sortie pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="c0713-112">Output protection levels for playback.</span></span> <span data-ttu-id="c0713-113">**WMDRMNET \_ La \_ lecture \_ de la stratégie OPL** est un type défini comme [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).</span><span class="sxs-lookup"><span data-stu-id="c0713-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0713-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c0713-114">Remarks</span></span>

<span data-ttu-id="c0713-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c0713-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0713-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0713-116">Requirements</span></span>



| <span data-ttu-id="c0713-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0713-117">Requirement</span></span> | <span data-ttu-id="c0713-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0713-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0713-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0713-119">Header</span></span><br/> | <dl> <span data-ttu-id="c0713-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0713-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0713-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0713-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0713-122">**Structures**</span><span class="sxs-lookup"><span data-stu-id="c0713-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="c0713-123">**\_stratégie WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="c0713-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





