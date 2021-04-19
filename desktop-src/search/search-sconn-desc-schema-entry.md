---
description: Présente le schéma de description du connecteur de recherche utilisé par les bibliothèques de l’Explorateur Windows et les fournisseurs de recherche fédérés.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Schéma de la description du connecteur de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515210"
---
# <a name="search-connector-description-schema"></a><span data-ttu-id="bc970-103">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="bc970-103">Search Connector Description Schema</span></span>

<span data-ttu-id="bc970-104">Présente le schéma de description du connecteur de recherche utilisé par les bibliothèques de l’Explorateur Windows et les fournisseurs de recherche fédérés.</span><span class="sxs-lookup"><span data-stu-id="bc970-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="bc970-105">Le schéma spécifie la structure et la configuration requise pour les fichiers de description du connecteur de recherche ( \* . searchConnector-ms) et pour les éléments **searchConnectorDescriptionType** des fichiers de description de la bibliothèque de l’interpréteur de commandes ( \* . Library-ms).</span><span class="sxs-lookup"><span data-stu-id="bc970-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="bc970-106">Cette rubrique décrit le schéma en ce qui concerne les connecteurs de recherche fédérés.</span><span class="sxs-lookup"><span data-stu-id="bc970-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="bc970-107">Pour plus d’informations sur les bibliothèques et le schéma de description de la bibliothèque, consultez [schéma de description](../shell/library-schema-entry.md)de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bc970-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="bc970-108">Cette rubrique comporte les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc970-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="bc970-109">Que sont les connecteurs de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="bc970-110">Comment fonctionnent les fichiers de description du connecteur de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="bc970-111">Qu’est-ce que le schéma de description du connecteur de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="bc970-112">Quelles sont les principales parties du schéma ?</span><span class="sxs-lookup"><span data-stu-id="bc970-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="bc970-113">Exemples de fichiers de description de connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="bc970-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="bc970-114">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bc970-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="bc970-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc970-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="bc970-116">Que sont les connecteurs de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-116">What Are Search Connectors?</span></span>

<span data-ttu-id="bc970-117">Les connecteurs de recherche connectent les utilisateurs aux données stockées dans les services Web ou les emplacements de stockage distant.</span><span class="sxs-lookup"><span data-stu-id="bc970-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="bc970-118">Avec Windows 7, les utilisateurs peuvent installer des connecteurs de recherche pour des emplacements tels que des services Web, afin qu’ils recherchent ces emplacements directement à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="bc970-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="bc970-119">Les connecteurs de recherche sont des fichiers de description de connecteur de recherche ( \* . searchConnector-ms) qui spécifient comment se connecter à, envoyer des requêtes à et recevoir des résultats de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="bc970-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="bc970-120">En plus des services Web, les connecteurs de recherche peuvent être utilisés pour rechercher des étendues d’index locales créées par des gestionnaires de protocole.</span><span class="sxs-lookup"><span data-stu-id="bc970-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="bc970-121">Par exemple, les utilisateurs peuvent rechercher des messages électroniques indexés localement avec le gestionnaire de protocole MAPI à l’aide d’un connecteur de recherche pour ce magasin de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="bc970-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="bc970-122">Comment fonctionnent les fichiers de description du connecteur de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="bc970-123">Lorsque la recherche de fichiers de description de connecteur est installée sur les systèmes des utilisateurs, les utilisateurs peuvent ouvrir l’Explorateur Windows, cliquer sur le connecteur de recherche dans le volet de navigation, puis entrer une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="bc970-124">L’Explorateur Windows envoie la requête à l’aide des informations du fichier de description du connecteur de recherche, telles que le fournisseur à utiliser et l’étendue de la recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="bc970-125">Les résultats sont retournés en tant qu’éléments de flux RSS ou Atom et affichés aux utilisateurs comme s’il s’agissait d’éléments de Shell normaux.</span><span class="sxs-lookup"><span data-stu-id="bc970-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="bc970-126">Le mode de déploiement du fichier de description du connecteur de recherche dépend du type d’emplacement pris en charge par le connecteur de recherche :</span><span class="sxs-lookup"><span data-stu-id="bc970-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="bc970-127">Dans un fichier de configuration OpenSearch ( \* . fichier osdx) pour votre service Web</span><span class="sxs-lookup"><span data-stu-id="bc970-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="bc970-128">Dans le cadre de l’installation du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="bc970-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="bc970-129">Vous devez vous assurer que les événements suivants se produisent lorsqu’un utilisateur ouvre le fichier. fichier osdx ou installe le gestionnaire de protocole :</span><span class="sxs-lookup"><span data-stu-id="bc970-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="bc970-130">Le fichier. searchconnector-MS est créé dans le dossier **recherches Windows** des utilisateurs (% UserProfile%/Searches).</span><span class="sxs-lookup"><span data-stu-id="bc970-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="bc970-131">Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier **des liens des** utilisateurs (% UserProfile%/Links).</span><span class="sxs-lookup"><span data-stu-id="bc970-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="bc970-132">Qu’est-ce que le schéma de description du connecteur de recherche ?</span><span class="sxs-lookup"><span data-stu-id="bc970-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="bc970-133">Le schéma de la description du connecteur de recherche est un schéma XML qui définit la structure des fichiers de description du connecteur de recherche ( \* . searchConnector-ms).</span><span class="sxs-lookup"><span data-stu-id="bc970-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="bc970-134">Chaque connecteur de recherche doit avoir un fichier de description de connecteur de recherche qui spécifie comment se connecter à, envoyer des requêtes à et recevoir des résultats de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="bc970-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="bc970-135">Quelles sont les principales parties du schéma ?</span><span class="sxs-lookup"><span data-stu-id="bc970-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="bc970-136">Le tableau suivant répertorie les principales parties du schéma.</span><span class="sxs-lookup"><span data-stu-id="bc970-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="bc970-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bc970-137">Child elements</span></span>                                                                         | <span data-ttu-id="bc970-138">Description</span><span class="sxs-lookup"><span data-stu-id="bc970-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc970-139">isSearchOnlyItem</span><span class="sxs-lookup"><span data-stu-id="bc970-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="bc970-140">Indique si les emplacements pris en charge par le connecteur de recherche sont uniquement de recherche ou de recherche et de navigation.</span><span class="sxs-lookup"><span data-stu-id="bc970-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="bc970-141">isDefaultSaveLocation</span><span class="sxs-lookup"><span data-stu-id="bc970-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="bc970-142">Pour l’utilisation de la bibliothèque uniquement.</span><span class="sxs-lookup"><span data-stu-id="bc970-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="bc970-143">isDefaultNonOwnerSaveLocation</span><span class="sxs-lookup"><span data-stu-id="bc970-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="bc970-144">Pour l’utilisation de la bibliothèque uniquement.</span><span class="sxs-lookup"><span data-stu-id="bc970-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="bc970-145">description</span><span class="sxs-lookup"><span data-stu-id="bc970-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="bc970-146">Décrit le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="bc970-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="bc970-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="bc970-148">Identifie l’emplacement d’une icône personnalisée pour le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="bc970-149">imageLink</span><span class="sxs-lookup"><span data-stu-id="bc970-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="bc970-150">Identifie l’emplacement d’une miniature personnalisée pour le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="bc970-151">auteur</span><span class="sxs-lookup"><span data-stu-id="bc970-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="bc970-152">Identifie l’auteur du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="bc970-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="bc970-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="bc970-154">Identifie la date à laquelle le connecteur de recherche a été créé.</span><span class="sxs-lookup"><span data-stu-id="bc970-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="bc970-155">templateInfo</span><span class="sxs-lookup"><span data-stu-id="bc970-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="bc970-156">Spécifie un type de dossier pour le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="bc970-157">locationProvider</span><span class="sxs-lookup"><span data-stu-id="bc970-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="bc970-158">Spécifie le moteur de recherche à utiliser par ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="bc970-159">scope</span><span class="sxs-lookup"><span data-stu-id="bc970-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="bc970-160">Spécifie les emplacements à inclure dans l’étendue de recherche et à exclure de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="bc970-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="bc970-161">propertyStore</span><span class="sxs-lookup"><span data-stu-id="bc970-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="bc970-162">Spécifie l’emplacement d’un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basé sur XML pour ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="bc970-163">**IPropertyStore** prend en charge les métadonnées ouvertes du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="bc970-164">includeInStartMenuScope</span><span class="sxs-lookup"><span data-stu-id="bc970-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="bc970-165">Spécifie si l’emplacement représenté par le connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="bc970-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="bc970-166">Domain</span><span class="sxs-lookup"><span data-stu-id="bc970-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="bc970-167">Identifie le domaine de premier niveau du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc970-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="bc970-168">supportsAdvancedQuerySyntax</span><span class="sxs-lookup"><span data-stu-id="bc970-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="bc970-169">Spécifie si le connecteur de recherche prend en charge la syntaxe de requête avancée (AQS).</span><span class="sxs-lookup"><span data-stu-id="bc970-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="bc970-170">isIndexed</span><span class="sxs-lookup"><span data-stu-id="bc970-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="bc970-171">Spécifie si l’emplacement représenté par le connecteur de recherche est indexé.</span><span class="sxs-lookup"><span data-stu-id="bc970-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="bc970-172">Exemples de fichiers de description de connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="bc970-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="bc970-173">Voici un exemple de fichier de description de connecteur de recherche pour un service Web de recherche fédérée.</span><span class="sxs-lookup"><span data-stu-id="bc970-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="bc970-174">Voici un exemple de fichier de description de connecteur de recherche pour un gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="bc970-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a><span data-ttu-id="bc970-175">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bc970-175">Additional Resources</span></span>

-   <span data-ttu-id="bc970-176">Pour plus d’informations sur le schéma de description de la bibliothèque, consultez [schéma de description](../shell/library-schema-entry.md)de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bc970-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="bc970-177">Pour plus d’informations sur l’installation d’un connecteur de recherche, consultez [recherche fédérée dans Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bc970-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc970-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc970-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc970-179">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="bc970-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc970-180">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="bc970-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="bc970-181">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="bc970-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bc970-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="bc970-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="bc970-183">Centre de téléchargement Microsoft</span><span class="sxs-lookup"><span data-stu-id="bc970-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
