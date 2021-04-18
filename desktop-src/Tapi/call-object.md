---
description: L’objet d’appel représente une connexion d’adresses entre l’adresse locale et une ou plusieurs autres adresses.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Objet d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522747"
---
# <a name="call-object"></a><span data-ttu-id="aff9a-103">Objet d’appel</span><span class="sxs-lookup"><span data-stu-id="aff9a-103">Call Object</span></span>

<span data-ttu-id="aff9a-104">L’objet d’appel représente la connexion d’une adresse entre l’adresse locale et une ou plusieurs autres adresses.</span><span class="sxs-lookup"><span data-stu-id="aff9a-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="aff9a-105">Tout le contrôle d’appel est effectué par le biais de l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="aff9a-105">All call control is done through the Call object.</span></span> <span data-ttu-id="aff9a-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) et [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sont les interfaces les plus fréquemment utilisées sur l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="aff9a-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="aff9a-107">Ces interfaces implémentent une variété d’opérations et de requêtes, telles que l’acquisition de pointeurs d’interface pour les flux multimédias ou l’obtention de l’ID de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="aff9a-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="aff9a-108">Consultez les principales sections de la vue d’ensemble sur les [opérations de session](session-operations-ovr.md) et les [informations de session](session-information-ovr.md) pour les révisions de celles prises en charge par TAPI.</span><span class="sxs-lookup"><span data-stu-id="aff9a-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="aff9a-109">Un fournisseur de services multimédias peut implémenter des [interfaces spécifiques au fournisseur](provider-specific-interfaces.md), qui sont agrégées sur un objet d’appel par l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="aff9a-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="aff9a-110">Pour plus d’informations sur l’implémentation d’un fournisseur, consultez la documentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="aff9a-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="aff9a-111">Les exemples [créer un appel](make-a-call.md) et [recevoir un](receive-a-call.md) code d’appel montrent quelques illustrations de l’utilisation d’un objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="aff9a-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="aff9a-112">Consultez [appeler des interfaces d’objet](call-object-interfaces.md) pour obtenir la liste de toutes les interfaces associées à l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="aff9a-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



