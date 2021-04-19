---
title: TBN_INITCUSTOMIZE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que la personnalisation a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- Contrôles Windows de code de notification TBN_INITCUSTOMIZE
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512775"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="99122-105">\_Code de notification TBN INITCUSTOMIZE</span><span class="sxs-lookup"><span data-stu-id="99122-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="99122-106">Avertit la fenêtre parente d’une barre d’outils que la personnalisation a commencé.</span><span class="sxs-lookup"><span data-stu-id="99122-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="99122-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="99122-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="99122-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99122-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99122-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99122-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99122-110">Pointeur vers la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="99122-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99122-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99122-111">Return value</span></span>

<span data-ttu-id="99122-112">Retourne TBNRF \_ HIDEHELP pour supprimer le bouton aide.</span><span class="sxs-lookup"><span data-stu-id="99122-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="99122-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99122-113">Requirements</span></span>



| <span data-ttu-id="99122-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99122-114">Requirement</span></span> | <span data-ttu-id="99122-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="99122-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99122-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99122-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99122-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99122-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99122-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99122-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99122-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99122-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99122-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="99122-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99122-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99122-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





