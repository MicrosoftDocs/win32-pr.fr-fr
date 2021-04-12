---
title: Structure MCI_OVLY_RECT_PARMS (Mciapi. h)
description: La \_ structure MCI OVLY \_ rect \_ PARMS contient des informations de positionnement pour les \_ commandes MCI put et MCI pour les \_ périphériques de superposition vidéo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Structure de MCI_OVLY_RECT_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464226"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="1b8d1-104">MCI \_ OVLY \_ rect \_ PARMS, structure</span><span class="sxs-lookup"><span data-stu-id="1b8d1-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="1b8d1-105">La structure **MCI \_ OVLY \_ rect \_ PARMS** contient des informations de positionnement pour les commandes [**MCI \_ put**](mci-put.md) et [**MCI \_**](mci-where.md) pour les périphériques de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="1b8d1-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b8d1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="1b8d1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1b8d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b8d1-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1b8d1-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="1b8d1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1b8d1-110">**Release**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="1b8d1-111">Rectangle contenant les informations de positionnement.</span><span class="sxs-lookup"><span data-stu-id="1b8d1-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="1b8d1-112">Les structures [Rect](/previous-versions//ms536136(v=vs.85)) sont gérées différemment dans MCI et dans d’autres parties de Windows. dans MCI, **RC. Right** contient la largeur du rectangle et **RC. Bottom** contient sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="1b8d1-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b8d1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1b8d1-113">Remarks</span></span>

<span data-ttu-id="1b8d1-114">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="1b8d1-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8d1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b8d1-115">Requirements</span></span>



| <span data-ttu-id="1b8d1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b8d1-116">Requirement</span></span> | <span data-ttu-id="1b8d1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b8d1-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8d1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8d1-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8d1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1b8d1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8d1-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8d1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b8d1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b8d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b8d1-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8d1-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b8d1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b8d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8d1-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1b8d1-126">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1b8d1-127">**\_put MCI**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="1b8d1-128">**MCI \_ où**</span><span class="sxs-lookup"><span data-stu-id="1b8d1-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="1b8d1-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b8d1-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1b8d1-130">[RECTANGULAIRE](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b8d1-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

