---
description: Le message de la \_ tablette WM \_ supprimée est publié lorsqu’un appareil tablette est supprimé de Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Message WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515225"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="4d3d5-103">Message de suppression de la \_ tablette WM \_</span><span class="sxs-lookup"><span data-stu-id="4d3d5-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="4d3d5-104">Le message de la **\_ tablette WM \_ supprimée** est publié lorsqu’un appareil tablette est supprimé de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="4d3d5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d3d5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d3d5-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d3d5-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d3d5-107">Index du périphérique tablette en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="4d3d5-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d3d5-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d3d5-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d3d5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4d3d5-110">Remarks</span></span>

<span data-ttu-id="4d3d5-111">Ce message est envoyé à toutes les fenêtres de niveau supérieur du système, y compris les fenêtres sans propriétaire désactivées ou inactives, les fenêtres superposées et les fenêtres indépendantes. mais le message n’est pas envoyé aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="4d3d5-112">Les index passés dans *wParam* sont liés à l’index utilisé par la méthode [**ITabletManager :: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4d3d5-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d3d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d3d5-113">Requirements</span></span>



| <span data-ttu-id="4d3d5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d3d5-114">Requirement</span></span> | <span data-ttu-id="4d3d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d3d5-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3d5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d3d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3d5-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d3d5-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="4d3d5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d3d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3d5-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d3d5-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4d3d5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d3d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d3d5-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d5-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
