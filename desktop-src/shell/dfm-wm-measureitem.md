---
description: Envoyé à la fenêtre propriétaire d’un contrôle ou d’un élément de menu lors de la création du contrôle ou du menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Message DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393436"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="ab0a1-103">\_Message DFM WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="ab0a1-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="ab0a1-104">Envoyé à la fenêtre propriétaire d’un contrôle ou d’un élément de menu lors de la création du contrôle ou du menu.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="ab0a1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab0a1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab0a1-106">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab0a1-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0a1-107">Valeur du membre **CtlID** de la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) vers laquelle pointe le paramètre *lpMeasureItem* .</span><span class="sxs-lookup"><span data-stu-id="ab0a1-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="ab0a1-108">Cette valeur identifie le contrôle qui a envoyé le message **DFM \_ WM \_ MEASUREITEM** .</span><span class="sxs-lookup"><span data-stu-id="ab0a1-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="ab0a1-109">*lpMeasureItem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ab0a1-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0a1-110">Pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui contient les dimensions de l’élément de menu ou de contrôle owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab0a1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ab0a1-111">Remarks</span></span>

<span data-ttu-id="ab0a1-112">Lorsque la fenêtre propriétaire reçoit le message **DFM \_ WM \_ MEASUREITEM** , le propriétaire remplit la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) pointée par le paramètre *lpMeasureItem* du message et retourne. cela indique au système les dimensions du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0a1-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ab0a1-113">Requirements</span></span>



| <span data-ttu-id="ab0a1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab0a1-114">Requirement</span></span> | <span data-ttu-id="ab0a1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab0a1-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0a1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab0a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0a1-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab0a1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ab0a1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab0a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0a1-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab0a1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab0a1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab0a1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0a1-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0a1-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
