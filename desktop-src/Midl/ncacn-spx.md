---
title: attribut ncacn_spx
description: Le \_ mot clé ncacn SPX identifie SPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106518005"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="825c2-105">\_attribut ncacn SPX</span><span class="sxs-lookup"><span data-stu-id="825c2-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="825c2-106">Le mot clé **ncacn \_ SPX** identifie SPX comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="825c2-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="825c2-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="825c2-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="825c2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="825c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825c2-109">*adresse de lien*</span><span class="sxs-lookup"><span data-stu-id="825c2-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="825c2-110">Spécifie le serveur hôte.</span><span class="sxs-lookup"><span data-stu-id="825c2-110">Specifies the host server.</span></span> <span data-ttu-id="825c2-111">Il peut s’agir d’une chaîne de caractères (nom du serveur) ou d’un nombre hexadécimal à 20 chiffres qui se compose de l’adresse réseau du serveur hôte (8 chiffres) concaténée avec l’adresse du nœud (12 chiffres).</span><span class="sxs-lookup"><span data-stu-id="825c2-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="825c2-112">Pour obtenir des instructions sur l’obtention de l’adresse réseau et de l’adresse du nœud, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="825c2-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="825c2-113">Une chaîne **null** spécifie l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="825c2-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="825c2-114">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="825c2-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="825c2-115">Spécifie un nombre 16 bits facultatif qui représente l’adresse du Socket.</span><span class="sxs-lookup"><span data-stu-id="825c2-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="825c2-116">Les valeurs peuvent être comprises entre 1 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="825c2-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="825c2-117">Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.</span><span class="sxs-lookup"><span data-stu-id="825c2-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="825c2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="825c2-118">Remarks</span></span>

<span data-ttu-id="825c2-119">Lorsque vous utilisez le transport **ncacn \_ SPX** , le nom du serveur est exactement le même que le nom Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="825c2-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="825c2-120">Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell.</span><span class="sxs-lookup"><span data-stu-id="825c2-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="825c2-121">Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec le transport **ncacn \_ SPX** .</span><span class="sxs-lookup"><span data-stu-id="825c2-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="825c2-122">Voici une liste partielle des caractères interdits dans les noms de serveurs Novell :</span><span class="sxs-lookup"><span data-stu-id="825c2-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="825c2-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="825c2-123">" \* + .</span></span> <span data-ttu-id="825c2-124">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="825c2-124">/ : ; < = > ?</span></span> <span data-ttu-id="825c2-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="825c2-125">\[ \] \\ \|</span></span>

<span data-ttu-id="825c2-126">Le transport **ncacn \_ SPX** n’est pas pris en charge par la version de NWLink fournie avec MS client 3,0.</span><span class="sxs-lookup"><span data-stu-id="825c2-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="825c2-127">les applications clientes Windows 16 bits qui utilisent le transport **ncacn \_ SPX** requièrent que le fichier Nwipxspx.dll être installé pour s’exécuter sous le sous-système wow.</span><span class="sxs-lookup"><span data-stu-id="825c2-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="825c2-128">Contactez Novell pour obtenir ce fichier.</span><span class="sxs-lookup"><span data-stu-id="825c2-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="825c2-129">Pour obtenir les adresses du réseau et du nœud, utilisez l’utilitaire **ComCheck** de Novell ou l’API définie par Novell **IPXGetInternetAddress**.</span><span class="sxs-lookup"><span data-stu-id="825c2-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="825c2-130">Sur Windows, vous pouvez également obtenir ces adresses à l’aide de la commande **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="825c2-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="825c2-131">La syntaxe de la chaîne de port de transport SPX, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="825c2-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="825c2-132">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="825c2-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="825c2-133">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="825c2-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="825c2-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="825c2-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="825c2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="825c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825c2-136">**poste**</span><span class="sxs-lookup"><span data-stu-id="825c2-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="825c2-137">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="825c2-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="825c2-138">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="825c2-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="825c2-139">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="825c2-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="825c2-140">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="825c2-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="825c2-141">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="825c2-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="825c2-142">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="825c2-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="825c2-143">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="825c2-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="825c2-144">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="825c2-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="825c2-145">**ncacn \_ réseaux virtuels \_ spp**</span><span class="sxs-lookup"><span data-stu-id="825c2-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="825c2-146">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="825c2-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="825c2-147">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="825c2-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="825c2-148">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="825c2-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="825c2-149">liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="825c2-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 