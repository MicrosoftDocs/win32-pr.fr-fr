---
title: Constantes Authentication-Level (rpcdce. h)
description: Les constantes de niveau d’authentification représentent les niveaux d’authentification passés à différentes fonctions d’exécution.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509209"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="e314e-103">Constantes au niveau de l’authentification</span><span class="sxs-lookup"><span data-stu-id="e314e-103">Authentication-Level Constants</span></span>

<span data-ttu-id="e314e-104">Les constantes de niveau d’authentification représentent les niveaux d’authentification passés à différentes fonctions d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e314e-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="e314e-105">Ces niveaux sont répertoriés par ordre d’authentification accru.</span><span class="sxs-lookup"><span data-stu-id="e314e-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="e314e-106">Chaque nouveau niveau ajoute à l’authentification fournie par le niveau précédent.</span><span class="sxs-lookup"><span data-stu-id="e314e-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="e314e-107">Si la bibliothèque Runtime RPC ne prend pas en charge le niveau spécifié, elle est automatiquement mise à niveau vers le niveau immédiatement supérieur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e314e-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="e314e-108">Constante</span><span class="sxs-lookup"><span data-stu-id="e314e-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="e314e-109">Description</span><span class="sxs-lookup"><span data-stu-id="e314e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="e314e-110"><dt>**\_ \_ \_ valeur par défaut du niveau d’authentification RPC C \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="e314e-111">Utilise le niveau d'authentification par défaut pour le service d'authentification spécifié.</span><span class="sxs-lookup"><span data-stu-id="e314e-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="e314e-112"><dt>**RPC \_ C \_ Authn \_ niveau \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="e314e-113">N’effectue aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="e314e-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="e314e-114"><dt>**\_ \_ \_ connexion au niveau AUTHn C RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="e314e-115">Effectue une authentification uniquement lorsque le client établit une relation avec un serveur.</span><span class="sxs-lookup"><span data-stu-id="e314e-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="e314e-116"><dt>**\_ \_ \_ appel au niveau d’authentification RPC C \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="e314e-117">Authentifie uniquement au début de chaque appel de procédure distante lorsque le serveur reçoit la demande.</span><span class="sxs-lookup"><span data-stu-id="e314e-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="e314e-118">Ne s’applique pas aux appels de procédure distante effectués à l’aide des séquences de protocole basées sur la connexion (celles qui commencent par le préfixe « ncacn »).</span><span class="sxs-lookup"><span data-stu-id="e314e-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="e314e-119">Si la séquence de protocole dans un handle de liaison est une séquence de protocole basée sur la connexion et que vous spécifiez ce niveau, cette routine utilise à la place la \_ \_ constante PKT du niveau d’authentification RPC C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e314e-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="e314e-120"><dt>**protocole d’authentification de l' \_ authentification RPC C \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="e314e-121">Authentifie uniquement que toutes les données reçues proviennent du client attendu.</span><span class="sxs-lookup"><span data-stu-id="e314e-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="e314e-122">Ne valide pas les données elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e314e-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="e314e-123"><dt>**\_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="e314e-124">Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="e314e-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="e314e-125"><dt>**\_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="e314e-126">Comprend tous les niveaux précédents et garantit que les données en texte clair ne peuvent être consultées que par l’expéditeur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="e314e-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="e314e-127">Dans le cas local, cela implique l’utilisation d’un canal sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e314e-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="e314e-128">Dans le cas distant, cela implique le chiffrement de la valeur d’argument de chaque appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e314e-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="e314e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="e314e-129">Remarks</span></span>

<span data-ttu-id="e314e-130">Quelle que soit la valeur spécifiée par la constante, **Ncalrpc** utilise toujours le niveau de confidentialité de la \_ déclaration d’authentification RPC C \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e314e-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e314e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e314e-131">Requirements</span></span>



| <span data-ttu-id="e314e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e314e-132">Requirement</span></span> | <span data-ttu-id="e314e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e314e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e314e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e314e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e314e-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e314e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e314e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e314e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e314e-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e314e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e314e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="e314e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e314e-139"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="e314e-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e314e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e314e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e314e-141">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e314e-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="e314e-142">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e314e-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="e314e-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="e314e-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="e314e-144">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="e314e-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="e314e-145">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="e314e-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="e314e-146">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e314e-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="e314e-147">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e314e-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





