---
title: attribut ncacn_ip_tcp
description: Le \_ \_ mot clé TCP IP NCACN identifie TCP/IP comme famille de protocoles pour le point de terminaison.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510065"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="e417a-104">ncacn \_ TCP IP ( \_ attribut)</span><span class="sxs-lookup"><span data-stu-id="e417a-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="e417a-105">Le mot clé **\_ \_ TCP IP ncacn** identifie TCP/IP comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e417a-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="e417a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e417a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e417a-107">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="e417a-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e417a-108">Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="e417a-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="e417a-109">Le nom est une chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="e417a-109">The name is a character string.</span></span> <span data-ttu-id="e417a-110">L’adresse Internet est une notation d’adresse Internet courante.</span><span class="sxs-lookup"><span data-stu-id="e417a-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="e417a-111">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="e417a-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e417a-112">Spécifie un nombre 16 bits facultatif.</span><span class="sxs-lookup"><span data-stu-id="e417a-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="e417a-113">Les valeurs inférieures à 1024 sont généralement réservées.</span><span class="sxs-lookup"><span data-stu-id="e417a-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="e417a-114">Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.</span><span class="sxs-lookup"><span data-stu-id="e417a-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e417a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e417a-115">Remarks</span></span>

<span data-ttu-id="e417a-116">La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="e417a-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="e417a-117">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="e417a-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="e417a-118">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="e417a-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="e417a-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e417a-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="e417a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e417a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e417a-121">**poste**</span><span class="sxs-lookup"><span data-stu-id="e417a-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="e417a-122">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e417a-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e417a-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="e417a-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="e417a-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="e417a-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="e417a-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="e417a-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="e417a-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="e417a-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="e417a-127">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="e417a-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 