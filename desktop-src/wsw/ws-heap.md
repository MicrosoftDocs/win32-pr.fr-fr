---
title: WS_HEAP (WebServices. h)
description: Type opaque utilisé pour référencer un objet de segment de mémoire.
ms.assetid: 1866f54f-26fc-4889-a88f-0d298a418bdc
keywords:
- WS_HEAP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d996d3a3905a7f247cfc84840e5aae4baa781f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465735"
---
# <a name="ws_heap"></a><span data-ttu-id="83911-104">\_tas WS</span><span class="sxs-lookup"><span data-stu-id="83911-104">WS\_HEAP</span></span>

<span data-ttu-id="83911-105">Type opaque utilisé pour référencer un objet de [segment de mémoire](heap.md) .</span><span class="sxs-lookup"><span data-stu-id="83911-105">An opaque type used to reference a [heap](heap.md) object.</span></span>


```C++
typedef struct _WS_HEAP WS_HEAP;
```



## <a name="remarks"></a><span data-ttu-id="83911-106">Notes</span><span class="sxs-lookup"><span data-stu-id="83911-106">Remarks</span></span>

<span data-ttu-id="83911-107">Cet objet n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="83911-107">This object is not thread safe.</span></span> <span data-ttu-id="83911-108">Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="83911-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83911-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83911-109">Requirements</span></span>



| <span data-ttu-id="83911-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83911-110">Requirement</span></span> | <span data-ttu-id="83911-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="83911-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83911-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83911-112">Minimum supported client</span></span><br/> | <span data-ttu-id="83911-113">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83911-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="83911-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83911-114">Minimum supported server</span></span><br/> | <span data-ttu-id="83911-115">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83911-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="83911-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="83911-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="83911-117"><dt>WebServices. h</dt></span><span class="sxs-lookup"><span data-stu-id="83911-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83911-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83911-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83911-119">Système</span><span class="sxs-lookup"><span data-stu-id="83911-119">Heap</span></span>](heap.md)
</dt> <dt>

[<span data-ttu-id="83911-120">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="83911-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





