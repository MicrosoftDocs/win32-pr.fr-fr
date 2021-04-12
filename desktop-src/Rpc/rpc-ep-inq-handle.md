---
title: RPC_EP_INQ_HANDLE (Rpcasync. h)
description: Le \_ \_ \_ type de données de descripteur INQ EP RPC déclare un handle pour un contexte de recherche. Les applications RPC l’utilisent pour afficher les informations d’adresse de serveur stockées dans le mappage de point de terminaison.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385135"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="d5e37-105">\_ \_ descripteur INQ RPC EP \_</span><span class="sxs-lookup"><span data-stu-id="d5e37-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="d5e37-106">Le type de données de **\_ \_ \_ descripteur INQ EP RPC** déclare un handle pour un contexte de recherche.</span><span class="sxs-lookup"><span data-stu-id="d5e37-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="d5e37-107">Les applications RPC l’utilisent pour afficher les informations d’adresse de serveur stockées dans le mappage de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d5e37-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="d5e37-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5e37-108">Requirements</span></span>



| <span data-ttu-id="d5e37-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5e37-109">Requirement</span></span> | <span data-ttu-id="d5e37-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e37-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e37-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5e37-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e37-112">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5e37-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d5e37-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5e37-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e37-114">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5e37-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="d5e37-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5e37-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e37-116"><dt>Rpcasync. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5e37-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e37-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5e37-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e37-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="d5e37-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="d5e37-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="d5e37-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="d5e37-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="d5e37-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





