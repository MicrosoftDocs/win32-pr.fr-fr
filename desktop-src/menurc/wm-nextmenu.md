---
title: Message WM_NEXTMENU (winuser. h)
description: Envoyé à une application lorsque la touche de direction droite ou gauche est utilisée pour basculer entre la barre de menus et le menu système.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942878"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="b6eb6-104">\_Message WM NEXTMENU</span><span class="sxs-lookup"><span data-stu-id="b6eb6-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="b6eb6-105">Envoyé à une application lorsque la touche de direction droite ou gauche est utilisée pour basculer entre la barre de menus et le menu système.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="b6eb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6eb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6eb6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6eb6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6eb6-108">Code de la clé virtuelle de la clé.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-108">The virtual-key code of the key.</span></span> <span data-ttu-id="b6eb6-109">Consultez [**codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="b6eb6-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="b6eb6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6eb6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6eb6-111">Pointeur vers une structure [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) qui contient des informations sur le menu à activer.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6eb6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6eb6-112">Remarks</span></span>

<span data-ttu-id="b6eb6-113">En répondant à ce message, l’application peut spécifier le menu vers lequel basculer dans le membre **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) et la fenêtre pour recevoir les messages de notification de menu dans le membre **hwndNext** de la structure **MDINEXTMENU** .</span><span class="sxs-lookup"><span data-stu-id="b6eb6-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="b6eb6-114">Vous devez définir les deux membres pour que les modifications prennent effet (elles ont initialement la **valeur null**).</span><span class="sxs-lookup"><span data-stu-id="b6eb6-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6eb6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6eb6-115">Requirements</span></span>



| <span data-ttu-id="b6eb6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6eb6-116">Requirement</span></span> | <span data-ttu-id="b6eb6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6eb6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6eb6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6eb6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6eb6-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6eb6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6eb6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6eb6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6eb6-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6eb6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6eb6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6eb6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6eb6-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6eb6-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6eb6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6eb6-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6eb6-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b6eb6-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6eb6-126">**MDINEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="b6eb6-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="b6eb6-127">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b6eb6-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6eb6-128">Menus</span><span class="sxs-lookup"><span data-stu-id="b6eb6-128">Menus</span></span>](menus.md)
</dt> </dl>

 

