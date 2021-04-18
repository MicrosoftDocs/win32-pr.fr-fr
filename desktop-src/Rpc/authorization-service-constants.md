---
title: Constantes Authorization-Service (rpcdce. h)
description: Les constantes de service d’autorisation représentent les services d’autorisation passés à différentes fonctions d’exécution.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519265"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="d9393-103">Constantes Authorization-Service</span><span class="sxs-lookup"><span data-stu-id="d9393-103">Authorization-Service Constants</span></span>

<span data-ttu-id="d9393-104">Les constantes de service d’autorisation représentent les services d’autorisation passés à différentes fonctions d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d9393-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="d9393-105">Les constantes suivantes sont des valeurs valides pour le paramètre *AuthzSvc* .</span><span class="sxs-lookup"><span data-stu-id="d9393-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="d9393-106">La plupart des applications recherchent une autorisation RPC \_ C \_ \_ insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d9393-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="d9393-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="d9393-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="d9393-108">Description</span><span class="sxs-lookup"><span data-stu-id="d9393-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="d9393-109"><dt>**RPC \_ C \_ authnt \_ aucun**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d9393-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="d9393-110">Le serveur n’effectue aucune autorisation.</span><span class="sxs-lookup"><span data-stu-id="d9393-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="d9393-111"><dt>**RPC \_ \_ \_ Nom**</dt> d’autorisation C <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d9393-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="d9393-112">Le serveur effectue une autorisation basée sur le nom principal du client.</span><span class="sxs-lookup"><span data-stu-id="d9393-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="d9393-113"><dt>**RPC \_ C \_ authz \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d9393-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="d9393-114">Le serveur effectue une vérification d’autorisation à l’aide des informations de certificat PAC (Privileged attribute Certificate) du client, qui sont envoyées au serveur avec chaque appel de procédure distante effectué à l’aide du handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="d9393-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="d9393-115">En règle générale, l’accès est vérifié par rapport aux listes de contrôle d’accès ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)) DCE.</span><span class="sxs-lookup"><span data-stu-id="d9393-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="d9393-116"><dt>**RPC \_ C \_ auth \_ par défaut**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="d9393-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="d9393-117">Le serveur utilise le service d’autorisation par défaut pour le fournisseur de services partagés actuel.</span><span class="sxs-lookup"><span data-stu-id="d9393-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="d9393-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9393-118">Requirements</span></span>



| <span data-ttu-id="d9393-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9393-119">Requirement</span></span> | <span data-ttu-id="d9393-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9393-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9393-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9393-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9393-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9393-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d9393-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9393-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9393-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9393-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d9393-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9393-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9393-126"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9393-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9393-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9393-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9393-128">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="d9393-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="d9393-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="d9393-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="d9393-130">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="d9393-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="d9393-131">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="d9393-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="d9393-132">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="d9393-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="d9393-133">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="d9393-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="d9393-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="d9393-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

