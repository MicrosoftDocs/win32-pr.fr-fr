---
description: TAPI 3 prend en charge l’intégration d’interfaces spécifiques au fournisseur de services dans les objets standard, ce qui permet aux applications de tirer parti des fonctionnalités spécifiques au fournisseur.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035040"
---
# <a name="provider-specific-interfaces"></a><span data-ttu-id="93c19-103">Interfaces Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="93c19-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="93c19-104">TAPI 3 prend en charge l’intégration d’interfaces spécifiques au fournisseur de services dans les objets standard, ce qui permet aux applications de tirer parti des fonctionnalités spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="93c19-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="93c19-105">En outre, TAPI 3 permet aux fournisseurs de services de fournir des événements spécifiques au fournisseur aux applications en tant qu’objets COM sur la même interface que celle sur laquelle l’application reçoit des événements standard.</span><span class="sxs-lookup"><span data-stu-id="93c19-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="93c19-106">L’interface TAPI réalise cette intégration en regroupant des objets spécifiques au fournisseur avec les objets standard (TAPI, Address, terminal, Call et CallHub) et en distribuant ou déléguant des méthodes inconnues à ces objets spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="93c19-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="93c19-107">Par exemple, un fournisseur de services peut autoriser les applications à obtenir des informations sur un appel au-delà de ce qui est exposé par l’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="93c19-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="93c19-108">Le fournisseur doit définir une interface qui permet aux applications d’effectuer ces requêtes supplémentaires et d’implémenter cette interface sur un objet.</span><span class="sxs-lookup"><span data-stu-id="93c19-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="93c19-109">Cet objet implémente également une interface d’interrogation des informations sur le fournisseur afin qu’une application puisse découvrir les types de fonctions spécifiques au fournisseur qui peuvent être disponibles.</span><span class="sxs-lookup"><span data-stu-id="93c19-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="93c19-110">Lorsque l’application obtient une référence à un objet d’appel, l’application peut utiliser la nouvelle interface propre au fournisseur et ses méthodes comme si elles étaient implémentées par l’objet d’appel lui-même.</span><span class="sxs-lookup"><span data-stu-id="93c19-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="93c19-111">Consultez la [référence MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md) pour obtenir la liste de toutes les interfaces MSP standard.</span><span class="sxs-lookup"><span data-stu-id="93c19-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="93c19-112">Pour obtenir la liste de toutes les interfaces spécifiques au MSP IPConf, consultez la page [interfaces IPCONF MSP](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="93c19-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



