---
title: WS_SECURITY_TOKEN (WebServices. h)
description: Handle opaque représentant un jeton de sécurité.
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52e69a46f206f1def7cc2e7e2d03c2e5f1369f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465730"
---
# <a name="ws_security_token"></a><span data-ttu-id="18d6d-104">\_jeton de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="18d6d-104">WS\_SECURITY\_TOKEN</span></span>

<span data-ttu-id="18d6d-105">Handle opaque représentant un [jeton de sécurité](security-processing-results.md).</span><span class="sxs-lookup"><span data-stu-id="18d6d-105">The opaque handle representing a [security token](security-processing-results.md).</span></span>


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
```



## <a name="remarks"></a><span data-ttu-id="18d6d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="18d6d-106">Remarks</span></span>

<span data-ttu-id="18d6d-107">Cet objet n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="18d6d-107">This object is not thread safe.</span></span> <span data-ttu-id="18d6d-108">Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="18d6d-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18d6d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d6d-109">Requirements</span></span>



| <span data-ttu-id="18d6d-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d6d-110">Requirement</span></span> | <span data-ttu-id="18d6d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d6d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d6d-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d6d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="18d6d-113">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="18d6d-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="18d6d-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d6d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="18d6d-115">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="18d6d-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="18d6d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="18d6d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d6d-117"><dt>WebServices. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d6d-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d6d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d6d-119">Résultats du traitement de la sécurité</span><span class="sxs-lookup"><span data-stu-id="18d6d-119">Security Processing Results</span></span>](security-processing-results.md)
</dt> <dt>

[<span data-ttu-id="18d6d-120">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="18d6d-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





