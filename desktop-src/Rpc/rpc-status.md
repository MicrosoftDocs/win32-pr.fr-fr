---
title: RPC_STATUS (rpcdce. h)
description: L’état RPC du type de données \_ représente un type de code d’état spécifique à la plateforme.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032826"
---
# <a name="rpc_status"></a><span data-ttu-id="36540-105">\_état RPC</span><span class="sxs-lookup"><span data-stu-id="36540-105">RPC\_STATUS</span></span>

<span data-ttu-id="36540-106">L' **\_ état RPC** du type de données représente un type de code d’état spécifique à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="36540-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="36540-107">Notes</span><span class="sxs-lookup"><span data-stu-id="36540-107">Remarks</span></span>

<span data-ttu-id="36540-108">Le type d' **\_ état RPC** est retourné par la plupart des fonctions RPC et fait partie de la définition du type de fonction [**\_ \_ INQ \_ FN de l’objet RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .</span><span class="sxs-lookup"><span data-stu-id="36540-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="36540-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36540-109">Requirements</span></span>



| <span data-ttu-id="36540-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36540-110">Requirement</span></span> | <span data-ttu-id="36540-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="36540-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36540-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36540-112">Minimum supported client</span></span><br/> | <span data-ttu-id="36540-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36540-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36540-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36540-114">Minimum supported server</span></span><br/> | <span data-ttu-id="36540-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36540-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36540-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="36540-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="36540-117"><dt>Rpcdce. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36540-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36540-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36540-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36540-119">**\_objet RPC \_ INQ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="36540-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





