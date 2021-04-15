---
title: Code de notification EN_PARAGRAPHEXPANDED (RichEdit. h)
description: Avertit le parent d’un contrôle RichEdit qu’un plan a été développé. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- Contrôles Windows de code de notification EN_PARAGRAPHEXPANDED
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465483"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="7dec0-105">\_Code de notification en PARAGRAPHEXPANDED</span><span class="sxs-lookup"><span data-stu-id="7dec0-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="7dec0-106">Avertit le parent d’un contrôle RichEdit qu’un plan a été développé.</span><span class="sxs-lookup"><span data-stu-id="7dec0-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="7dec0-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7dec0-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7dec0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dec0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dec0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dec0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dec0-110">Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="7dec0-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dec0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dec0-111">Requirements</span></span>



| <span data-ttu-id="7dec0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dec0-112">Requirement</span></span> | <span data-ttu-id="7dec0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dec0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dec0-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dec0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7dec0-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dec0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dec0-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dec0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7dec0-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dec0-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dec0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dec0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dec0-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dec0-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 





