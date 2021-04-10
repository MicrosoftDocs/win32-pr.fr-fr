---
title: Code de notification EN_STARTCOMPOSITION (RichEdit. h)
description: Avertit une fenêtre parente de contrôle RichEdit que l’utilisateur a commencé à taper avec l’IME ou l’infrastructure de services de texte.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- Contrôles Windows de code de notification EN_STARTCOMPOSITION
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105556"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="6d7c4-104">\_Code de notification en STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="6d7c4-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="6d7c4-105">Avertit une fenêtre parente de contrôle RichEdit que l’utilisateur a commencé à taper avec l’IME ou l' [infrastructure de services de texte](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="6d7c4-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d7c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d7c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d7c4-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d7c4-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d7c4-108">Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="6d7c4-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d7c4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d7c4-109">Requirements</span></span>



| <span data-ttu-id="6d7c4-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d7c4-110">Requirement</span></span> | <span data-ttu-id="6d7c4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d7c4-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7c4-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d7c4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7c4-113">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d7c4-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d7c4-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d7c4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7c4-115">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d7c4-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d7c4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d7c4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d7c4-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d7c4-117"><dt>Richedit.h</dt></span></span> </dl> |



 

