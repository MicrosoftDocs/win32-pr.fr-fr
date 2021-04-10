---
title: NM_GETCUSTOMSPLITRECT le code de notification (commctrl. h)
description: Envoyé par un contrôle bouton à son parent pour obtenir des mesures pour les deux rectangles du bouton partagé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Contrôles Windows de code de notification NM_GETCUSTOMSPLITRECT
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102880"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="82dff-105">\_Code de notification GETCUSTOMSPLITRECT nm</span><span class="sxs-lookup"><span data-stu-id="82dff-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="82dff-106">Envoyé par un contrôle bouton à son parent pour obtenir des mesures pour les deux rectangles du bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="82dff-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="82dff-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="82dff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="82dff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82dff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82dff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82dff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82dff-110">Pointeur vers un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) pour recevoir des informations sur les rectangles englobants.</span><span class="sxs-lookup"><span data-stu-id="82dff-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="82dff-111">La structure **NMCUSTOMSPLITRECTINFO** est envoyée avec le code de notification sous la forme d’une demande pour que le parent fournisse des mesures pour les rectangles du bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="82dff-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82dff-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82dff-112">Return value</span></span>

<span data-ttu-id="82dff-113">Retournez [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) pour indiquer au contrôle Button d’utiliser les valeurs retournées dans la structure [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; sinon, retournez la [**valeur de CDRF \_ par défaut**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="82dff-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82dff-114">Notes</span><span class="sxs-lookup"><span data-stu-id="82dff-114">Remarks</span></span>

<span data-ttu-id="82dff-115">Ce code de notification est envoyé par un contrôle Button avant d’être dessiné.</span><span class="sxs-lookup"><span data-stu-id="82dff-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="82dff-116">Le bouton doit être de style [**BS \_ SPLITBUTTON**](button-styles.md) ou [**BS \_ DEFSPLITBUTTON**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="82dff-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="82dff-117">Si les rectangles retournés au contrôle dans *lParam* ne sont pas valides, ils sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="82dff-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="82dff-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82dff-118">Requirements</span></span>



| <span data-ttu-id="82dff-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82dff-119">Requirement</span></span> | <span data-ttu-id="82dff-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="82dff-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82dff-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82dff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82dff-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82dff-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82dff-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82dff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82dff-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82dff-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82dff-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="82dff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82dff-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82dff-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





