---
title: Implémentation des fournisseurs d’interfaces de service Active Directory
description: Les interfaces ADSI (Active Directory Service Interfaces) sont des interfaces COM qui encapsulent des objets de service d’annuaire pour les exposer aux clients des services d’annuaire. En fournissant une implémentation d’ADSI, vous étendez votre client-base à l’ensemble des applications clientes ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implémentation des fournisseurs d’interfaces de service Active Directory ADSI
- Implémentation de l’interface ADSI des fournisseurs ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671142"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="4ca9d-106">Implémentation des fournisseurs d’interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="4ca9d-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="4ca9d-107">Les interfaces ADSI (Active Directory Service Interfaces) sont des interfaces COM qui encapsulent des objets de service d’annuaire pour les exposer aux clients des services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="4ca9d-108">En fournissant une implémentation d’ADSI, vous étendez votre client-base à l’ensemble des applications clientes ADSI.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="4ca9d-109">Comme pour toute implémentation COM, vous pouvez écrire un fournisseur ADSI dans de nombreux langages.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="4ca9d-110">Les interfaces COM ADSI sont définies en tant qu’interfaces doubles qui autorisent la résolution de noms au moment de l’exécution et au moment de la compilation et peuvent être appelées par des langages conformes à Automation tels que Visual Basic, Visual Basic Scripting Edition, ainsi que des langages de performances et d’efficacité plus sensibles, tels que C et C++.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="4ca9d-111">Les clients ADSI incluent également les applications Web à l’aide des composants logiciels enfichables pages et administration de Active Server via Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="4ca9d-112">Étant donné que l’interface ADSI fournit son propre OLE DB fournisseur, l’implémentation des fonctionnalités de recherche définies par [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) permet également aux clients ADSI d’interroger votre service d’annuaire à la recherche de données.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="4ca9d-113">Tous les objets de service d’annuaire peuvent être représentés par un objet ADSI générique prenant en charge [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="4ca9d-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="4ca9d-114">ADSI fournit les blocs de construction nécessaires pour représenter les fonctionnalités et les services d’un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="4ca9d-115">En outre, les interfaces méta ADSI représentent des objets communs utilisés par les administrateurs de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="4ca9d-116">Vous mappez les propriétés des méta-interfaces avec les propriétés prises en charge par votre service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="4ca9d-117">Les clients ADSI programmant sur les interfaces du service Active Directory accèdent à votre service d’annuaire dès que le fournisseur est installé et que le système a redémarré.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="4ca9d-118">Si votre service d’annuaire prend en charge une représentation de schéma, la prise en charge des interfaces de gestion de schéma rend votre espace de noms accessible directement aux navigateurs de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="4ca9d-119">En publiant vos fonctionnalités par le biais du schéma, les clients peuvent interroger votre service d’annuaire en ligne et tirer parti des services que vous offrez.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="4ca9d-120">En raison de la disponibilité du schéma en ligne et de l’avantage de l’interface COM, vous pouvez continuer à mettre de nouvelles fonctionnalités à la disposition de votre logiciel client tout en prenant en charge les versions de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="4ca9d-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




