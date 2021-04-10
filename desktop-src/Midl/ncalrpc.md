---
title: attribut Ncalrpc
description: Le mot clé Ncalrpc identifie la communication interprocessus locale comme la famille de protocoles pour le point de terminaison. Ce mot clé est l’un des noms de famille de protocoles valides qui doivent être utilisés avec l’attribut \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- MIDL de l’attribut Ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940957"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="5ddca-105">attribut Ncalrpc</span><span class="sxs-lookup"><span data-stu-id="5ddca-105">ncalrpc attribute</span></span>

<span data-ttu-id="5ddca-106">Le mot clé **Ncalrpc** identifie la communication interprocessus locale comme la famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5ddca-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="5ddca-107">Ce mot clé est l’un des noms de famille de protocoles valides qui doivent être utilisés avec l’attribut de **\[** [**point de terminaison**](endpoint.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ddca-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="5ddca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ddca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ddca-109">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="5ddca-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddca-110">Chaîne de caractères qui spécifie le port de communication (une application, un service ou une instance d’un service) qu’un client utilise pour effectuer des appels interprocessus à un serveur.</span><span class="sxs-lookup"><span data-stu-id="5ddca-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="5ddca-111">La chaîne peut contenir jusqu’à 53 caractères et ne doit pas contenir de barre oblique inverse ( \) caractères).</span><span class="sxs-lookup"><span data-stu-id="5ddca-111">The string can contain up to 53 characters and should not contain any backslash (\) characters.</span></span> <span data-ttu-id="5ddca-112">Le nom d’ordinateur ne doit pas être utilisé avec le mot clé **Ncalrpc** .</span><span class="sxs-lookup"><span data-stu-id="5ddca-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ddca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5ddca-113">Remarks</span></span>

<span data-ttu-id="5ddca-114">La syntaxe de la chaîne de port de communication interprocessus locale, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="5ddca-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="5ddca-115">Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="5ddca-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="5ddca-116">Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5ddca-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="5ddca-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5ddca-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="5ddca-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ddca-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddca-119">**poste**</span><span class="sxs-lookup"><span data-stu-id="5ddca-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="5ddca-120">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5ddca-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5ddca-121">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="5ddca-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-122">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="5ddca-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-123">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="5ddca-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-124">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="5ddca-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="5ddca-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="5ddca-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="5ddca-126">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="5ddca-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="5ddca-127">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="5ddca-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-128">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="5ddca-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="5ddca-129">**ncacn \_ réseaux virtuels \_ spp**</span><span class="sxs-lookup"><span data-stu-id="5ddca-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-130">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="5ddca-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="5ddca-131">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="5ddca-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="5ddca-132">Liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="5ddca-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 