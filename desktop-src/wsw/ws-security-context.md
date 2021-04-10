---
title: WS_SECURITY_CONTEXT (WebServices. h)
description: Type opaque utilisé pour référencer un objet de contexte de sécurité.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104239"
---
# <a name="ws_security_context"></a><span data-ttu-id="aab30-104">\_contexte de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="aab30-104">WS\_SECURITY\_CONTEXT</span></span>

<span data-ttu-id="aab30-105">Type opaque utilisé pour référencer un [objet de contexte de sécurité](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="aab30-105">An opaque type used to reference a [security context object](security-context.md).</span></span>


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a><span data-ttu-id="aab30-106">Notes</span><span class="sxs-lookup"><span data-stu-id="aab30-106">Remarks</span></span>

<span data-ttu-id="aab30-107">Cet objet n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="aab30-107">This object is not thread safe.</span></span> <span data-ttu-id="aab30-108">Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="aab30-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aab30-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aab30-109">Requirements</span></span>



| <span data-ttu-id="aab30-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aab30-110">Requirement</span></span> | <span data-ttu-id="aab30-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="aab30-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab30-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab30-112">Minimum supported client</span></span><br/> | <span data-ttu-id="aab30-113">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aab30-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="aab30-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab30-114">Minimum supported server</span></span><br/> | <span data-ttu-id="aab30-115">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aab30-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aab30-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="aab30-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab30-117"><dt>WebServices. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab30-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab30-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aab30-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab30-119">Contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="aab30-119">Security Context</span></span>](security-context.md)
</dt> <dt>

[<span data-ttu-id="aab30-120">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="aab30-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





