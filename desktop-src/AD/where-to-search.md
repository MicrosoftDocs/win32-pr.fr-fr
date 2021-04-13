---
title: Choix de l’emplacement de recherche
description: Cette rubrique explique les différentes recherches qui peuvent être effectuées dans Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Choix de l’emplacement où rechercher les annonces
- Active Directory AD, recherche, choix de l’emplacement de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314597"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="44431-105">Choix de l’emplacement de recherche</span><span class="sxs-lookup"><span data-stu-id="44431-105">Deciding Where to Search</span></span>

<span data-ttu-id="44431-106">Cette rubrique explique les différentes recherches qui peuvent être effectuées dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="44431-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="44431-107">Toutes les recherches sont effectuées dans l’un des contextes de nommage suivants :</span><span class="sxs-lookup"><span data-stu-id="44431-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="44431-108">Domaine, y compris les partitions d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="44431-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="44431-109">Conteneur de schéma</span><span class="sxs-lookup"><span data-stu-id="44431-109">Schema container</span></span>
-   <span data-ttu-id="44431-110">Conteneur de configuration</span><span class="sxs-lookup"><span data-stu-id="44431-110">Configuration container</span></span>
-   <span data-ttu-id="44431-111">Catalogue global</span><span class="sxs-lookup"><span data-stu-id="44431-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="44431-112">Recherche dans un domaine</span><span class="sxs-lookup"><span data-stu-id="44431-112">Searching a Domain</span></span>

<span data-ttu-id="44431-113">Les domaines contiennent la plupart des objets hautement utilisés tels que les utilisateurs, les contacts, les groupes, les unités d’organisation, les ordinateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="44431-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="44431-114">La plupart des requêtes effectuent une recherche dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="44431-114">Most queries will search a domain.</span></span> <span data-ttu-id="44431-115">Pour plus d’informations sur la recherche d’un domaine, consultez [recherche de contenu de domaine](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="44431-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="44431-116">Recherche dans le conteneur de schéma</span><span class="sxs-lookup"><span data-stu-id="44431-116">Searching the Schema Container</span></span>

<span data-ttu-id="44431-117">Le conteneur de schéma contient les objets [**classSchema**](/windows/desktop/ADSchema/c-classschema) et [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) qui fournissent la définition formelle de chaque classe et attribut qui peut exister dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="44431-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="44431-118">Pour rechercher des objets dans le conteneur de schéma, connectez-vous au conteneur de schéma sur n’importe quel contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="44431-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="44431-119">Le conteneur de schéma est disponible sur tous les contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="44431-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="44431-120">Le nom unique du conteneur de schéma est obtenu à partir de l’attribut **schemaNamingContext** de rootDSE.</span><span class="sxs-lookup"><span data-stu-id="44431-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="44431-121">Pour plus d’informations sur rootDSE et l’attribut **schemaNamingContext** , consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="44431-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="44431-122">Pour plus d’informations sur la lecture à partir du conteneur de schéma ou de schéma abstrait, consultez [instructions pour la liaison au schéma](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="44431-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="44431-123">Recherche dans le conteneur de configuration</span><span class="sxs-lookup"><span data-stu-id="44431-123">Searching the Configuration Container</span></span>

<span data-ttu-id="44431-124">Le conteneur de configuration contient des informations de configuration, telles que les sites, les services et les spécificateurs d’affichage, pour l’ensemble de la forêt.</span><span class="sxs-lookup"><span data-stu-id="44431-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="44431-125">Pour rechercher des objets dans le conteneur de configuration, connectez-vous au conteneur de configuration sur n’importe quel contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="44431-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="44431-126">Le conteneur de configuration est disponible sur tous les contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="44431-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="44431-127">Le nom unique du conteneur de configuration est obtenu à partir de l’attribut **configurationNamingContext** de rootDSE.</span><span class="sxs-lookup"><span data-stu-id="44431-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="44431-128">Pour plus d’informations sur rootDSE et l’attribut **configurationNamingContext** , consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="44431-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="44431-129">Recherche dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="44431-129">Searching the Global Catalog</span></span>

<span data-ttu-id="44431-130">Le catalogue global contient un réplica de chaque objet dans Active Directory Domain Services, mais avec seulement un petit nombre de leurs attributs.</span><span class="sxs-lookup"><span data-stu-id="44431-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="44431-131">Les attributs du catalogue global sont ceux qui sont utilisés le plus fréquemment dans les opérations de recherche, comme le prénom et le nom d’un utilisateur, les noms de connexion, etc.</span><span class="sxs-lookup"><span data-stu-id="44431-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="44431-132">Pour plus d’informations sur la recherche dans le catalogue global, consultez [recherche dans le catalogue global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="44431-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 