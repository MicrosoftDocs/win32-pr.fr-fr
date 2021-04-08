---
title: Utilisation des interfaces de service Active Directory
description: Les interfaces de service Active Directory (ADSI) permettent aux applications clientes des services d’annuaire d’utiliser un ensemble d’interfaces pour communiquer avec n’importe quel espace de noms qui fournit une implémentation ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Utilisation des interfaces de service Active Directory ADSI
- ADSI ADSI, utilisation
- Interfaces ADSI (Active Directory Service Interfaces), utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839118"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="55f6d-106">Utilisation des interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="55f6d-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="55f6d-107">Les interfaces de service Active Directory (ADSI) permettent aux applications clientes des services d’annuaire d’utiliser un ensemble d’interfaces pour communiquer avec n’importe quel espace de noms qui fournit une implémentation ADSI.</span><span class="sxs-lookup"><span data-stu-id="55f6d-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="55f6d-108">Les clients ADSI utilisent les interfaces de service Active Directory bien définies à la place des appels d’API spécifiques au réseau pour obtenir un accès plus simple aux services d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="55f6d-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="55f6d-109">Active Directory interfaces de service sont conformes au modèle COM (Component Object Model) et prennent en charge les fonctionnalités COM standard.</span><span class="sxs-lookup"><span data-stu-id="55f6d-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="55f6d-110">ADSI fournit des interfaces qui sont conformes à l’automatisation pour les contrôleurs liés au nom tels que Java, Microsoft Visual Basic Development System et Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="55f6d-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="55f6d-111">ADSI peut également fournir une interface qui peut optimiser les performances pour les interfaces qui ne sont pas conformes à Automation, à utiliser avec des environnements de langage tels que C et C++.</span><span class="sxs-lookup"><span data-stu-id="55f6d-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="55f6d-112">ADSI fournit également les interfaces non-Automation, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), pour prendre en charge la gestion et les requêtes d’objets d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="55f6d-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="55f6d-113">En outre, l’interface ADSI fournit son propre fournisseur de OLE DB, de sorte que tout client qui utilise déjà OLE DB, y compris ceux qui utilisent ActiveX Data Objects, peut interroger directement les services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="55f6d-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="55f6d-114">Les applications Web qui utilisent des pages de Active Server peuvent également programmer l’accès aux services d’annuaire par le biais d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="55f6d-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="55f6d-115">Les clients ADSI peuvent découvrir par programmation tous les fournisseurs ADSI sur un site et utiliser les mêmes interfaces pour communiquer avec chaque espace de noms.</span><span class="sxs-lookup"><span data-stu-id="55f6d-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="55f6d-116">Au fur et à mesure que des fournisseurs supplémentaires sont installés, les clients ADSI peuvent communiquer, sans recompilation, avec les nouveaux espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="55f6d-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="55f6d-117">Ce guide de programmation décrit le fonctionnement d’ADSI et fournit des informations pour effectuer des tâches spécifiques dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="55f6d-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="55f6d-118">Les rubriques suivantes sont présentées :</span><span class="sxs-lookup"><span data-stu-id="55f6d-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="55f6d-119">Liaison à un objet ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="55f6d-120">Création et suppression d’objets</span><span class="sxs-lookup"><span data-stu-id="55f6d-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="55f6d-121">Accès et manipulation de données avec ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="55f6d-122">Utilisation du schéma ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="55f6d-123">Collections et groupes</span><span class="sxs-lookup"><span data-stu-id="55f6d-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="55f6d-124">Énumération des objets ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="55f6d-125">Recherche Active Directory</span><span class="sxs-lookup"><span data-stu-id="55f6d-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="55f6d-126">Modèle de sécurité ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="55f6d-127">Extensions ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="55f6d-128">Utilisation d’ADSI avec Exchange</span><span class="sxs-lookup"><span data-stu-id="55f6d-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="55f6d-129">Interfaces de l’utilitaire ADSI</span><span class="sxs-lookup"><span data-stu-id="55f6d-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="55f6d-130">Programmation d’ADSI avec Java/COM</span><span class="sxs-lookup"><span data-stu-id="55f6d-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




