---
title: Recherche Active Directory
description: Une fonction importante de Active Directory consiste à résoudre les requêtes de données pour les utilisateurs, ainsi que les données de configuration pour les ordinateurs et les services.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Recherche Active Directory ADSI
- ADSI ADSI, recherche Active Directory
- interroge ADSI, en recherchant Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309218"
---
# <a name="searching-active-directory"></a><span data-ttu-id="3fca9-106">Recherche Active Directory</span><span class="sxs-lookup"><span data-stu-id="3fca9-106">Searching Active Directory</span></span>

<span data-ttu-id="3fca9-107">Une fonction importante de Active Directory consiste à résoudre les requêtes de données pour les utilisateurs, ainsi que les données de configuration pour les ordinateurs et les services.</span><span class="sxs-lookup"><span data-stu-id="3fca9-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="3fca9-108">Pour écrire des requêtes efficaces pour Active Directory, il est utile de vous familiariser avec les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3fca9-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="3fca9-109">Détermination de l’étendue de la requête : le client doit-il Rechercher des propriétés pour les objets qui peuvent se trouver n’importe où dans une forêt, ou uniquement dans un domaine, ou dans une unité d’organisation (UO) donnée ?</span><span class="sxs-lookup"><span data-stu-id="3fca9-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="3fca9-110">Détermination de la profondeur de la requête : la requête doit-elle effectuer une recherche uniquement dans un niveau ou peut-elle traverser d’autres annuaires LDAP ?</span><span class="sxs-lookup"><span data-stu-id="3fca9-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="3fca9-111">Performances et gestion des jeux de résultats volumineux : comment le client doit-il gérer efficacement le potentiel d’un jeu de résultats volumineux ?</span><span class="sxs-lookup"><span data-stu-id="3fca9-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="3fca9-112">Détermination des meilleures requêtes : Quels types de requêtes fournissent les résultats les plus efficaces ?</span><span class="sxs-lookup"><span data-stu-id="3fca9-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="3fca9-113">Quels types de requêtes le développeur doit-il éviter ?</span><span class="sxs-lookup"><span data-stu-id="3fca9-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="3fca9-114">Compréhension de la syntaxe de requête : ADSI prend en charge la syntaxe LDAP comme indiqué dans RFC 2254, ainsi qu’un sous-ensemble de SQL.</span><span class="sxs-lookup"><span data-stu-id="3fca9-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="3fca9-115">Choix des interfaces : ADSI offre une prise en charge OLE DB, ainsi qu’une interface C/C++ appelée [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="3fca9-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="3fca9-116">Étant donné que l’interface ADSI fonctionne pour plusieurs espaces de noms, vous pouvez utiliser ces interfaces pour interroger d’autres espaces de noms tels qu’Exchange, ainsi que Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3fca9-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="3fca9-117">Étant donné que l’objet ADO (ActiveX Data Object) est un modèle objet d’accès aux données simple et scriptable par-dessus OLE DB, les interfaces OLE DB fonctionnent bien pour les programmeurs Visual Basic et les rédacteurs de script de page Web.</span><span class="sxs-lookup"><span data-stu-id="3fca9-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="3fca9-118">Les nouvelles fonctionnalités d’accès aux données dans les applications Visual Studio et Office qui tirent parti d’ADO et de OLE DB peuvent désormais accéder aux données Active Directory de la même manière qu’elles accèdent aux données d’autres fournisseurs OLE DB, telles que les SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3fca9-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="3fca9-119">Toutefois, si un développeur C/C++ doit effectuer une recherche d’annuaire simple, l’interface **IDirectorySearch** peut être plus appropriée que les interfaces de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3fca9-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="3fca9-120">Les rubriques suivantes expliquent comment effectuer des recherches Active Directory pour vous assurer que votre application émet la requête la plus efficace, en fonction des exigences du client :</span><span class="sxs-lookup"><span data-stu-id="3fca9-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="3fca9-121">Étendue de la requête</span><span class="sxs-lookup"><span data-stu-id="3fca9-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="3fca9-122">Performances et gestion des jeux de résultats volumineux</span><span class="sxs-lookup"><span data-stu-id="3fca9-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="3fca9-123">Syntaxe de filtre de recherche</span><span class="sxs-lookup"><span data-stu-id="3fca9-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="3fca9-124">Interfaces de requête</span><span class="sxs-lookup"><span data-stu-id="3fca9-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="3fca9-125">Recherche de données binaires</span><span class="sxs-lookup"><span data-stu-id="3fca9-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="3fca9-126">Requête distribuée</span><span class="sxs-lookup"><span data-stu-id="3fca9-126">Distributed Query</span></span>](distributed-query.md)

 

 




