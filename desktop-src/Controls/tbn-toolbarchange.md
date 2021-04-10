---
title: TBN_TOOLBARCHANGE le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils que l’utilisateur a personnalisé une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- Contrôles Windows de code de notification TBN_TOOLBARCHANGE
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942532"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="6cddd-105">\_Code de notification TBN TOOLBARCHANGE</span><span class="sxs-lookup"><span data-stu-id="6cddd-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="6cddd-106">Avertit la fenêtre parente de la barre d’outils que l’utilisateur a personnalisé une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="6cddd-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="6cddd-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6cddd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6cddd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cddd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cddd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cddd-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="6cddd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cddd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cddd-111">Return value</span></span>

<span data-ttu-id="6cddd-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6cddd-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cddd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cddd-113">Requirements</span></span>



| <span data-ttu-id="6cddd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cddd-114">Requirement</span></span> | <span data-ttu-id="6cddd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cddd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cddd-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cddd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6cddd-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cddd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cddd-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cddd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6cddd-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cddd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cddd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cddd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cddd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cddd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





