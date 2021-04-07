---
title: attribut ncacn_np
description: Le \_ mot clé ncacn NP identifie les canaux nommés comme famille de protocoles pour le point de terminaison.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726733"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="9298b-104">\_attribut ncacn NP</span><span class="sxs-lookup"><span data-stu-id="9298b-104">ncacn\_np attribute</span></span>

<span data-ttu-id="9298b-105">Le mot clé **ncacn \_ NP** identifie les canaux nommés comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9298b-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="9298b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9298b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9298b-107">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="9298b-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9298b-108">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9298b-108">Optional.</span></span> <span data-ttu-id="9298b-109">Spécifie le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="9298b-109">Specifies the name of the server.</span></span> <span data-ttu-id="9298b-110">Les barres obliques inverses sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="9298b-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="9298b-111">*nom du canal*</span><span class="sxs-lookup"><span data-stu-id="9298b-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9298b-112">Spécifie un nom de canal valide.</span><span class="sxs-lookup"><span data-stu-id="9298b-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="9298b-113">Un nom de canal valide est une chaîne contenant des identificateurs séparés par des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="9298b-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="9298b-114">Le premier identificateur doit être [**pipe**](pipe.md).</span><span class="sxs-lookup"><span data-stu-id="9298b-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="9298b-115">Chaque identificateur doit être séparé par deux barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="9298b-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9298b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9298b-116">Remarks</span></span>

<span data-ttu-id="9298b-117">Un serveur crée une instance d’un canal nommé qui est ensuite disponible pour n’importe quel client.</span><span class="sxs-lookup"><span data-stu-id="9298b-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="9298b-118">Lorsqu’un client tente de se connecter, l’instance existante est associée à ce client.</span><span class="sxs-lookup"><span data-stu-id="9298b-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="9298b-119">Avant qu’un autre client puisse se connecter, le serveur doit créer une autre instance du canal nommé.</span><span class="sxs-lookup"><span data-stu-id="9298b-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="9298b-120">Si un client tente d’établir une liaison avec le serveur avant la création de la nouvelle instance, l’appel de liaison, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), peut échouer avec le message d’erreur le \_ serveur RPC S est \_ \_ trop \_ occupé.</span><span class="sxs-lookup"><span data-stu-id="9298b-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="9298b-121">Par conséquent, vous devez vous assurer que votre application cliente gère le cas où le serveur est trop occupé pour accepter une connexion.</span><span class="sxs-lookup"><span data-stu-id="9298b-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="9298b-122">Le client doit réessayer automatiquement, demander à l’utilisateur un cours d’action ou échouer correctement.</span><span class="sxs-lookup"><span data-stu-id="9298b-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="9298b-123">La syntaxe de la chaîne de port de canal nommé, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="9298b-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="9298b-124">Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="9298b-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="9298b-125">Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="9298b-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="9298b-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="9298b-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="9298b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9298b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9298b-128">**poste**</span><span class="sxs-lookup"><span data-stu-id="9298b-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="9298b-129">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="9298b-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9298b-130">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="9298b-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="9298b-131">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="9298b-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="9298b-132">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="9298b-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="9298b-133">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="9298b-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="9298b-134">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="9298b-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="9298b-135">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="9298b-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="9298b-136">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="9298b-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="9298b-137">**ncacn \_ réseaux virtuels \_ spp**</span><span class="sxs-lookup"><span data-stu-id="9298b-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="9298b-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="9298b-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="9298b-139">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="9298b-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="9298b-140">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="9298b-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="9298b-141">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="9298b-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 