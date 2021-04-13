---
title: Message LVM_SETBKIMAGE (commctrl. h)
description: Définit l’image d’arrière-plan dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetBkImage.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465874"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="e1f74-105">\_Message SETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="e1f74-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="e1f74-106">Définit l’image d’arrière-plan dans un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="e1f74-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="e1f74-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .</span><span class="sxs-lookup"><span data-stu-id="e1f74-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1f74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1f74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1f74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f74-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e1f74-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e1f74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1f74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f74-112">Pointeur vers une structure [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) qui contient les nouvelles informations sur l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e1f74-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f74-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1f74-113">Return value</span></span>

<span data-ttu-id="e1f74-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e1f74-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="e1f74-115">Retourne zéro si le membre **ulFlags** de la structure [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) est **LVBKIF \_ source \_ None**.</span><span class="sxs-lookup"><span data-stu-id="e1f74-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f74-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f74-116">Remarks</span></span>

<span data-ttu-id="e1f74-117">Étant donné que le contrôle List-View utilise OLE COM pour manipuler les images d’arrière-plan, l’application appelante doit appeler [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e1f74-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="e1f74-118">Il est préférable d’appeler l’une de ces fonctions lorsque l’application est initialisée et d’appeler [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) ou [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) lorsque l’application se termine.</span><span class="sxs-lookup"><span data-stu-id="e1f74-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f74-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1f74-119">Requirements</span></span>



| <span data-ttu-id="e1f74-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1f74-120">Requirement</span></span> | <span data-ttu-id="e1f74-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f74-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f74-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1f74-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f74-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1f74-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1f74-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1f74-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f74-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1f74-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1f74-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1f74-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1f74-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1f74-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e1f74-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e1f74-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1f74-129">**LVM \_ SETBKIMAGEW** (Unicode) et **LVM \_ SETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1f74-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e1f74-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f74-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f74-131">**\_GETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="e1f74-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

