---
title: attribut ncadg_ipx
description: Le \_ mot clé IPX ncadg identifie IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725380"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="3e356-105">ncadg \_ IPX (attribut)</span><span class="sxs-lookup"><span data-stu-id="3e356-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="3e356-106">Le mot clé **\_ IPX NCADG** identifie IPX comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3e356-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="3e356-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="3e356-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="3e356-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e356-109">*adresse de lien*</span><span class="sxs-lookup"><span data-stu-id="3e356-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="3e356-110">Spécifie le serveur hôte.</span><span class="sxs-lookup"><span data-stu-id="3e356-110">Specifies the host server.</span></span> <span data-ttu-id="3e356-111">Il peut s’agir d’une chaîne de caractères (nom du serveur) ou d’un nombre hexadécimal à 20 chiffres qui se compose de l’adresse réseau du serveur hôte (8 chiffres) concaténée avec l’adresse du nœud (12 chiffres).</span><span class="sxs-lookup"><span data-stu-id="3e356-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="3e356-112">Pour obtenir des instructions sur l’obtention de l’adresse réseau et de l’adresse du nœud, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3e356-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="3e356-113">Une chaîne **null** spécifie l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3e356-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="3e356-114">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="3e356-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3e356-115">Spécifie un nombre 16 bits facultatif qui représente l’adresse du Socket.</span><span class="sxs-lookup"><span data-stu-id="3e356-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="3e356-116">Les valeurs peuvent être comprises entre 1 et 65535.</span><span class="sxs-lookup"><span data-stu-id="3e356-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="3e356-117">Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.</span><span class="sxs-lookup"><span data-stu-id="3e356-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e356-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3e356-118">Remarks</span></span>

<span data-ttu-id="3e356-119">Les restrictions suivantes s’appliquent aux protocoles de datagramme, **ncadg \_ IPX** et [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):</span><span class="sxs-lookup"><span data-stu-id="3e356-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="3e356-120">Ils ne prennent pas en charge les rappels.</span><span class="sxs-lookup"><span data-stu-id="3e356-120">They do not support callbacks.</span></span> <span data-ttu-id="3e356-121">Toutes les fonctions qui utilisent l' **\[** attribut [**callback**](callback.md) **\]** échouent.</span><span class="sxs-lookup"><span data-stu-id="3e356-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="3e356-122">Ils ne prennent pas en charge l’utilisation du constructeur de type [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="3e356-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="3e356-123">Lorsque vous utilisez le transport **ncadg \_ IPX** , le nom du serveur est exactement le même que le nom du serveur Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e356-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="3e356-124">Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell.</span><span class="sxs-lookup"><span data-stu-id="3e356-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="3e356-125">Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec le transport **\_ IPX ncadg** .</span><span class="sxs-lookup"><span data-stu-id="3e356-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="3e356-126">Voici une liste partielle des caractères interdits dans les noms de serveurs Novell :</span><span class="sxs-lookup"><span data-stu-id="3e356-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="3e356-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="3e356-127">" \* + .</span></span> <span data-ttu-id="3e356-128">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="3e356-128">/ : ; < = > ?</span></span> <span data-ttu-id="3e356-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="3e356-129">\[ \] \\ \|</span></span>

<span data-ttu-id="3e356-130">Le **transport \_ IPX ncadg** est pris en charge par la version de NWLink fournie avec MS client 3,0.</span><span class="sxs-lookup"><span data-stu-id="3e356-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="3e356-131">les applications clientes Windows 16 bits qui utilisent le transport **\_ IPX ncadg** requièrent que le fichier Nwipxspx.dll être installé pour s’exécuter sous le sous-système wow.</span><span class="sxs-lookup"><span data-stu-id="3e356-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="3e356-132">Contactez Novell pour obtenir ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3e356-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="3e356-133">Pour obtenir les adresses du réseau et du nœud, utilisez l’utilitaire **ComCheck** de Novell ou l’API définie par Novell **IPXGetInternetAddress**.</span><span class="sxs-lookup"><span data-stu-id="3e356-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="3e356-134">Sur Windows, vous pouvez également obtenir ces adresses à l’aide de la commande **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="3e356-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="3e356-135">La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="3e356-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="3e356-136">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="3e356-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="3e356-137">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="3e356-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="3e356-138">Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="3e356-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3e356-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e356-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="3e356-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e356-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e356-141">**poste**</span><span class="sxs-lookup"><span data-stu-id="3e356-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="3e356-142">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="3e356-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3e356-143">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="3e356-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="3e356-144">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="3e356-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="3e356-145">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="3e356-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="3e356-146">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3e356-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="3e356-147">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="3e356-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="3e356-148">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="3e356-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="3e356-149">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3e356-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="3e356-150">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="3e356-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="3e356-151">**ncacn \_ réseaux virtuels \_ spp**</span><span class="sxs-lookup"><span data-stu-id="3e356-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="3e356-152">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="3e356-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="3e356-153">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="3e356-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="3e356-154">liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="3e356-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 