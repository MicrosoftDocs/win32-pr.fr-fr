---
description: Cette rubrique décrit les étapes nécessaires à la connexion d’un service Web entre votre magasin de données et la recherche fédérée de Windows, et explique comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Connexion de votre service Web dans la recherche fédérée Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112462"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="2d1bf-103">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="2d1bf-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="2d1bf-104">Cette rubrique décrit les étapes nécessaires à la connexion d’un service Web entre votre magasin de données et la recherche fédérée de Windows, et explique comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="2d1bf-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="2d1bf-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2d1bf-106">Connexion de votre service Web</span><span class="sxs-lookup"><span data-stu-id="2d1bf-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="2d1bf-107">Inscrire une banque de données distante existante</span><span class="sxs-lookup"><span data-stu-id="2d1bf-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="2d1bf-108">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2d1bf-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="2d1bf-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d1bf-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="2d1bf-110">Connexion de votre service Web</span><span class="sxs-lookup"><span data-stu-id="2d1bf-110">Connect Your web Service</span></span>

<span data-ttu-id="2d1bf-111">**Pour connecter le service Web de votre magasin de données à la recherche fédérée, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="2d1bf-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="2d1bf-112">Créez un fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="2d1bf-113">Fournissez le fichier. fichier osdx aux utilisateurs afin qu’ils puissent ajouter le service à la demande en ouvrant le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="2d1bf-114">Générez un connecteur de recherche et déployez-le activement dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="2d1bf-115">Inscrire une banque de données distante existante</span><span class="sxs-lookup"><span data-stu-id="2d1bf-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="2d1bf-116">Un utilisateur inscrit un nouveau magasin de données distant auprès de Windows Federated Search en ouvrant un fichier de description OpenSearch (. fichier osdx).</span><span class="sxs-lookup"><span data-stu-id="2d1bf-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="2d1bf-117">Lorsque l’utilisateur le fait, les événements suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="2d1bf-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="2d1bf-118">Un fichier. searchconnector-ms (connecteur de recherche) est créé dans le dossier recherches Windows (% UserProfile%/Searches).</span><span class="sxs-lookup"><span data-stu-id="2d1bf-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="2d1bf-119">Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier des liens (% UserProfile%/Links).</span><span class="sxs-lookup"><span data-stu-id="2d1bf-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="2d1bf-120">Un raccourci s’affiche dans le volet **favoris** de navigation de l’Explorateur Windows, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service Web.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="2d1bf-121">Un magasin de données qui dispose déjà d’un service Web [OpenSearch](https://github.com/dewitt/opensearch) qui est compatible avec Windows Federated Search peut être ajouté à l’Explorateur Windows lorsqu’un utilisateur ouvre un fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="2d1bf-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="2d1bf-122">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2d1bf-122">Additional Resources</span></span>

<span data-ttu-id="2d1bf-123">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d1bf-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d1bf-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d1bf-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d1bf-125">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="2d1bf-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="2d1bf-126">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="2d1bf-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="2d1bf-127">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="2d1bf-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="2d1bf-128">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="2d1bf-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="2d1bf-129">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="2d1bf-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="2d1bf-130">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="2d1bf-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
