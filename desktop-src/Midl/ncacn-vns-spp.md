---
title: attribut ncacn_vns_spp
description: Le \_ \_ mot clé ncacn réseaux virtuels spp identifie Banyan VINES spp comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726077"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="ebeaa-105">\_ \_ attribut spp ncacn réseaux virtuels</span><span class="sxs-lookup"><span data-stu-id="ebeaa-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="ebeaa-106">Le mot clé **ncacn \_ réseaux virtuels \_ spp** identifie Banyan VINES spp comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="ebeaa-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="ebeaa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebeaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebeaa-109">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="ebeaa-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ebeaa-110">Spécifie le nom StreetTalk du serveur.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="ebeaa-111">Le nom se présente sous la forme item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="ebeaa-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="ebeaa-112">L’élément peut contenir jusqu’à 31 caractères et le groupe et l’organisation peuvent comporter jusqu’à 15 caractères.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ebeaa-113">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="ebeaa-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ebeaa-114">Spécifie un port de Banyan VINES SPP.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="ebeaa-115">La plage valide pour les points de terminaison statiques est 250 – 511.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebeaa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ebeaa-116">Remarks</span></span>

<span data-ttu-id="ebeaa-117">Pour pouvoir utiliser le protocole de transport **ncacn \_ réseaux virtuels \_ spp** dans des applications distribuées exécutées sur Windows 2000, le logiciel client Banyan Enterprise approprié doit être installé.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="ebeaa-118">Après l’installation, ouvrez **le panneau** de **configuration, choisissez Configuration et ajouter**, puis sélectionnez **service \| Banyan \| RPC services pour Banyan**.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="ebeaa-119">La prise en charge des clients 16 bits requiert le logiciel Vines approprié.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="ebeaa-120">Pour plus d’informations sur le produit client entreprise de Banyan et le logiciel de la vigne 16 bits, contactez Banyan.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="ebeaa-121">La syntaxe de la chaîne du port de transport Banyan VINES SPP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="ebeaa-122">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="ebeaa-123">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="ebeaa-124">Cette famille de protocoles n’est pas prise en charge dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ebeaa-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="ebeaa-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="ebeaa-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebeaa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebeaa-127">**poste**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ebeaa-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-129">**ncacn \_ au \_ fournisseur DSP**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-130">**ncacn \_ dnet \_**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-137">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-138">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-139">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="ebeaa-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="ebeaa-140">liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="ebeaa-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 