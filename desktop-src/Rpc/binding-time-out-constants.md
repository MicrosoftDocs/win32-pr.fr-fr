---
title: Constantes de délai d’attente de liaison (rpcdce. h)
description: La bibliothèque RPC utilise les constantes de délai d’expiration de liaison pour spécifier la durée relative à consacrer à l’établissement d’une liaison au serveur avant d’abandonner.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512564"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="9b794-103">Constantes de délai d’attente de liaison</span><span class="sxs-lookup"><span data-stu-id="9b794-103">Binding Time-out Constants</span></span>

<span data-ttu-id="9b794-104">La bibliothèque RPC utilise les constantes de délai d’expiration de liaison pour spécifier la durée relative à consacrer à l’établissement d’une liaison au serveur avant d’abandonner.</span><span class="sxs-lookup"><span data-stu-id="9b794-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="9b794-105">Le délai d’attente peut être activé à l’aide d’un appel à la fonction [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) .</span><span class="sxs-lookup"><span data-stu-id="9b794-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="9b794-106">La liste suivante contient les valeurs de délai d’attente valides.</span><span class="sxs-lookup"><span data-stu-id="9b794-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="9b794-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="9b794-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="9b794-108">Description</span><span class="sxs-lookup"><span data-stu-id="9b794-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="9b794-109"><dt>**RPC \_ \_Expiration de liaison C \_ infinie \_**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="9b794-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="9b794-110">La tentative d’établissement de communications est définitive.</span><span class="sxs-lookup"><span data-stu-id="9b794-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="9b794-111"><dt>**RPC \_ \_ \_ \_ Délai d’expiration minimal de liaison C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b794-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="9b794-112">Tente la durée minimale d’utilisation du protocole réseau.</span><span class="sxs-lookup"><span data-stu-id="9b794-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="9b794-113">Cette valeur favorise le temps de réponse par rapport à l’exactitude pour déterminer si le serveur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9b794-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="9b794-114"><dt>**RPC \_ \_ \_ \_ Délai d’attente de liaison C par défaut**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9b794-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="9b794-115">Tente une durée moyenne pour le protocole réseau utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b794-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="9b794-116">Cette valeur donne l’exactitude de déterminer si un serveur est en cours d’exécution et donne un temps de réponse égal au poids.</span><span class="sxs-lookup"><span data-stu-id="9b794-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="9b794-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b794-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="9b794-118"><dt>**RPC \_ \_ \_ \_ Délai maximal de liaison C**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9b794-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="9b794-119">Tente la durée la plus longue pour le protocole réseau utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b794-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="9b794-120">Cette valeur favorise l’exactitude pour déterminer si un serveur s’exécute sur le temps de réponse.</span><span class="sxs-lookup"><span data-stu-id="9b794-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="9b794-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9b794-121">Remarks</span></span>

<span data-ttu-id="9b794-122">Les valeurs du tableau précédent ne sont pas en secondes.</span><span class="sxs-lookup"><span data-stu-id="9b794-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="9b794-123">Ces valeurs représentent une durée relative sur une échelle de zéro à 10.</span><span class="sxs-lookup"><span data-stu-id="9b794-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="9b794-124">Pour plus d’informations sur l’évitement des retards de communication, consultez la rubrique prévention des blocages côté client.</span><span class="sxs-lookup"><span data-stu-id="9b794-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b794-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b794-125">Requirements</span></span>



| <span data-ttu-id="9b794-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b794-126">Requirement</span></span> | <span data-ttu-id="9b794-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b794-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b794-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b794-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b794-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b794-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b794-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b794-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b794-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b794-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b794-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b794-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b794-133"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b794-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





