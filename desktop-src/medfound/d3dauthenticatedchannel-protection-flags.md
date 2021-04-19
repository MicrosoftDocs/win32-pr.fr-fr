---
description: Spécifie le niveau de protection pour le contenu vidéo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Structure D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515187"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="7497d-103">D3DAUTHENTICATEDCHANNEL \_ , \_ structure d’indicateurs de protection</span><span class="sxs-lookup"><span data-stu-id="7497d-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="7497d-104">Spécifie le niveau de protection pour le contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="7497d-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7497d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7497d-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="7497d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7497d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7497d-107">**ProtectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="7497d-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="7497d-108">Si 1, la protection du contenu vidéo est activée.</span><span class="sxs-lookup"><span data-stu-id="7497d-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7497d-109">**OverlayOrFullscreenRequired**</span><span class="sxs-lookup"><span data-stu-id="7497d-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="7497d-110">Si la valeur est 1, l’application requiert que la vidéo soit affichée à l’aide d’une superposition matérielle ou en mode exclusif plein écran.</span><span class="sxs-lookup"><span data-stu-id="7497d-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="7497d-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7497d-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7497d-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7497d-112">Reserved.</span></span> <span data-ttu-id="7497d-113">Affectez à tous les bits la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7497d-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7497d-114">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7497d-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="7497d-115">Utilisez ce membre pour accéder à tous les bits de l’Union.</span><span class="sxs-lookup"><span data-stu-id="7497d-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7497d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7497d-116">Requirements</span></span>



| <span data-ttu-id="7497d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7497d-117">Requirement</span></span> | <span data-ttu-id="7497d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7497d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7497d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7497d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7497d-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7497d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7497d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7497d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7497d-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7497d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7497d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7497d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7497d-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7497d-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7497d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7497d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7497d-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="7497d-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




