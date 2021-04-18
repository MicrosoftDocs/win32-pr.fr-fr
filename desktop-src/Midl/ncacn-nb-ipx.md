---
title: attribut ncacn_nb_ipx
description: Le \_ \_ mot clé ncacn NB IPX identifie NetBIOS sur IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512099"
---
# <a name="ncacn_nb_ipx-attribute"></a><span data-ttu-id="59ac7-105">\_attribut ncacn NB \_ IPX</span><span class="sxs-lookup"><span data-stu-id="59ac7-105">ncacn\_nb\_ipx attribute</span></span>

<span data-ttu-id="59ac7-106">Le mot clé **ncacn \_ NB \_ IPX** identifie NetBIOS sur IPX comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="59ac7-106">The **ncacn\_nb\_ipx** keyword identifies NetBIOS over IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="59ac7-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="59ac7-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="59ac7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59ac7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ac7-109">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="59ac7-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="59ac7-110">Spécifie une valeur 8 bits facultative comprise entre 1 et 254.</span><span class="sxs-lookup"><span data-stu-id="59ac7-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="59ac7-111">Les valeurs inférieures à 0x20 sont réservées.</span><span class="sxs-lookup"><span data-stu-id="59ac7-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="59ac7-112">Si la valeur de *nom de port* n’est pas spécifiée, le service de mappage de point de terminaison sélectionne la valeur de port.</span><span class="sxs-lookup"><span data-stu-id="59ac7-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59ac7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="59ac7-113">Remarks</span></span>

<span data-ttu-id="59ac7-114">La syntaxe de la chaîne de port NetBIOS, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="59ac7-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="59ac7-115">Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="59ac7-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="59ac7-116">Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="59ac7-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="59ac7-117">Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="59ac7-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="59ac7-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="59ac7-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="59ac7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ac7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ac7-120">**poste**</span><span class="sxs-lookup"><span data-stu-id="59ac7-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="59ac7-121">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="59ac7-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="59ac7-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="59ac7-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="59ac7-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="59ac7-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="59ac7-124">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="59ac7-124">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="59ac7-125">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="59ac7-125">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="59ac7-126">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="59ac7-126">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="59ac7-127">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="59ac7-127">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="59ac7-128">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="59ac7-128">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="59ac7-129">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="59ac7-129">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="59ac7-130">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="59ac7-130">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="59ac7-131">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="59ac7-131">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 