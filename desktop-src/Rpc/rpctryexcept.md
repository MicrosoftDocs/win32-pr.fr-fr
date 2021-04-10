---
title: RpcTryExcept (RPC. h)
description: L’instruction RpcTryExcept fournit une gestion structurée des exceptions pour les applications RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104377"
---
# <a name="rpctryexcept"></a><span data-ttu-id="e2670-104">RpcTryExcept</span><span class="sxs-lookup"><span data-stu-id="e2670-104">RpcTryExcept</span></span>

<span data-ttu-id="e2670-105">L’instruction **RpcTryExcept** fournit une gestion structurée des exceptions pour les applications RPC.</span><span class="sxs-lookup"><span data-stu-id="e2670-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="e2670-106">Si l’une des instructions de programme dans le **RpcTryExcept** provoque une exception, les instructions du bloc de code [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="e2670-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="e2670-107">Toutes les instructions **RpcTryExcept** doivent être terminées par l’instruction [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="e2670-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="e2670-108">Pour plus d’informations, consultez [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="e2670-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="e2670-109">**Windows Vista et les versions ultérieures de Windows :**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) est recommandé pour la gestion structurée des exceptions pour les exceptions les plus courantes comme alternative aux filtres personnalisés avec [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="e2670-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2670-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2670-110">Requirements</span></span>



| <span data-ttu-id="e2670-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2670-111">Requirement</span></span> | <span data-ttu-id="e2670-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2670-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2670-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2670-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e2670-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2670-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e2670-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2670-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e2670-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2670-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2670-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2670-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2670-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2670-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2670-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2670-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2670-120">**RpcExcept**</span><span class="sxs-lookup"><span data-stu-id="e2670-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="e2670-121">**RpcExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="e2670-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="e2670-122">**RpcTryFinally**</span><span class="sxs-lookup"><span data-stu-id="e2670-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

