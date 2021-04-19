---
title: Comportements de test de positionnement tactile
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier la façon dont les messages pour le test d’atteinte tactile sont traités par les fenêtres inscrites via la fonction RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510770"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="23f68-103">Comportements de test de positionnement tactile</span><span class="sxs-lookup"><span data-stu-id="23f68-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="23f68-104">Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier la façon dont les messages pour le test d’atteinte tactile sont traités par les fenêtres inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="23f68-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="23f68-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="23f68-105">Constant/value</span></span> | <span data-ttu-id="23f68-106">Description</span><span class="sxs-lookup"><span data-stu-id="23f68-106">Description</span></span> |
|---|---|
| <span data-ttu-id="23f68-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="23f68-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="23f68-108">Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) ne sont pas envoyés à la fenêtre cible, mais sont envoyés aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="23f68-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="23f68-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="23f68-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="23f68-110">Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) sont envoyés à la fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="23f68-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="23f68-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="23f68-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="23f68-112">Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) ne sont pas envoyés à la fenêtre cible ou aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="23f68-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="23f68-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23f68-113">Requirements</span></span>

| <span data-ttu-id="23f68-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23f68-114">Requirement</span></span> | <span data-ttu-id="23f68-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="23f68-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23f68-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23f68-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23f68-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="23f68-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23f68-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f68-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="23f68-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="23f68-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f68-121"><dt>Winuser. h</span><span class="sxs-lookup"><span data-stu-id="23f68-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="23f68-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f68-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="23f68-123">Constants</span></span>](constants.md)
