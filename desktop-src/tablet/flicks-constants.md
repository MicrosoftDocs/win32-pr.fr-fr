---
description: Voici les constantes de raccourcis.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de raccourcis (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113419"
---
# <a name="flicks-constants"></a><span data-ttu-id="39c91-103">Constantes de raccourcis</span><span class="sxs-lookup"><span data-stu-id="39c91-103">Flicks Constants</span></span>

<span data-ttu-id="39c91-104">Voici les constantes de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="39c91-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="39c91-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="39c91-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="39c91-106">Description</span><span class="sxs-lookup"><span data-stu-id="39c91-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="39c91-107"><dt>**Raccourci \_ \_ \_ Masque WM traité**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="39c91-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="39c91-108">Valeur à retourner après la gestion du message du [**\_ message de \_ raccourci WM**](wm-tablet-flick-message.md) de la tablette.</span><span class="sxs-lookup"><span data-stu-id="39c91-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="39c91-109">Si **le \_ \_ \_ masque WM WM géré** est retourné, aucune action supplémentaire ne se produit.</span><span class="sxs-lookup"><span data-stu-id="39c91-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="39c91-110">Dans le cas contraire, Windows envoie des notifications de suivi, telles que [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)ou [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown), selon l’action associée au raccourci Pen.</span><span class="sxs-lookup"><span data-stu-id="39c91-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="39c91-111"><dt>**Nombre \_ \_Directions de mouvement**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="39c91-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="39c91-112">Nombre de directions définies dans l’énumération [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .</span><span class="sxs-lookup"><span data-stu-id="39c91-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="39c91-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39c91-113">Requirements</span></span>



| <span data-ttu-id="39c91-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39c91-114">Requirement</span></span> | <span data-ttu-id="39c91-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="39c91-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c91-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39c91-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39c91-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39c91-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39c91-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39c91-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39c91-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39c91-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39c91-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="39c91-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c91-121"><dt>Tabflicks. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c91-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c91-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39c91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c91-123">**Énumération FLICKDIRECTION**</span><span class="sxs-lookup"><span data-stu-id="39c91-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="39c91-124">**Message du raccourci de \_ tablette WM \_**</span><span class="sxs-lookup"><span data-stu-id="39c91-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="39c91-125">Mouvements de raccourcis</span><span class="sxs-lookup"><span data-stu-id="39c91-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="39c91-126">[Réponse aux raccourcis stylet](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39c91-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

