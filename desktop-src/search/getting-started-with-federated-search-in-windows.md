---
description: La prise en charge de Windows 7 pour la Fédération des recherches dans des magasins de données distants à l’aide des technologies OpenSearch permet aux utilisateurs d’accéder à leurs données distantes à partir de l’Explorateur Windows.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Prise en main avec la recherche fédérée dans Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525468"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="b9d44-103">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="b9d44-104">La prise en charge de Windows 7 pour la Fédération des recherches dans des magasins de données distants à l’aide des technologies OpenSearch permet aux utilisateurs d’accéder à leurs données distantes à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="b9d44-105">Vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et permettre une intégration enrichie de vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou déployer de code côté client Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="b9d44-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9d44-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b9d44-107">Qu’est-ce que la recherche fédérée ?</span><span class="sxs-lookup"><span data-stu-id="b9d44-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="b9d44-108">Étapes de création d’une recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="b9d44-109">Fonctionnement de la recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="b9d44-110">Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="b9d44-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="b9d44-111">Exemples de recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="b9d44-112">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b9d44-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b9d44-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9d44-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="b9d44-114">Qu’est-ce que la recherche fédérée ?</span><span class="sxs-lookup"><span data-stu-id="b9d44-114">What is Federated Search?</span></span>

<span data-ttu-id="b9d44-115">Windows 7 prend en charge la connexion de sources externes au client Windows via le protocole [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="b9d44-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="b9d44-116">Cela permet aux utilisateurs de rechercher dans un magasin de données distant et d’afficher les résultats à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="b9d44-117">Le standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 définit des formats de fichiers simples qui peuvent être utilisés pour décrire comment un client doit interroger le service Web pour le magasin de données et comment le service doit retourner les résultats à afficher par le client.</span><span class="sxs-lookup"><span data-stu-id="b9d44-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="b9d44-118">La recherche fédérée Windows se connecte aux services Web qui reçoivent des requêtes [OpenSearch](https://github.com/dewitt/opensearch) et retourne les résultats au format RSS ou Atom XML.</span><span class="sxs-lookup"><span data-stu-id="b9d44-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="b9d44-119">La capture d’écran suivante illustre les résultats de recherche obtenus après la recherche à distance sur un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b9d44-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![capture d’écran qui affiche les résultats de la recherche à partir d’un site SharePoint tel qu’il apparaît dans l’Explorateur Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="b9d44-121">Étapes de création d’une recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="b9d44-122">Pour créer une recherche fédérée, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9d44-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="b9d44-123">Autorisez la recherche dans votre banque de données à partir de l’Explorateur Windows en fournissant un service Web compatible [OpenSearch](https://github.com/dewitt/opensearch)qui peut retourner des résultats au format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="b9d44-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="b9d44-124">Créez un fichier de description OpenSearch (. fichier osdx) qui décrit comment se connecter au service Web et comment mapper des éléments personnalisés dans votre fichier XML RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="b9d44-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="b9d44-125">Déployez les connecteurs de recherche sur les ordinateurs clients Windows avec un fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="b9d44-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="b9d44-126">Le diagramme suivant illustre les étapes de création d’une recherche fédérée.</span><span class="sxs-lookup"><span data-stu-id="b9d44-126">The following diagram illustrates the steps for building federated search.</span></span>

![diagramme du processus de création d’une recherche fédérée](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="b9d44-128">Fonctionnement de la recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-128">How Federated Search Works</span></span>

<span data-ttu-id="b9d44-129">La communication entre l’Explorateur Windows et votre service Web [OpenSearch](https://github.com/dewitt/opensearch) s’effectue via la couche de données Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="b9d44-130">La couche de données Windows peut communiquer avec différents types de magasins de données via des fournisseurs Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b9d44-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="b9d44-131">Chaque fournisseur est spécialisé dans la communication avec les magasins de données qui prennent en charge un protocole particulier et qui possèdent des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b9d44-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="b9d44-132">Par exemple, l’illustration suivante explique comment le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) communique avec les magasins de données qui fournissent un service Web qui prend en charge la norme [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="b9d44-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![Diagramme montrant la communication à partir de l’Explorateur Windows sur le client via le magasin de données OpenSearch sur le serveur distant](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="b9d44-134">Pour permettre à votre magasin de données de prendre en charge la recherche fédérée dans Windows 7, vous devez effectuer un certain nombre de tâches.</span><span class="sxs-lookup"><span data-stu-id="b9d44-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="b9d44-135">Le tableau suivant répertorie les tâches d’activation de votre magasin de données, ce qui est nécessaire pour accomplir chaque tâche et où trouver de la documentation.</span><span class="sxs-lookup"><span data-stu-id="b9d44-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="b9d44-136">Tâche</span><span class="sxs-lookup"><span data-stu-id="b9d44-136">Task</span></span>                                                                                                     | <span data-ttu-id="b9d44-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9d44-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="b9d44-138">Documentation</span><span class="sxs-lookup"><span data-stu-id="b9d44-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d44-139">Activez la recherche de votre banque de données par l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="b9d44-140">Créez un service Web compatible OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="b9d44-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="b9d44-141">Créez un fichier de description OpenSearch (. fichier osdx).</span><span class="sxs-lookup"><span data-stu-id="b9d44-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="b9d44-142">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="b9d44-143">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="b9d44-144">Déployez activement votre service Web pour les utilisateurs au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="b9d44-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="b9d44-145">Fournissez un fichier. fichier osdx à vos utilisateurs, copiez-le localement et rendez-le accessible à l’utilisateur via un raccourci.</span><span class="sxs-lookup"><span data-stu-id="b9d44-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="b9d44-146">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="b9d44-147">Énumérer les résultats de la recherche dans l’Explorateur Windows en réponse à une requête.</span><span class="sxs-lookup"><span data-stu-id="b9d44-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="b9d44-148">Implémentez un service Web qui accepte une chaîne de requête et retourne les résultats au format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="b9d44-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="b9d44-149">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="b9d44-150">Permettre aux utilisateurs d’ajouter votre magasin de données à leur Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="b9d44-151">Créez un fichier. fichier osdx et fournissez-le à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b9d44-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="b9d44-152">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="b9d44-153">Affichez vos éléments en tant qu’éléments de type fichier dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="b9d44-154">Retourner une URL vers le fichier ou le flux de contenu à l’aide d’un **boîtier** ou d’un **média :** éléments de contenu</span><span class="sxs-lookup"><span data-stu-id="b9d44-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="b9d44-155">Fournissez une extension de nom de fichier ou un type MIME que l’ordinateur client reconnaît.</span><span class="sxs-lookup"><span data-stu-id="b9d44-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="b9d44-156">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="b9d44-157">Affichez les propriétés personnalisées dans l’Explorateur Windows, au-delà de celles définies dans les normes RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="b9d44-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="b9d44-158">Fournir des métadonnées supplémentaires à l’aide d’un autre espace de noms XML dans votre sortie RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="b9d44-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="b9d44-159">Ajoutez un mappage des propriétés à votre fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="b9d44-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="b9d44-160">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b9d44-161">Personnaliser les propriétés affichées pour vos éléments dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="b9d44-162">Ajoutez des mappages PropList à votre fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="b9d44-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="b9d44-163">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b9d44-164">Affichez une vue de page Web personnalisée de vos éléments dans le volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="b9d44-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="b9d44-165">Retourne des valeurs de lien et de boîtier distinctes.</span><span class="sxs-lookup"><span data-stu-id="b9d44-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="b9d44-166">Mappez une valeur d’URL à la propriété de l’interpréteur de commandes Windows **System. WebPreviewUrl** .</span><span class="sxs-lookup"><span data-stu-id="b9d44-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="b9d44-167">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b9d44-168">Affichez un bouton de barre de commandes dans l’Explorateur Windows qui restaure la requête sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="b9d44-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="b9d44-169">Fournissez un `Url format="text/html"` modèle dans le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="b9d44-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="b9d44-170">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="b9d44-171">Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="b9d44-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="b9d44-172">Lorsque l’utilisateur tape un terme dans la zone de recherche dans l’angle supérieur droit de l’Explorateur Windows, la requête est envoyée au fournisseur [OpenSearch](https://github.com/dewitt/opensearch) , qui envoie ensuite la requête au magasin de données distant.</span><span class="sxs-lookup"><span data-stu-id="b9d44-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="b9d44-173">Le service Web distant répond à la requête en fournissant des résultats dans un document XML, généralement appelé flux, dans l’un des deux formats pris en charge (RSS ou Atom).</span><span class="sxs-lookup"><span data-stu-id="b9d44-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="b9d44-174">Chaque élément de résultat dans le flux contient des éléments enfants XML pour représenter ou décrire des métadonnées d’élément, telles que le titre, l’URL, la description, l’image miniature, etc.</span><span class="sxs-lookup"><span data-stu-id="b9d44-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="b9d44-175">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) est chargé de mapper les valeurs des éléments XML aux propriétés système du shell Windows qui peuvent être utilisées par les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="b9d44-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="b9d44-176">Exemples de recherche fédérée</span><span class="sxs-lookup"><span data-stu-id="b9d44-176">Federated Search Examples</span></span>

<span data-ttu-id="b9d44-177">L’exemple suivant de fichier de description OpenSearch (. fichier osdx) se compose des `ShortName` `Url` éléments et, qui sont les éléments enfants requis minimum pour connecter un magasin de données externe au client Windows via le protocole OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="b9d44-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="b9d44-178">L’exemple suivant montre comment effectuer une recherche dans un magasin de données compatible avec le Web au format RSS et comment spécifier qu’un élément de recherche doit être retourné :</span><span class="sxs-lookup"><span data-stu-id="b9d44-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="b9d44-179">L’exemple suivant montre comment mapper des propriétés à des propriétés système par défaut afin que les éléments affichés soient triés et regroupés :</span><span class="sxs-lookup"><span data-stu-id="b9d44-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="b9d44-180">L’exemple suivant montre comment ajouter un affichage d’image miniature à chaque élément dans l’Explorateur Windows :</span><span class="sxs-lookup"><span data-stu-id="b9d44-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="b9d44-181">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b9d44-181">Additional Resources</span></span>

<span data-ttu-id="b9d44-182">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b9d44-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9d44-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9d44-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9d44-184">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b9d44-185">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="b9d44-186">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b9d44-187">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="b9d44-188">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="b9d44-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="b9d44-189">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="b9d44-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




