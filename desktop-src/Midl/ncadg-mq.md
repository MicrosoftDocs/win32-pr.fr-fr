---
title: attribut ncadg_mq
description: Le \_ mot clé ncadg MQ identifie Microsoft Message Queuing services (MSMQ) comme protocole de transport pour le point de terminaison. Ce protocole est obsolète et ne doit pas être utilisé dans les nouvelles applications.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940907"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="dab2f-105">\_attribut MQ ncadg</span><span class="sxs-lookup"><span data-stu-id="dab2f-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="dab2f-106">Le mot clé **ncadg \_ MQ** identifie Microsoft Message QUEUING services (MSMQ) comme protocole de transport pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="dab2f-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="dab2f-107">Ce protocole est obsolète et ne doit pas être utilisé dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="dab2f-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="dab2f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dab2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab2f-109">*nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="dab2f-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dab2f-110">Spécifie le nom du serveur ou de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="dab2f-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="dab2f-111">Le nom est une chaîne de caractères et peut être un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="dab2f-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dab2f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dab2f-112">Remarks</span></span>

<span data-ttu-id="dab2f-113">Pour pouvoir utiliser le protocole de transport **ncadg \_ MQ** , les composants MSMQ doivent être entièrement installés et les systèmes client et serveur doivent être accessibles via les protocoles mq.</span><span class="sxs-lookup"><span data-stu-id="dab2f-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="dab2f-114">Le protocole **ncadg \_ MQ** ne prend pas en charge les points de terminaison ou les appels de [**diffusion**](broadcast.md) dynamiques.</span><span class="sxs-lookup"><span data-stu-id="dab2f-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="dab2f-115">Comme avec les autres protocoles de datagramme, **ncadg \_ MQ** ne prend pas en charge les rappels ; les fonctions qui utilisent l’attribut de [**rappel**](callback.md) échouent.</span><span class="sxs-lookup"><span data-stu-id="dab2f-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="dab2f-116">Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="dab2f-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dab2f-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="dab2f-117">Examples</span></span>

<span data-ttu-id="dab2f-118">La syntaxe du protocole de file d’attente de messages est définie indépendamment de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="dab2f-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="dab2f-119">Le compilateur MIDL effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="dab2f-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="dab2f-120">Certaines erreurs peuvent être signalées au moment de l’exécution plutôt que pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="dab2f-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="dab2f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab2f-122">**diffusion**</span><span class="sxs-lookup"><span data-stu-id="dab2f-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="dab2f-123">**rappel**</span><span class="sxs-lookup"><span data-stu-id="dab2f-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="dab2f-124">**poste**</span><span class="sxs-lookup"><span data-stu-id="dab2f-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="dab2f-125">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="dab2f-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dab2f-126">**Message**</span><span class="sxs-lookup"><span data-stu-id="dab2f-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="dab2f-127">Message Queuing RPC</span><span class="sxs-lookup"><span data-stu-id="dab2f-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="dab2f-128">Liaison de chaîne</span><span class="sxs-lookup"><span data-stu-id="dab2f-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 