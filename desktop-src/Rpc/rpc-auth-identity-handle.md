---
title: RPC_AUTH_IDENTITY_HANDLE (rpcdce. h)
description: Le type de données du handle de l' \_ identité d’authentification RPC \_ \_ déclare un handle qui pointe vers une structure contenant les informations d’identification d’authentification et d’autorisation du client spécifiées pour les appels de procédure distante.
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106387"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="35961-104">\_handle d' \_ identité d’authentification RPC \_</span><span class="sxs-lookup"><span data-stu-id="35961-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="35961-105">Le type de données du handle de l' **\_ identité d’authentification \_ \_ RPC** déclare un handle qui pointe vers une structure contenant les informations d’identification d’authentification et d’autorisation du client spécifiées pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="35961-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="35961-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35961-106">Requirements</span></span>



| <span data-ttu-id="35961-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35961-107">Requirement</span></span> | <span data-ttu-id="35961-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="35961-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35961-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35961-109">Minimum supported client</span></span><br/> | <span data-ttu-id="35961-110">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35961-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35961-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35961-111">Minimum supported server</span></span><br/> | <span data-ttu-id="35961-112">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35961-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="35961-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="35961-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="35961-114"><dt>Rpcdce. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35961-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35961-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35961-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35961-116">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="35961-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="35961-117">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="35961-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





