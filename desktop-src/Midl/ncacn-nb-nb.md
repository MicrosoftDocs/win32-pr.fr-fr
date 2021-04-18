---
title: attribut ncacn_nb_nb
description: Le \_ \_ mot clé ncacn NB NB identifie NetBEUI sur NetBIOS comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512312"
---
# <a name="ncacn_nb_nb-attribute"></a><span data-ttu-id="5af92-105">ncacn \_ NB \_ NB (attribut)</span><span class="sxs-lookup"><span data-stu-id="5af92-105">ncacn\_nb\_nb attribute</span></span>

<span data-ttu-id="5af92-106">Le mot clé **ncacn \_ NB \_ NB** identifie NetBEUI sur NetBIOS comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5af92-106">The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="5af92-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="5af92-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="5af92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5af92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af92-109">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="5af92-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5af92-110">Spécifie une valeur 8 bits facultative comprise entre 1 et 255.</span><span class="sxs-lookup"><span data-stu-id="5af92-110">Specifies an optional 8-bit value ranging from 1 to 255.</span></span> <span data-ttu-id="5af92-111">Les valeurs inférieures à 0x20 sont réservées.</span><span class="sxs-lookup"><span data-stu-id="5af92-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="5af92-112">Si la valeur de *nom de port* n’est pas spécifiée, le service de mappage de point de terminaison sélectionne la valeur de port.</span><span class="sxs-lookup"><span data-stu-id="5af92-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5af92-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5af92-113">Remarks</span></span>

<span data-ttu-id="5af92-114">La syntaxe de la chaîne de port NetBIOS, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="5af92-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="5af92-115">Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="5af92-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="5af92-116">Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5af92-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="5af92-117">Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="5af92-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5af92-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="5af92-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="5af92-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af92-120">**poste**</span><span class="sxs-lookup"><span data-stu-id="5af92-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="5af92-121">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5af92-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5af92-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="5af92-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="5af92-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="5af92-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="5af92-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="5af92-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="5af92-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="5af92-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="5af92-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="5af92-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="5af92-127">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="5af92-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 