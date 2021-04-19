---
description: Explique comment permettre à votre magasin de données d’être accessible par un service Web OpenSearch et comment éviter les obstacles potentiels.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Activation de votre magasin de données dans la recherche fédérée Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516219"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="c065e-103">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="c065e-104">Explique comment permettre à votre magasin de données d’être accessible par un service Web [OpenSearch](https://github.com/dewitt/opensearch) et comment éviter les obstacles potentiels.</span><span class="sxs-lookup"><span data-stu-id="c065e-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="c065e-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c065e-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c065e-106">Conditions pour l’acceptation des demandes de recherche</span><span class="sxs-lookup"><span data-stu-id="c065e-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="c065e-107">Syntaxe de requête prise en charge</span><span class="sxs-lookup"><span data-stu-id="c065e-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="c065e-108">Protocoles d’authentification pris en charge</span><span class="sxs-lookup"><span data-stu-id="c065e-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="c065e-109">Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="c065e-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="c065e-110">Exemple de sortie d’un flux RSS</span><span class="sxs-lookup"><span data-stu-id="c065e-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="c065e-111">Mappage automatique aux propriétés de l’interpréteur de commandes Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="c065e-112">Comprendre comment Windows mappe les éléments aux types de fichiers</span><span class="sxs-lookup"><span data-stu-id="c065e-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="c065e-113">Éviter les obstacles potentiels à l’activation d’un magasin de données</span><span class="sxs-lookup"><span data-stu-id="c065e-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="c065e-114">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c065e-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c065e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c065e-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="c065e-116">Conditions pour l’acceptation des demandes de recherche</span><span class="sxs-lookup"><span data-stu-id="c065e-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="c065e-117">Le service Web [OpenSearch](https://github.com/dewitt/opensearch) que vous créez sur votre serveur Web **doit** répondre aux deux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c065e-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="c065e-118">Pouvoir accepter une `GET URL` requête du client.</span><span class="sxs-lookup"><span data-stu-id="c065e-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="c065e-119">Autorisez l’incorporation des termes de recherche dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="c065e-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="c065e-120">L’exemple suivant montre comment un terme de recherche peut être incorporé dans une URL.</span><span class="sxs-lookup"><span data-stu-id="c065e-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="c065e-121">La recherche fédérée ne prend pas en charge l’envoi `POST` de demandes à un service Web.</span><span class="sxs-lookup"><span data-stu-id="c065e-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="c065e-122">Pour plus d’informations sur la construction d’une URL, consultez « Paramètres de modèle d’URL » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="c065e-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="c065e-123">Syntaxe de requête prise en charge</span><span class="sxs-lookup"><span data-stu-id="c065e-123">Supported Query Syntax</span></span>

<span data-ttu-id="c065e-124">Aucune syntaxe de requête spécifique n’est attendue dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c065e-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="c065e-125">Le fournisseur OpenSearch accepte les termes que l’utilisateur entre dans la zone d’entrée dans l’Explorateur Windows et l’encode dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="c065e-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="c065e-126">Elle le fait en fonction du modèle d’URL décrit dans « paramètres de modèle d’URL » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="c065e-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="c065e-127">Les utilisateurs s’attendent à ce que des termes distincts soient traités comme des liés implicites.</span><span class="sxs-lookup"><span data-stu-id="c065e-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="c065e-128">Par exemple, une requête pour « Microsoft Windows » doit renvoyer uniquement les résultats qui contiennent à la fois « Windows » et « Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="c065e-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="c065e-129">Protocoles d’authentification pris en charge</span><span class="sxs-lookup"><span data-stu-id="c065e-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="c065e-130">La recherche fédérée Windows prend en charge l’authentification Windows et peut fournir des informations d’identification aux services Web via les protocoles suivants :</span><span class="sxs-lookup"><span data-stu-id="c065e-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="c065e-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="c065e-131">NTLM.</span></span>
-   <span data-ttu-id="c065e-132">Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c065e-132">Kerberos.</span></span>
-   <span data-ttu-id="c065e-133">De base (uniquement via HTTPS).</span><span class="sxs-lookup"><span data-stu-id="c065e-133">Basic (only over https).</span></span>
-   <span data-ttu-id="c065e-134">Autres fournisseurs de support de sécurité (SSP) installés sur Windows qui fournissent une capacité d’interrogation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c065e-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="c065e-135">Consultez la documentation du kit de développement logiciel (SDK) de l' [interface SSP](../secauthn/sspi.md) pour vous tenir informé de l’ajout potentiel d’autres ssp.</span><span class="sxs-lookup"><span data-stu-id="c065e-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="c065e-136">Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="c065e-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="c065e-137">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) est chargé de mapper les valeurs des éléments XML aux propriétés système du shell Windows qui peuvent être utilisées par les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="c065e-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="c065e-138">Toutefois, vous n’êtes pas limité aux mappages par défaut des éléments RSS ou Atom standard et vous pouvez inclure des éléments XML personnalisés dans l’espace de noms Windows pour chacune des propriétés.</span><span class="sxs-lookup"><span data-stu-id="c065e-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="c065e-139">Par exemple, vous pouvez ajouter vos propres éléments XML personnalisés dans l’élément **Item** pour fournir des métadonnées supplémentaires à Windows.</span><span class="sxs-lookup"><span data-stu-id="c065e-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="c065e-140">Vous pouvez également mapper des éléments à partir d’autres espaces de noms XML, tels que iTunes</span><span class="sxs-lookup"><span data-stu-id="c065e-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="c065e-141">Exemple de sortie d’un flux RSS</span><span class="sxs-lookup"><span data-stu-id="c065e-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="c065e-142">L’exemple de sortie de flux RSS suivant retourne un élément.</span><span class="sxs-lookup"><span data-stu-id="c065e-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="c065e-143">Pour plus d’informations sur le mappage de propriété, consultez les sections « éléments étendus dans WIndows Federated Search » et « mappages de propriétés personnalisées » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="c065e-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="c065e-144">Mappage automatique aux propriétés de l’interpréteur de commandes Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="c065e-145">Dans les éléments de votre flux RSS, vous pouvez choisir d’inclure d’autres éléments XML qui sont automatiquement mappés aux propriétés du système de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="c065e-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="c065e-146">Pour ce faire, incluez un élément nommé après la propriété de l’interpréteur de commandes Windows et préfixé avec l’espace de noms du système Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="c065e-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="c065e-147">L’exemple suivant illustre la déclaration d’espace de noms `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` et l’inclusion d’un élément pour le mappage de propriété `win:System.Contact.PrimaryEmailAddress` :</span><span class="sxs-lookup"><span data-stu-id="c065e-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="c065e-148">Le préfixe d’espace de noms utilisé ici ( `"win"` ) est une suggestion ; vous pouvez utiliser n’importe quel préfixe.</span><span class="sxs-lookup"><span data-stu-id="c065e-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="c065e-149">Toutefois, vous devez utiliser les noms exacts des propriétés de l’interpréteur de commandes Windows et vous devez inclure le Uniform Resource Identifier (URI) exact, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c065e-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="c065e-150">**À propos des propriétés système du shell Windows**</span><span class="sxs-lookup"><span data-stu-id="c065e-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="c065e-151">Windows définit une liste complète des [Propriétés système](../properties/props.md) et le format de type valeur requis pour chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="c065e-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="c065e-152">La documentation de la propriété de l’interpréteur de commandes de la fenêtre [System. FileExtension](../properties/props-system-fileextension.md) , par exemple, spécifie que la valeur doit contenir le point de début (". docx" et non "docx").</span><span class="sxs-lookup"><span data-stu-id="c065e-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="c065e-153">**Valeurs Date et heure**</span><span class="sxs-lookup"><span data-stu-id="c065e-153">**Date and Time Values**</span></span>

<span data-ttu-id="c065e-154">Le format de date et d’heure par défaut est ISO-8601, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c065e-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="c065e-155">Les développeurs .NET doivent utiliser la classe DateTime avec `ToString("R") ` pour générer le format correct.</span><span class="sxs-lookup"><span data-stu-id="c065e-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="c065e-156">Pour plus d’informations sur le mappage de propriété, consultez « éléments étendus dans la recherche fédérée Windows » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="c065e-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="c065e-157">Comprendre comment Windows mappe les éléments aux types de fichiers</span><span class="sxs-lookup"><span data-stu-id="c065e-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="c065e-158">La recherche dans l’interface utilisateur de l’Explorateur Windows permet aux utilisateurs de traiter les résultats comme des fichiers lorsqu’un élément RSS pointe vers un fichier stocké à distance.</span><span class="sxs-lookup"><span data-stu-id="c065e-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="c065e-159">L’utilisateur peut glisser-déplacer des éléments sur le bureau, et l’interface utilisateur de l’Explorateur Windows affiche l’icône correcte et fournit le menu contextuel approprié.</span><span class="sxs-lookup"><span data-stu-id="c065e-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="c065e-160">Si l’élément RSS ne pointe pas vers un fichier stocké à distance, le fichier est traité comme un lien et les utilisateurs peuvent effectuer des actions sur celui-ci, par exemple créer un raccourci ou l’ouvrir dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="c065e-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="c065e-161">L’organigramme suivant montre comment Windows détermine le type de fichier d’un élément.</span><span class="sxs-lookup"><span data-stu-id="c065e-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![Organigramme présentant les chemins d’accès d’un élément aux décisions pour le traiter en tant qu’élément de type de lien Web ou en tant que type de fichier](images/determineanitemfiletype.png)

<span data-ttu-id="c065e-163">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) effectue les étapes suivantes pour mapper un élément à un type de fichier :</span><span class="sxs-lookup"><span data-stu-id="c065e-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="c065e-164">Identifiez si l’élément doit être traité comme un fichier ou un lien Web.</span><span class="sxs-lookup"><span data-stu-id="c065e-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="c065e-165">Identifiez l’extension de nom de fichier correcte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c065e-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="c065e-166">Par exemple, si l’élément a une URL de lien qui utilise un chemin d’accès de système de fichiers (tel que `file:///\\server\share\etc\item.ext` ), le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) traite le lien comme un fichier et détermine le type en fonction de l’extension de nom de fichier utilisée dans le chemin d’accès (. ext dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="c065e-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="c065e-167">Si l’élément utilise le boîtier RSS standard ou **MediaRSS Media : content** , le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) suppose que l’élément est un fichier et identifie l’extension de nom de fichier comme suit :</span><span class="sxs-lookup"><span data-stu-id="c065e-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="c065e-168">Si la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) a été mappée pour l’élément, le fournisseur utilise cette extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c065e-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="c065e-169">Si la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) n’a pas été mappée, le fournisseur utilise l’attribut **type** spécifié dans le boîtier ou l’élément de contenu.</span><span class="sxs-lookup"><span data-stu-id="c065e-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="c065e-170">Cet élément doit contenir une `MIMEType` chaîne, telle que `"image/jpeg"` .</span><span class="sxs-lookup"><span data-stu-id="c065e-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="c065e-171">Si le `MIMEType` est associé à une extension de nom de fichier inscrite sur l’ordinateur client, l’élément est considéré comme un fichier de ce type.</span><span class="sxs-lookup"><span data-stu-id="c065e-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="c065e-172">Si le `MIMEType` n’est pas associé à une extension de nom de fichier inscrite sur l’ordinateur client, l’élément est traité comme un type de lien Web.</span><span class="sxs-lookup"><span data-stu-id="c065e-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="c065e-173">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) n’essaie pas d’analyser l’attribut **URL** pour localiser l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c065e-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="c065e-174">Si le `MIMEType` est associé à une extension de nom de fichier inscrite sur l’ordinateur client, le fournisseur détermine si l’extension de nom de fichier est un type de fichier Web connu (. htm,. html,. asp,. aspx,. php,. swf,. stm).</span><span class="sxs-lookup"><span data-stu-id="c065e-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="c065e-175">Dans ce cas, le type de fichier est considéré comme un type de lien Web ; dans le cas contraire, il est considéré comme un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="c065e-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="c065e-176">Par exemple, si le `MIMEType "text/html"` est associé à l’extension de nom de fichier. htm, cet élément est considéré comme un lien Web et non comme un type de fichier. htm.</span><span class="sxs-lookup"><span data-stu-id="c065e-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="c065e-177">Éviter les obstacles potentiels à l’activation d’un magasin de données</span><span class="sxs-lookup"><span data-stu-id="c065e-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="c065e-178">Certains magasins de données ne fournissent pas de service Web compatible [OpenSearch](https://github.com/dewitt/opensearch), mais ils peuvent toujours être connectés à Windows Federated Search.</span><span class="sxs-lookup"><span data-stu-id="c065e-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="c065e-179">Ces magasins de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c065e-179">Such data stores include:</span></span>

-   <span data-ttu-id="c065e-180">Les index distants avec des méthodes d’authentification qui ne sont pas prises en charge dans la recherche fédérée de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c065e-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="c065e-181">Les exemples incluent l’authentification basée sur les formulaires et d’autres méthodes d’authentification personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c065e-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="c065e-182">Si un magasin public de valeur élevée possède des API Web publiques, n’importe qui peut écrire un autre service Web compatible [OpenSearch](https://github.com/dewitt/opensearch)et appelle ces API en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c065e-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="c065e-183">Exemples : la bibliothèque de congrès et les bases de données de recherche médicale.</span><span class="sxs-lookup"><span data-stu-id="c065e-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="c065e-184">Les magasins de données d’entreprise propriétaires, les index et les magasins de gestion de contenu hérités, pour lesquels il peut être impossible d’implémenter un serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="c065e-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="c065e-185">Toutefois, il existe des alternatives qui peuvent éviter les obstacles à l’activation d’un magasin de données.</span><span class="sxs-lookup"><span data-stu-id="c065e-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="c065e-186">Voici quelques-unes de ces alternatives :</span><span class="sxs-lookup"><span data-stu-id="c065e-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="c065e-187">**Pour écrire un service Web intermédiaire lorsque vous ne pouvez pas modifier le service Web pour la source de données existante, ou si le service Web fournit une API personnalisée :**</span><span class="sxs-lookup"><span data-stu-id="c065e-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="c065e-188">Écrire un service Web intermédiaire qui peut accepter une requête Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c065e-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="c065e-189">Connectez-vous à votre source de données et récupérez les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="c065e-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="c065e-190">Reformatez les résultats au format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="c065e-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="c065e-191">Retournez les résultats au client Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c065e-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="c065e-192">Notez que pour les services de données d’entreprise et de nombreux services de données Internet, vous devrez peut-être transmettre les informations d’identification de l’utilisateur via pour le compte du service Web afin d’effectuer une suppression des résultats en fonction des autorisations de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c065e-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="c065e-193">**Pour utiliser un moteur de recherche existant lorsque vous ne pouvez pas activer un magasin de données public :**</span><span class="sxs-lookup"><span data-stu-id="c065e-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="c065e-194">Utilisez un moteur de recherche public qui prend déjà en charge [OpenSearch](https://github.com/dewitt/opensearch) avec RSS.</span><span class="sxs-lookup"><span data-stu-id="c065e-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="c065e-195">Pour ce faire, vous devez fournir à vos utilisateurs un fichier. fichier osdx avec un modèle d’URL qui limite les résultats à ceux de votre domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="c065e-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="c065e-196">Consultez l’exemple suivant d’une description [OpenSearch](https://github.com/dewitt/opensearch) pour rechercher uniquement le contenu d’aide pour Windows à l’aide d’une requête sur Live.com.</span><span class="sxs-lookup"><span data-stu-id="c065e-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="c065e-197">**Pour utiliser un serveur d’indexation existant qui prend en charge OpenSearch quand vous ne pouvez pas activer des magasins de données d’entreprise propriétaires ou des index :**</span><span class="sxs-lookup"><span data-stu-id="c065e-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="c065e-198">Sélectionnez un serveur d’indexation existant qui prend en charge [OpenSearch](https://github.com/dewitt/opensearch) pour indexer votre contenu, tel que le serveur de recherche SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c065e-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="c065e-199">Créez un fichier. fichier osdx qui limite les résultats de l’index SharePoint à ceux de votre serveur à l’aide de leur syntaxe de mot clé dans le modèle d’URL.</span><span class="sxs-lookup"><span data-stu-id="c065e-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="c065e-200">**Pour écrire une banque de données côté client si une solution côté serveur uniquement ne fonctionne pas :**</span><span class="sxs-lookup"><span data-stu-id="c065e-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="c065e-201">Écrivez une source de données [OpenSearch](https://github.com/dewitt/opensearch) côté client qui se situe entre le fournisseur Windows [OpenSearch](https://github.com/dewitt/opensearch) et la source de données externe.</span><span class="sxs-lookup"><span data-stu-id="c065e-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="c065e-202">Utilisez l’API de l' [interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) dans la SDK Windows pour créer un fichier. searchconnector-MS correctement configuré par le biais duquel l’Explorateur Windows peut appeler votre implémentation avec les paramètres de requête.</span><span class="sxs-lookup"><span data-stu-id="c065e-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="c065e-203">Votre implémentation peut ensuite retourner des résultats au format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="c065e-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="c065e-204">Cela permet à votre implémentation de fournir une interface utilisateur d’authentification personnalisée et de se connecter à la source de données à l’aide de son API propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c065e-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="c065e-205">L’ouverture d’un fichier. fichier osdx crée un fichier. searchconnector-ms (connecteur de recherche) dans le répertoire% USERPROFILE%/Searches et y place un lien dans le répertoire% USERPROFILE%/links.</span><span class="sxs-lookup"><span data-stu-id="c065e-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="c065e-206">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c065e-206">Additional Resources</span></span>

<span data-ttu-id="c065e-207">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c065e-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c065e-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c065e-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c065e-209">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="c065e-210">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="c065e-211">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="c065e-212">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="c065e-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="c065e-213">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="c065e-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="c065e-214">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="c065e-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
