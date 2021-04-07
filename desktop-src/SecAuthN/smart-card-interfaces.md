---
description: Une interface de carte à puce se compose d’un ensemble prédéfini de services disponibles au sein d’une carte à puce, des protocoles nécessaires pour appeler les services et de toute hypothèse relative au contexte des services.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758391"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="a5d0b-103">Interfaces de carte à puce</span><span class="sxs-lookup"><span data-stu-id="a5d0b-103">Smart Card Interfaces</span></span>

<span data-ttu-id="a5d0b-104">Une interface de [*carte à puce*](../secgloss/s-gly.md) se compose d’un ensemble prédéfini de services disponibles au sein d’une *carte à puce*, des protocoles nécessaires pour appeler les services et de toute hypothèse relative au contexte des services.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="a5d0b-105">En ce qui concerne les cartes à puce, le terme « interface » est semblable à la façon dont il est utilisé dans COM, qui, à son tour, est similaire au concept de l’identificateur d’application ISO 7816/5, mais avec une portée différente.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="a5d0b-106">Chaque interface de carte à puce est identifiée par un GUID.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="a5d0b-107">Par exemple, une interface peut être définie pour fournir des informations de biorythme à son détenteur.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="a5d0b-108">Si une carte à puce donnée prend en charge ce service, elle peut demander à prendre en charge ce GUID d’interface.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="a5d0b-109">À l’aide des GUID d’interface, une application peut rechercher un ensemble particulier d’interfaces, en localisant une carte qui prend en charge ce jeu pour terminer une tâche.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="a5d0b-110">Bien qu’une interface ait un GUID, elle peut être implémentée différemment sur différentes cartes.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="a5d0b-111">Par exemple, l’interface de biorythme mentionnée ci-dessus peut avoir plusieurs implémentations différentes, mais toutes sont référencées à l’aide du même GUID.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="a5d0b-112">Les différentes implémentations ne modifient pas l’interaction entre l’application et la carte à puce ; Toutefois, l’interaction entre le [*fournisseur de services*](../secgloss/c-gly.md) et les cartes à puce peut varier en fonction de l’implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a5d0b-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="a5d0b-113">L’ensemble des interfaces prises en charge par une carte à puce est défini lors de l’introduction de la carte à puce (voir [Présentation des cartes à puce au système](introducing-smart-cards-to-the-system.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d0b-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
