---
title: Constantes de niveau d’authentification (rpcdce. h)
description: Ces valeurs spécifient un niveau d’authentification, qui indique la quantité d’authentification fournie pour aider à protéger l’intégrité des données. Chaque niveau comprend la protection fournie par les niveaux précédents.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
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
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519065"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="0fe11-104">Constantes de niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="0fe11-104">Authentication Level Constants</span></span>

<span data-ttu-id="0fe11-105">Ces valeurs spécifient un niveau d’authentification, qui indique la quantité d’authentification fournie pour aider à protéger l’intégrité des données.</span><span class="sxs-lookup"><span data-stu-id="0fe11-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="0fe11-106">Chaque niveau comprend la protection fournie par les niveaux précédents.</span><span class="sxs-lookup"><span data-stu-id="0fe11-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="0fe11-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="0fe11-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="0fe11-108">Description</span><span class="sxs-lookup"><span data-stu-id="0fe11-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="0fe11-109"><dt>**RPC \_ \_ \_ \_ Valeur par défaut du niveau d’authentification C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="0fe11-110">Indique à DCOM de choisir le niveau d’authentification à l’aide de son algorithme de négociation permanente de sécurité normal.</span><span class="sxs-lookup"><span data-stu-id="0fe11-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="0fe11-111">Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="0fe11-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="0fe11-112"><dt>**RPC \_ C \_ Authn \_ niveau \_ aucun**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="0fe11-113">N’effectue aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="0fe11-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="0fe11-114"><dt>**RPC \_ \_ \_ \_ Connexion au niveau de l’authentification C**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="0fe11-115">Authentifie les informations d’identification du client uniquement lorsque le client établit une relation avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="0fe11-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="0fe11-116">Les transports de datagrammes utilisent toujours l' \_ authentification PKT au niveau de l’authentification RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0fe11-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="0fe11-117"><dt>**RPC \_ \_ \_ \_ Appel de niveau Authn C**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="0fe11-118">Authentifie uniquement au début de chaque appel de procédure distante lorsque le serveur reçoit la demande.</span><span class="sxs-lookup"><span data-stu-id="0fe11-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="0fe11-119">Les transports de datagrammes utilisent à la place la procédure d' \_ authentification par authentification C RPC \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0fe11-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="0fe11-120"><dt>**RPC \_ C \_ Authn \_ niveau \_ d’authentification PKT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="0fe11-121">Authentifie que toutes les données reçues proviennent du client attendu.</span><span class="sxs-lookup"><span data-stu-id="0fe11-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="0fe11-122"><dt>**RPC \_ \_ \_ \_ \_ Intégrité PKT de niveau d’authentification C**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="0fe11-123">Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="0fe11-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="0fe11-124"><dt>**RPC \_ C Authentication \_ \_ PKT niveau de \_ \_ confidentialité**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="0fe11-125">Authentifie tous les niveaux précédents et chiffre la valeur d’argument de chaque appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="0fe11-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="0fe11-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fe11-126">Requirements</span></span>



| <span data-ttu-id="0fe11-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fe11-127">Requirement</span></span> | <span data-ttu-id="0fe11-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fe11-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe11-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fe11-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe11-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0fe11-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fe11-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fe11-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe11-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0fe11-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fe11-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fe11-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fe11-134"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fe11-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





