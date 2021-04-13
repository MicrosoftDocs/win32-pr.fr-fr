---
title: RPC_NS_HANDLE (Rpcnsi. h)
description: Le \_ \_ descripteur NS RPC de type de données définit un handle de service de nom.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509202"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="47c13-104">\_descripteur NS RPC \_</span><span class="sxs-lookup"><span data-stu-id="47c13-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="47c13-105">Le **\_ \_ descripteur NS RPC** de type de données définit un handle de service de nom.</span><span class="sxs-lookup"><span data-stu-id="47c13-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="47c13-106">Notes</span><span class="sxs-lookup"><span data-stu-id="47c13-106">Remarks</span></span>

<span data-ttu-id="47c13-107">Un descripteur de nom-service est une variable opaque contenant les informations que la bibliothèque Runtime RPC utilise pour retourner les données RPC suivantes de la base de données nom-service :</span><span class="sxs-lookup"><span data-stu-id="47c13-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="47c13-108">Handles de liaison de serveur</span><span class="sxs-lookup"><span data-stu-id="47c13-108">Server-binding handles</span></span>
-   <span data-ttu-id="47c13-109">UUID des ressources offertes par les membres du profil de serveur</span><span class="sxs-lookup"><span data-stu-id="47c13-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="47c13-110">Membres de groupe</span><span class="sxs-lookup"><span data-stu-id="47c13-110">Group members</span></span>

<span data-ttu-id="47c13-111">La portée d’un handle de service de nom provient d’une routine « Begin » dans la routine « Done » correspondante.</span><span class="sxs-lookup"><span data-stu-id="47c13-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="47c13-112">Les applications sont responsables du contrôle de l’accès concurrentiel des handles de service de nom sur les threads.</span><span class="sxs-lookup"><span data-stu-id="47c13-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c13-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47c13-113">Requirements</span></span>



| <span data-ttu-id="47c13-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47c13-114">Requirement</span></span> | <span data-ttu-id="47c13-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47c13-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c13-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47c13-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47c13-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="47c13-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47c13-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47c13-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="47c13-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="47c13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c13-121"><dt>Rpcnsi. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47c13-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c13-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47c13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c13-123">**RpcNsBindingImportBegin**</span><span class="sxs-lookup"><span data-stu-id="47c13-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="47c13-124">**RpcNsBindingImportDone**</span><span class="sxs-lookup"><span data-stu-id="47c13-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="47c13-125">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="47c13-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="47c13-126">**RpcNsBindingLookupBegin**</span><span class="sxs-lookup"><span data-stu-id="47c13-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="47c13-127">**RpcNsBindingLookupDone**</span><span class="sxs-lookup"><span data-stu-id="47c13-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="47c13-128">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="47c13-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





