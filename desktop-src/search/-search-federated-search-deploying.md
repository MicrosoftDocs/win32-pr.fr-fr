---
description: Cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de description OpenSearch (. fichier osdx), le déploiement d’un fichier. fichier osdx et le suivi de l’utilisation de votre service OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Déployer des connecteurs de recherche dans la recherche fédérée Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484440"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="3b0fb-103">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="3b0fb-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="3b0fb-104">Cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de description OpenSearch (. fichier osdx), le déploiement d’un fichier. fichier osdx et le suivi de l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="3b0fb-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="3b0fb-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="3b0fb-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3b0fb-106">Fichier. searchconnector-ms (connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="3b0fb-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="3b0fb-107">Méthodes de déploiement</span><span class="sxs-lookup"><span data-stu-id="3b0fb-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="3b0fb-108">Déploiement par extraction</span><span class="sxs-lookup"><span data-stu-id="3b0fb-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="3b0fb-109">Déploiement Push</span><span class="sxs-lookup"><span data-stu-id="3b0fb-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="3b0fb-110">Suivi de l’utilisation</span><span class="sxs-lookup"><span data-stu-id="3b0fb-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="3b0fb-111">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3b0fb-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3b0fb-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b0fb-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="3b0fb-113">Fichier. searchconnector-ms (connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="3b0fb-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="3b0fb-114">Il vous suffit d’ouvrir le fichier. fichier osdx qui décrit comment se connecter au service Web et de mapper les éléments personnalisés dans votre fichier. XML RSS ou Atom inscrit votre nouveau magasin de données distant avec la recherche fédérée.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="3b0fb-115">Un magasin de données qui dispose déjà d’un service Web [OpenSearch](https://github.com/dewitt/opensearch) compatible avec la recherche fédérée peut être ajouté à l’Explorateur Windows lorsqu’un utilisateur ouvre un fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="3b0fb-116">Une fois que vous avez donné l’fichier osdx à votre utilisateur et que l’utilisateur ouvre le fichier. fichier osdx, les événements suivants se produisent.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="3b0fb-117">Un fichier. searchconnector-MS est créé dans le dossier **recherches Windows** (% UserProfile%/Searches).</span><span class="sxs-lookup"><span data-stu-id="3b0fb-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="3b0fb-118">Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier **des liens** (% UserProfile%/Links).</span><span class="sxs-lookup"><span data-stu-id="3b0fb-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="3b0fb-119">Un raccourci s’affiche dans le volet **favoris** de navigation de l’Explorateur Windows, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service Web.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="3b0fb-120">Méthodes de déploiement</span><span class="sxs-lookup"><span data-stu-id="3b0fb-120">Deployment Methods</span></span>

<span data-ttu-id="3b0fb-121">Il existe deux façons de déployer des connecteurs de recherche, le déploiement par extraction et le déploiement push.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="3b0fb-122">Déploiement par extraction</span><span class="sxs-lookup"><span data-stu-id="3b0fb-122">Pull Deployment</span></span>

<span data-ttu-id="3b0fb-123">Le déploiement par extraction décrit tout type de déploiement dans lequel l’utilisateur final prend l’initiative d’installer les connecteurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="3b0fb-124">Les méthodes courantes de déploiement par extraction sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b0fb-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="3b0fb-125">Attachement du fichier. fichier osdx dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="3b0fb-126">Publication du fichier sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="3b0fb-127">Fournir un lien dynamique sur votre site intranet ; par exemple, un qui génère des fichiers. fichier osdx personnalisés en fonction des choix de l’utilisateur ou de l’étendue actuelle au sein du site.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="3b0fb-128">Pour que le fichier soit téléchargé lorsque l’utilisateur clique sur le lien dans son navigateur, le serveur Web qui héberge le service Web doit être configuré pour remettre le fichier. fichier osdx en tant que fichier.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="3b0fb-129">Par conséquent, vous devez configurer les types MIME sur le serveur Web pour traiter les fichiers. fichier osdx comme `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="3b0fb-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="3b0fb-130">Si vous le souhaitez, vous pouvez utiliser l’icône fournie par Microsoft pour identifier le lien du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="3b0fb-131">Déploiement Push</span><span class="sxs-lookup"><span data-stu-id="3b0fb-131">Push Deployment</span></span>

<span data-ttu-id="3b0fb-132">Déploiement Push décrit tout type de déploiement qui ne dépend pas de l’initiative de l’utilisateur pour installer les connecteurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="3b0fb-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="3b0fb-133">Les méthodes courantes de déploiement Push sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b0fb-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="3b0fb-134">Préférences de stratégie de groupe (Préférences)</span><span class="sxs-lookup"><span data-stu-id="3b0fb-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="3b0fb-135">Script d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="3b0fb-135">Logon script</span></span>
-   <span data-ttu-id="3b0fb-136">Profils d’itinérance</span><span class="sxs-lookup"><span data-stu-id="3b0fb-136">Roaming profiles</span></span>
-   <span data-ttu-id="3b0fb-137">Images</span><span class="sxs-lookup"><span data-stu-id="3b0fb-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="3b0fb-138">Suivi de l’utilisation</span><span class="sxs-lookup"><span data-stu-id="3b0fb-138">Tracking Usage</span></span>

<span data-ttu-id="3b0fb-139">Pour suivre l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) par les utilisateurs effectuant des recherches à partir de l’Explorateur Windows, filtrez les fichiers journaux de votre serveur Web pour cette chaîne d’agent utilisateur : `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="3b0fb-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b0fb-140">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3b0fb-140">Additional Resources</span></span>

<span data-ttu-id="3b0fb-141">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b0fb-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b0fb-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b0fb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0fb-143">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="3b0fb-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="3b0fb-144">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="3b0fb-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="3b0fb-145">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="3b0fb-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="3b0fb-146">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="3b0fb-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="3b0fb-147">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="3b0fb-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="3b0fb-148">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="3b0fb-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
