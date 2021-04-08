---
description: Indique une demande d’arrêt d’une application et est générée lorsque l’application appelle la fonction PostQuitMessage. Ce message amène la fonction GetMessage à retourner zéro.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Message WM_QUIT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034541"
---
# <a name="wm_quit-message"></a><span data-ttu-id="a2b37-104">\_Message WM Quit</span><span class="sxs-lookup"><span data-stu-id="a2b37-104">WM\_QUIT message</span></span>

<span data-ttu-id="a2b37-105">Indique une demande d’arrêt d’une application et est générée lorsque l’application appelle la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="a2b37-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="a2b37-106">Ce message amène la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) à retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="a2b37-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="a2b37-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2b37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b37-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2b37-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b37-109">Code de sortie donné dans la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="a2b37-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="a2b37-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2b37-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b37-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2b37-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b37-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2b37-112">Return value</span></span>

<span data-ttu-id="a2b37-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a2b37-113">Type: **LRESULT**</span></span>

<span data-ttu-id="a2b37-114">Ce message n’a pas de valeur de retour, car il provoque l’arrêt de la boucle de message avant que le message ne soit envoyé à la procédure de fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="a2b37-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2b37-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a2b37-115">Remarks</span></span>

<span data-ttu-id="a2b37-116">Le message **WM \_ Quit** n’est pas associé à une fenêtre et ne sera donc jamais reçu via la procédure de fenêtre d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a2b37-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="a2b37-117">Elle est extraite uniquement par les fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="a2b37-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="a2b37-118">Ne publiez pas le message **WM \_ Quit** à l’aide de la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; utilisez [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="a2b37-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b37-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b37-119">Requirements</span></span>



| <span data-ttu-id="a2b37-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2b37-120">Requirement</span></span> | <span data-ttu-id="a2b37-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b37-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b37-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b37-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b37-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b37-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2b37-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b37-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b37-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b37-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2b37-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2b37-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b37-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b37-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b37-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b37-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2b37-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a2b37-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a2b37-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="a2b37-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="a2b37-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="a2b37-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="a2b37-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="a2b37-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="a2b37-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a2b37-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a2b37-134">Windows</span><span class="sxs-lookup"><span data-stu-id="a2b37-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
