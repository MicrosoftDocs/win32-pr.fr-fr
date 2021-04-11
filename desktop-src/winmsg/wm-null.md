---
description: N’effectue aucune opération. Une application envoie le \_ message WM null s’il souhaite poster un message que la fenêtre destinataire ignorera.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Message WM_NULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202881"
---
# <a name="wm_null-message"></a><span data-ttu-id="22207-104">\_Message WM null</span><span class="sxs-lookup"><span data-stu-id="22207-104">WM\_NULL message</span></span>

<span data-ttu-id="22207-105">N’effectue aucune opération.</span><span class="sxs-lookup"><span data-stu-id="22207-105">Performs no operation.</span></span> <span data-ttu-id="22207-106">Une application envoie le message **WM \_ null** s’il souhaite poster un message que la fenêtre destinataire ignorera.</span><span class="sxs-lookup"><span data-stu-id="22207-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="22207-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="22207-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="22207-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22207-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22207-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22207-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22207-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="22207-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22207-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22207-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22207-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="22207-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22207-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22207-113">Return value</span></span>

<span data-ttu-id="22207-114">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="22207-114">Type: **LRESULT**</span></span>

<span data-ttu-id="22207-115">Une application retourne la valeur zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="22207-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="22207-116">Notes</span><span class="sxs-lookup"><span data-stu-id="22207-116">Remarks</span></span>

<span data-ttu-id="22207-117">Par exemple, si une application a installé un hook **BL \_ GETMESSAGE** et qu’elle souhaite empêcher le traitement d’un message, la fonction de rappel [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) peut modifier le numéro de message en **WM \_ null** afin que le destinataire l’ignore.</span><span class="sxs-lookup"><span data-stu-id="22207-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="22207-118">Autre exemple : une application peut vérifier si une fenêtre répond aux messages en envoyant le message **WM \_ null** avec la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="22207-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22207-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22207-119">Requirements</span></span>



| <span data-ttu-id="22207-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22207-120">Requirement</span></span> | <span data-ttu-id="22207-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="22207-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22207-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22207-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22207-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22207-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22207-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22207-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22207-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22207-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22207-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="22207-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="22207-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22207-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22207-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22207-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22207-129">Vue d’ensemble de Windows</span><span class="sxs-lookup"><span data-stu-id="22207-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
