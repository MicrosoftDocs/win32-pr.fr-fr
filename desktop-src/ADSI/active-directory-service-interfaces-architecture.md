---
title: Architecture des interfaces de service Active Directory
description: De nombreux services d’annuaire sont hiérarchiques et se prêtent donc à un modèle d’objet hiérarchique. Cette section utilise des représentations d’objets COM pour illustrer différentes fonctionnalités d’ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Architecture des interfaces de service Active Directory ADSI
- ADSI ADSI, à propos de, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671197"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="fe4b3-106">Architecture des interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="fe4b3-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="fe4b3-107">De nombreux services d’annuaire sont hiérarchiques et se prêtent donc à un modèle d’objet hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="fe4b3-108">Cette section utilise des représentations d’objets COM pour illustrer différentes fonctionnalités d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="fe4b3-109">Dans la figure ci-dessous, un objet système de niveau supérieur contient un objet d’espace de noms pour chaque fournisseur ADSI installé.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![objet conteneur d’espaces de noms](images/ds2top.png)

<span data-ttu-id="fe4b3-111">Chacun des objets d’espace de noms est lui-même un conteneur qui contient les nœuds racine de niveau supérieur de chaque serveur, domaine ou tout autre type d’objets de système d’annuaire qui sont définis en tant que racines dans chaque service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="fe4b3-112">ADSI fournit un ensemble d’interfaces et d’objets prédéfinis afin que les applications clientes puissent interagir avec les services d’annuaire à l’aide d’un ensemble de méthodes uniformes.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="fe4b3-113">Toutefois, ADSI peut ne pas fournir l’accès à toutes les fonctionnalités d’un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="fe4b3-114">Pour mieux utiliser l’ensemble complet des fonctionnalités de chaque service d’annuaire, ADSI fournit un modèle de schéma que les fournisseurs de services d’annuaire et les fournisseurs de logiciels tiers peuvent utiliser pour étendre les fonctionnalités au-delà des interfaces fournies dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="fe4b3-115">Les objets conteneurs de nœud racine, qui se trouvent dans chaque objet espace de noms de fournisseur, incluent un objet conteneur de schéma ADSI.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="fe4b3-116">Cet objet contient la définition de toutes les fonctionnalités de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fe4b3-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="fe4b3-117">Pour plus d’informations, consultez [modèle de schéma ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="fe4b3-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="fe4b3-118">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe4b3-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="fe4b3-119">Objets interfaces du service Active Directory</span><span class="sxs-lookup"><span data-stu-id="fe4b3-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="fe4b3-120">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="fe4b3-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="fe4b3-121">Fournisseur d’interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="fe4b3-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="fe4b3-122">Modèle de schéma ADSI</span><span class="sxs-lookup"><span data-stu-id="fe4b3-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




