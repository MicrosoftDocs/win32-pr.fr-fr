---
title: attribut de message
description: L’attribut \ message \ indique que l’appel de procédure distante doit être traité comme un message du client au serveur.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL (attribut de message)
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463055"
---
# <a name="message-attribute"></a><span data-ttu-id="d282d-104">attribut de message</span><span class="sxs-lookup"><span data-stu-id="d282d-104">message attribute</span></span>

<span data-ttu-id="d282d-105">L’attribut de **\[ message \]** indique que l’appel de procédure distante doit être traité comme un message du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="d282d-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="d282d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d282d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d282d-107">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d282d-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d282d-108">Autres attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="d282d-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="d282d-109">Seuls les **\[** attributs [**local**](local.md) **\]** , **\[** [**nocode**](nocode.md) **\]** , **\[** [**code**](code.md)**\]** et **\[** [**optimize**](optimize.md) **\]** peuvent être utilisés avec l’attribut de **\[ message \]** .</span><span class="sxs-lookup"><span data-stu-id="d282d-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d282d-110">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="d282d-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d282d-111">Nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d282d-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d282d-112">*facultatif-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="d282d-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d282d-113">Zéro, un ou plusieurs attributs MIDL qui seront appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="d282d-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d282d-114">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="d282d-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d282d-115">Nom du paramètre tel que défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d282d-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d282d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d282d-116">Remarks</span></span>

<span data-ttu-id="d282d-117">En tant que messages du client, les appels de procédure distante avec l’attribut de **\[ message \]** sont remis au serveur de façon asynchrone via le transport [**ncadg \_ MQ**](ncadg-mq.md) Message-Queuing.</span><span class="sxs-lookup"><span data-stu-id="d282d-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="d282d-118">Vous pouvez indiquer une messagerie en mode synchrone en spécifiant le protocole de transport **ncadg \_ MQ** sans utiliser l’attribut de **\[ \] message** .</span><span class="sxs-lookup"><span data-stu-id="d282d-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="d282d-119">En spécifiant une messagerie en mode asynchrone, l’attribut de **\[ message \]** permet au client d’effectuer l’appel de procédure distante et de retourner immédiatement, même lorsque l’application serveur ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="d282d-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="d282d-120">Si le serveur cible n’est pas disponible, l’appel est stocké jusqu’à ce que le serveur soit disponible.</span><span class="sxs-lookup"><span data-stu-id="d282d-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="d282d-121">En outre, la messagerie en mode asynchrone vous permet de contrôler les propriétés de file d’attente de messages de la file d’attente de réception pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="d282d-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="d282d-122">Consultez [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) pour plus d’informations sur la sélection de la qualité de service, la priorité d’appel et la durée de vie des appels pour le processus serveur.</span><span class="sxs-lookup"><span data-stu-id="d282d-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="d282d-123">Les restrictions suivantes s’appliquent également à l’attribut de **\[ message \]** :</span><span class="sxs-lookup"><span data-stu-id="d282d-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="d282d-124">Microsoft Message Queuing doit être implémenté dans les systèmes client et serveur et les systèmes doivent être visibles les uns avec les autres, comme déterminé par l’étendue de l’installation de la file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="d282d-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="d282d-125">La liaison doit utiliser des points de terminaison connus et le protocole de transport [**\_ MQ ncadg**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="d282d-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="d282d-126">La fonction ne peut pas contenir de paramètres de sortie ou de type de retour autre que [**void**](void.md).</span><span class="sxs-lookup"><span data-stu-id="d282d-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="d282d-127">Notez que la dernière restriction rend l’attribut de **\[ message \]** inapproprié pour les méthodes d’interface com (objet), à l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="d282d-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="d282d-128">La prochaine version de MIDL permettra aux fonctions de **\[ message \]** de retourner l’état d’erreur \_ \_ t ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d282d-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="d282d-129">Toute interface contenant au moins un appel de **\[ \] message** doit être inscrite en appelant [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) avant d’appeler [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span><span class="sxs-lookup"><span data-stu-id="d282d-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="d282d-130">Dans le cas contraire, les appels qui étaient en attente sur la file d’attente du serveur sont lus avant l’inscription de l’interface et les appels échouent.</span><span class="sxs-lookup"><span data-stu-id="d282d-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="d282d-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="d282d-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="d282d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d282d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d282d-133">**code**</span><span class="sxs-lookup"><span data-stu-id="d282d-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="d282d-134">**localisé**</span><span class="sxs-lookup"><span data-stu-id="d282d-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="d282d-135">**ncadg \_ MQ**</span><span class="sxs-lookup"><span data-stu-id="d282d-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="d282d-136">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="d282d-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="d282d-137">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="d282d-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="d282d-138">Message Queuing RPC</span><span class="sxs-lookup"><span data-stu-id="d282d-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="d282d-139">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="d282d-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="d282d-140">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="d282d-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="d282d-141">**void**</span><span class="sxs-lookup"><span data-stu-id="d282d-141">**void**</span></span>](void.md)
</dt> </dl>

 

 