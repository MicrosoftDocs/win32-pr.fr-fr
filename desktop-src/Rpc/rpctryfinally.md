---
title: RpcTryFinally (RPC. h)
description: L’instruction RpcTryFinally fournit une gestion structurée des arrêts.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RpcTryFinally RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465834"
---
# <a name="rpctryfinally"></a><span data-ttu-id="581cd-104">RpcTryFinally</span><span class="sxs-lookup"><span data-stu-id="581cd-104">RpcTryFinally</span></span>

<span data-ttu-id="581cd-105">L’instruction **RpcTryFinally** fournit une gestion structurée des arrêts.</span><span class="sxs-lookup"><span data-stu-id="581cd-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="581cd-106">Une exception se produit pendant les instructions d’exécution du bloc de code associé à l’instruction **RpcTryFinally** , les instructions du bloc de code associé à l’instruction [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="581cd-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="581cd-107">Toutes les instructions **RpcTryFinally** doivent se terminer par une instruction [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="581cd-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="581cd-108">Pour plus d’informations, consultez [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="581cd-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="581cd-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="581cd-109">Requirements</span></span>



| <span data-ttu-id="581cd-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="581cd-110">Requirement</span></span> | <span data-ttu-id="581cd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="581cd-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="581cd-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="581cd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="581cd-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="581cd-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="581cd-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="581cd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="581cd-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="581cd-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="581cd-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="581cd-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="581cd-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="581cd-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581cd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="581cd-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="581cd-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="581cd-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="581cd-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="581cd-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

