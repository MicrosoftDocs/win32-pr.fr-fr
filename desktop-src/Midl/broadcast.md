---
title: attribut de diffusion
description: Le mot clé \ Broadcast \ spécifie que les appels de procédure distante doivent être envoyés à tous les serveurs sur un réseau local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- attribut de diffusion MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312853"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="6ce27-104">attribut de diffusion</span><span class="sxs-lookup"><span data-stu-id="6ce27-104">broadcast attribute</span></span>

<span data-ttu-id="6ce27-105">Le mot clé **\[ Broadcast \]** spécifie que les appels de procédure distante doivent être envoyés à tous les serveurs sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="6ce27-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="6ce27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ce27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce27-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="6ce27-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-108">Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="6ce27-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="6ce27-109">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="6ce27-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="6ce27-110">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="6ce27-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-111">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="6ce27-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6ce27-112">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="6ce27-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-113">Spécifie des attributs supplémentaires à appliquer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="6ce27-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="6ce27-114">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="6ce27-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6ce27-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="6ce27-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-116">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6ce27-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="6ce27-117">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="6ce27-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-118">Spécifie le nom de la fonction à laquelle l’attribut de **\[ diffusion \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="6ce27-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="6ce27-119">*params*</span><span class="sxs-lookup"><span data-stu-id="6ce27-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce27-120">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6ce27-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ce27-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6ce27-121">Remarks</span></span>

<span data-ttu-id="6ce27-122">Le mot clé **\[ Broadcast \]** spécifie que la routine est toujours diffusée à tous les serveurs sur le réseau, au lieu d’être remise à un serveur particulier. Le client reçoit la sortie de la première réponse pour qu’elle retourne correctement, tandis que les réponses suivantes sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="6ce27-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="6ce27-123">Une opération avec l’attribut **\[ Broadcast \]** est implicitement une opération [**\[ idempotent \]**](idempotent.md) .</span><span class="sxs-lookup"><span data-stu-id="6ce27-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="6ce27-124">Toutefois, l’attribut **\[ Broadcast \]** spécifie des propriétés supplémentaires que les fonctions avec l’attribut **\[ idempotent \]** n’ont pas.</span><span class="sxs-lookup"><span data-stu-id="6ce27-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="6ce27-125">Plus précisément, les fonctions qui utilisent l’attribut **\[ Broadcast \]** spécifient que la routine peut être appelée plusieurs fois à la suite d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="6ce27-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="6ce27-126">En même temps, ils peuvent être envoyés à plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="6ce27-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="6ce27-127">Cela diffère de l’attribut **\[ idempotent \]** , qui spécifie uniquement qu’un appel peut être retenté s’il n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="6ce27-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="6ce27-128">Si une procédure distante diffuse son appel à tous les ordinateurs hôtes sur un réseau local, elle doit utiliser la séquence de [**protocole \_ IPX**](ncadg-ipx.md) [**ncadg \_ \_ IP**](ncadg-ip-udp.md) ou ncadg.</span><span class="sxs-lookup"><span data-stu-id="6ce27-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="6ce27-129">Notez que la taille d’un paquet de **\[ diffusion \]** est déterminée par le service de datagramme en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6ce27-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ce27-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ce27-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce27-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="6ce27-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="6ce27-132">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="6ce27-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6ce27-133">**environ**</span><span class="sxs-lookup"><span data-stu-id="6ce27-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="6ce27-134">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="6ce27-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="6ce27-135">**\_IPX ncadg**</span><span class="sxs-lookup"><span data-stu-id="6ce27-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




