---
title: attribut ncacn_dnet_nsp
description: Le \_ \_ mot clé ncacn dnet NSP identifie DECnet comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101604"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="176fc-105">ncacn \_ dnet, \_ attribut NSP</span><span class="sxs-lookup"><span data-stu-id="176fc-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="176fc-106">Le mot clé **ncacn \_ dnet \_ NSP** identifie DECnet comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="176fc-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="176fc-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="176fc-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="176fc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="176fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="176fc-109">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="176fc-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="176fc-110">Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="176fc-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="176fc-111">Le nom est une chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="176fc-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="176fc-112">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="176fc-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="176fc-113">Spécifie un nom d’objet DECnet ou un numéro d’objet.</span><span class="sxs-lookup"><span data-stu-id="176fc-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="176fc-114">Le nom de l’objet peut comporter jusqu’à 16 caractères.</span><span class="sxs-lookup"><span data-stu-id="176fc-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="176fc-115">Les numéros d’objet peuvent être précédés du signe dièse ( \# ).</span><span class="sxs-lookup"><span data-stu-id="176fc-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="176fc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="176fc-116">Remarks</span></span>

<span data-ttu-id="176fc-117">La syntaxe de la chaîne de port de transport DECnet, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="176fc-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="176fc-118">Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="176fc-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="176fc-119">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="176fc-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="176fc-120">Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="176fc-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="176fc-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="176fc-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="176fc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="176fc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176fc-123">**poste**</span><span class="sxs-lookup"><span data-stu-id="176fc-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="176fc-124">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="176fc-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 