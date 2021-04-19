---
description: Le \_ \_ message ajouté à la tablette WM est publié lorsqu’un périphérique tablette est ajouté à Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Message WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513211"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="ecb64-103">\_ \_ Message ajouté à la tablette WM</span><span class="sxs-lookup"><span data-stu-id="ecb64-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="ecb64-104">Le **message \_ \_ ajouté à la tablette WM** est publié lorsqu’un périphérique tablette est ajouté à Windows.</span><span class="sxs-lookup"><span data-stu-id="ecb64-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="ecb64-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecb64-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb64-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecb64-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb64-107">Index du périphérique tablette ajouté</span><span class="sxs-lookup"><span data-stu-id="ecb64-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="ecb64-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecb64-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb64-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ecb64-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecb64-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ecb64-110">Remarks</span></span>

<span data-ttu-id="ecb64-111">Ce message est envoyé à toutes les fenêtres de niveau supérieur du système, y compris les fenêtres sans propriétaire désactivées ou inactives, les fenêtres superposées et les fenêtres indépendantes. mais le message n’est pas envoyé aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="ecb64-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="ecb64-112">Les index passés dans *wParam* sont liés à l’index utilisé par la méthode [**ITabletManager :: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ecb64-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb64-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecb64-113">Requirements</span></span>



| <span data-ttu-id="ecb64-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecb64-114">Requirement</span></span> | <span data-ttu-id="ecb64-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecb64-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb64-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecb64-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb64-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecb64-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ecb64-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecb64-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb64-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecb64-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ecb64-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecb64-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb64-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb64-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
