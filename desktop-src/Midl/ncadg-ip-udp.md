---
title: attribut ncadg_ip_udp
description: Le \_ \_ mot clé IP UDP ncadg identifie la version de datagramme de TCP/IP comme famille de protocole pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101529"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="527fb-105">\_ \_ attribut UDP IP ncadg</span><span class="sxs-lookup"><span data-stu-id="527fb-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="527fb-106">Le mot clé **\_ IP \_ UDP ncadg** identifie la version de datagramme de TCP/IP comme famille de protocole pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="527fb-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="527fb-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="527fb-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="527fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="527fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527fb-109">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="527fb-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="527fb-110">Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="527fb-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="527fb-111">Le nom est une chaîne de caractères et peut être un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="527fb-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="527fb-112">L’adresse Internet est une notation d’adresse Internet courante.</span><span class="sxs-lookup"><span data-stu-id="527fb-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="527fb-113">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="527fb-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="527fb-114">Spécifie un nombre 16 bits facultatif.</span><span class="sxs-lookup"><span data-stu-id="527fb-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="527fb-115">Les valeurs inférieures à 1024 sont généralement réservées.</span><span class="sxs-lookup"><span data-stu-id="527fb-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="527fb-116">Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.</span><span class="sxs-lookup"><span data-stu-id="527fb-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="527fb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="527fb-117">Remarks</span></span>

<span data-ttu-id="527fb-118">Les restrictions suivantes s’appliquent aux protocoles de datagramme, [**ncadg \_ IPX**](ncadg-ipx.md) et **ncadg \_ IP \_ UDP**:</span><span class="sxs-lookup"><span data-stu-id="527fb-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="527fb-119">Ils ne prennent pas en charge les rappels.</span><span class="sxs-lookup"><span data-stu-id="527fb-119">They do not support callbacks.</span></span> <span data-ttu-id="527fb-120">Toutes les fonctions qui utilisent l' **\[** attribut [**callback**](callback.md) **\]** échouent.</span><span class="sxs-lookup"><span data-stu-id="527fb-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="527fb-121">Ils ne prennent pas en charge l’utilisation du constructeur de type [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="527fb-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="527fb-122">La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="527fb-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="527fb-123">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="527fb-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="527fb-124">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="527fb-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="527fb-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="527fb-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="527fb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="527fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527fb-127">**poste**</span><span class="sxs-lookup"><span data-stu-id="527fb-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="527fb-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="527fb-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="527fb-129">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="527fb-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="527fb-130">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="527fb-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="527fb-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="527fb-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="527fb-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="527fb-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="527fb-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="527fb-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="527fb-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="527fb-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="527fb-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="527fb-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="527fb-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="527fb-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="527fb-137">**ncacn \_ réseaux virtuels \_ spp**</span><span class="sxs-lookup"><span data-stu-id="527fb-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="527fb-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="527fb-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="527fb-139">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="527fb-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="527fb-140">Liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="527fb-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 