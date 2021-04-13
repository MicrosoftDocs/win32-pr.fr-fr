---
title: Message CB_GETDROPPEDCONTROLRECT (winuser. h)
description: Une application envoie un \_ message CB GETDROPPEDCONTROLRECT pour récupérer les coordonnées d’écran d’une zone de liste déroulante dans son état abandonné.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465719"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="ff595-104">\_Message GETDROPPEDCONTROLRECT CB</span><span class="sxs-lookup"><span data-stu-id="ff595-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="ff595-105">Une application envoie un message **CB \_ GETDROPPEDCONTROLRECT** pour récupérer les coordonnées d’écran d’une zone de liste déroulante dans son état abandonné.</span><span class="sxs-lookup"><span data-stu-id="ff595-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff595-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff595-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff595-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff595-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff595-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ff595-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff595-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff595-110">Pointeur vers la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit les coordonnées de la zone de liste déroulante dans son état abandonné.</span><span class="sxs-lookup"><span data-stu-id="ff595-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff595-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff595-111">Return value</span></span>

<span data-ttu-id="ff595-112">Si le message est correctement exécuté, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ff595-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="ff595-113">Si le message échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="ff595-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff595-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff595-114">Requirements</span></span>



| <span data-ttu-id="ff595-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff595-115">Requirement</span></span> | <span data-ttu-id="ff595-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff595-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff595-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff595-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff595-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff595-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ff595-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff595-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff595-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff595-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff595-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff595-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff595-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff595-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff595-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff595-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff595-124">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff595-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

