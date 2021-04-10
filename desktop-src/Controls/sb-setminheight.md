---
title: Message SB_SETMINHEIGHT (commctrl. h)
description: Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942545"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="95960-104">\_Message SB SETMINHEIGHT</span><span class="sxs-lookup"><span data-stu-id="95960-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="95960-105">Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="95960-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="95960-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95960-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95960-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95960-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95960-108">Hauteur minimale, en pixels, de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="95960-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="95960-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95960-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95960-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95960-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95960-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95960-111">Return value</span></span>

<span data-ttu-id="95960-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="95960-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95960-113">Notes</span><span class="sxs-lookup"><span data-stu-id="95960-113">Remarks</span></span>

<span data-ttu-id="95960-114">La hauteur minimale est la somme de *wParam* et du double de la largeur, en pixels, de la bordure verticale de la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="95960-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="95960-115">Une application doit envoyer le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) à la fenêtre d’État pour redessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="95960-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="95960-116">Les paramètres *wParam* et *lParam* du message **de \_ taille WM** doivent être définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="95960-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="95960-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95960-117">Requirements</span></span>



| <span data-ttu-id="95960-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95960-118">Requirement</span></span> | <span data-ttu-id="95960-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="95960-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95960-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95960-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95960-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95960-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95960-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95960-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95960-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95960-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95960-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="95960-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95960-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95960-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

