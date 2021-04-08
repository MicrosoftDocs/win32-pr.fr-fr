---
title: Constantes d’autorisation (RpcDce. h)
description: Définit ce que le serveur autorise.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743709"
---
# <a name="authorization-constants"></a><span data-ttu-id="a51c7-103">Constantes d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a51c7-103">Authorization Constants</span></span>

<span data-ttu-id="a51c7-104">Définit ce que le serveur autorise.</span><span class="sxs-lookup"><span data-stu-id="a51c7-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="a51c7-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="a51c7-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="a51c7-106">Description</span><span class="sxs-lookup"><span data-stu-id="a51c7-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="a51c7-107"><dt>**RPC \_ C \_ authnt \_ aucun**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a51c7-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="a51c7-108">Le serveur n’effectue aucune autorisation.</span><span class="sxs-lookup"><span data-stu-id="a51c7-108">The server performs no authorization.</span></span> <span data-ttu-id="a51c7-109">Actuellement, RPC \_ c Authn \_ \_ WinNT, RPC \_ c \_ Authn \_ GSS \_ Schannel et RPC \_ c \_ Authn \_ GSS \_ Kerberos utilisent uniquement RPC \_ c \_ auth \_ aucun.</span><span class="sxs-lookup"><span data-stu-id="a51c7-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="a51c7-110"><dt>**RPC \_ \_ \_ Nom**</dt> d’autorisation C <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a51c7-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="a51c7-111">Le serveur effectue une autorisation basée sur le nom principal du client.</span><span class="sxs-lookup"><span data-stu-id="a51c7-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="a51c7-112"><dt>**RPC \_ C \_ authz \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a51c7-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="a51c7-113">Le serveur effectue une vérification d’autorisation à l’aide des informations de certificat PAC (Privileged attribute Certificate) du client, qui sont envoyées au serveur avec chaque appel de procédure distante effectué à l’aide du handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="a51c7-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="a51c7-114">En règle générale, l’accès est vérifié par rapport aux listes de contrôle d’accès (ACL) DCE.</span><span class="sxs-lookup"><span data-stu-id="a51c7-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="a51c7-115"><dt>**RPC \_ C \_ auth \_ par défaut**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="a51c7-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="a51c7-116">DCOM peut choisir le niveau d’autorisation à l’aide de son algorithme de négociation permanente de sécurité normal.</span><span class="sxs-lookup"><span data-stu-id="a51c7-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="a51c7-117">Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="a51c7-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="a51c7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a51c7-118">Remarks</span></span>

<span data-ttu-id="a51c7-119">Ces constantes sont utilisées par les méthodes de l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="a51c7-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="a51c7-120">Ils sont utilisés dans la structure du [**\_ \_ service d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , qui est récupérée par la fonction [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .</span><span class="sxs-lookup"><span data-stu-id="a51c7-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="a51c7-121">Ils sont également utilisés dans la structure des [**\_ \_ informations d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , qui est, à son tour, membre de la structure de la [**\_ \_ liste d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) .</span><span class="sxs-lookup"><span data-stu-id="a51c7-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="a51c7-122">Cette structure, qui est une liste de services d’authentification, les services d’autorisation qu’elles exécutent et les informations d’authentification de chaque service, est passée à la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et à la méthode [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .</span><span class="sxs-lookup"><span data-stu-id="a51c7-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a51c7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a51c7-123">Requirements</span></span>



| <span data-ttu-id="a51c7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a51c7-124">Requirement</span></span> | <span data-ttu-id="a51c7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a51c7-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a51c7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a51c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a51c7-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a51c7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a51c7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a51c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a51c7-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a51c7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a51c7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a51c7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a51c7-131"><dt>RpcDce. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51c7-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a51c7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a51c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51c7-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="a51c7-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="a51c7-134">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="a51c7-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="a51c7-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="a51c7-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="a51c7-136">**\_informations d’authentification exclusives \_**</span><span class="sxs-lookup"><span data-stu-id="a51c7-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="a51c7-137">**\_service d’authentification unique \_**</span><span class="sxs-lookup"><span data-stu-id="a51c7-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

