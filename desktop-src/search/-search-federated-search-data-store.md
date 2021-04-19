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
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Activation de votre magasin de données dans la recherche fédérée Windows

Explique comment permettre à votre magasin de données d’être accessible par un service Web [OpenSearch](https://github.com/dewitt/opensearch) et comment éviter les obstacles potentiels.

Cette rubrique est organisée comme suit :

-   [Conditions pour l’acceptation des demandes de recherche](#conditions-for-search-request-acceptance)
    -   [Syntaxe de requête prise en charge](#supported-query-syntax)
    -   [Protocoles d’authentification pris en charge](#supported-authentication-protocols)
-   [Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Exemple de sortie d’un flux RSS](#example-of-an-rss-feed-output)
-   [Mappage automatique aux propriétés de l’interpréteur de commandes Windows](#automatic-mapping-to-windows-shell-properties)
-   [Comprendre comment Windows mappe les éléments aux types de fichiers](#understanding-how-windows-maps-items-to-file-types)
-   [Éviter les obstacles potentiels à l’activation d’un magasin de données](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Conditions pour l’acceptation des demandes de recherche

Le service Web [OpenSearch](https://github.com/dewitt/opensearch) que vous créez sur votre serveur Web **doit** répondre aux deux conditions suivantes :

-   Pouvoir accepter une `GET URL` requête du client.
-   Autorisez l’incorporation des termes de recherche dans l’URL.

    L’exemple suivant montre comment un terme de recherche peut être incorporé dans une URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> La recherche fédérée ne prend pas en charge l’envoi `POST` de demandes à un service Web.

 

Pour plus d’informations sur la construction d’une URL, consultez « Paramètres de modèle d’URL » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Syntaxe de requête prise en charge

Aucune syntaxe de requête spécifique n’est attendue dans Windows 7. Le fournisseur OpenSearch accepte les termes que l’utilisateur entre dans la zone d’entrée dans l’Explorateur Windows et l’encode dans l’URL. Elle le fait en fonction du modèle d’URL décrit dans « paramètres de modèle d’URL » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).

Les utilisateurs s’attendent à ce que des termes distincts soient traités comme des liés implicites. Par exemple, une requête pour « Microsoft Windows » doit renvoyer uniquement les résultats qui contiennent à la fois « Windows » et « Microsoft ».

### <a name="supported-authentication-protocols"></a>Protocoles d’authentification pris en charge

La recherche fédérée Windows prend en charge l’authentification Windows et peut fournir des informations d’identification aux services Web via les protocoles suivants :

-   NTLM.
-   Kerberos.
-   De base (uniquement via HTTPS).
-   Autres fournisseurs de support de sécurité (SSP) installés sur Windows qui fournissent une capacité d’interrogation supplémentaire. Consultez la documentation du kit de développement logiciel (SDK) de l' [interface SSP](../secauthn/sspi.md) pour vous tenir informé de l’ajout potentiel d’autres ssp.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom

Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) est chargé de mapper les valeurs des éléments XML aux propriétés système du shell Windows qui peuvent être utilisées par les applications Windows. Toutefois, vous n’êtes pas limité aux mappages par défaut des éléments RSS ou Atom standard et vous pouvez inclure des éléments XML personnalisés dans l’espace de noms Windows pour chacune des propriétés. Par exemple, vous pouvez ajouter vos propres éléments XML personnalisés dans l’élément **Item** pour fournir des métadonnées supplémentaires à Windows. Vous pouvez également mapper des éléments à partir d’autres espaces de noms XML, tels que iTunes

### <a name="example-of-an-rss-feed-output"></a>Exemple de sortie d’un flux RSS

L’exemple de sortie de flux RSS suivant retourne un élément.


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



Pour plus d’informations sur le mappage de propriété, consultez les sections « éléments étendus dans WIndows Federated Search » et « mappages de propriétés personnalisées » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Mappage automatique aux propriétés de l’interpréteur de commandes Windows

Dans les éléments de votre flux RSS, vous pouvez choisir d’inclure d’autres éléments XML qui sont automatiquement mappés aux propriétés du système de l’interpréteur de commandes Windows. Pour ce faire, incluez un élément nommé après la propriété de l’interpréteur de commandes Windows et préfixé avec l’espace de noms du système Windows Shell. L’exemple suivant illustre la déclaration d’espace de noms `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` et l’inclusion d’un élément pour le mappage de propriété `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



Le préfixe d’espace de noms utilisé ici ( `"win"` ) est une suggestion ; vous pouvez utiliser n’importe quel préfixe. Toutefois, vous devez utiliser les noms exacts des propriétés de l’interpréteur de commandes Windows et vous devez inclure le Uniform Resource Identifier (URI) exact, comme indiqué dans l’exemple suivant :


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**À propos des propriétés système du shell Windows**

Windows définit une liste complète des [Propriétés système](../properties/props.md) et le format de type valeur requis pour chaque propriété. La documentation de la propriété de l’interpréteur de commandes de la fenêtre [System. FileExtension](../properties/props-system-fileextension.md) , par exemple, spécifie que la valeur doit contenir le point de début (". docx" et non "docx").

**Valeurs Date et heure**

Le format de date et d’heure par défaut est ISO-8601, comme illustré dans l’exemple suivant :


```
2008-01-16T 19:20:30:.45+01:00
```



Les développeurs .NET doivent utiliser la classe DateTime avec `ToString("R") ` pour générer le format correct.

Pour plus d’informations sur le mappage de propriété, consultez « éléments étendus dans la recherche fédérée Windows » dans [création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Comprendre comment Windows mappe les éléments aux types de fichiers

La recherche dans l’interface utilisateur de l’Explorateur Windows permet aux utilisateurs de traiter les résultats comme des fichiers lorsqu’un élément RSS pointe vers un fichier stocké à distance. L’utilisateur peut glisser-déplacer des éléments sur le bureau, et l’interface utilisateur de l’Explorateur Windows affiche l’icône correcte et fournit le menu contextuel approprié. Si l’élément RSS ne pointe pas vers un fichier stocké à distance, le fichier est traité comme un lien et les utilisateurs peuvent effectuer des actions sur celui-ci, par exemple créer un raccourci ou l’ouvrir dans le navigateur.

L’organigramme suivant montre comment Windows détermine le type de fichier d’un élément.

![Organigramme présentant les chemins d’accès d’un élément aux décisions pour le traiter en tant qu’élément de type de lien Web ou en tant que type de fichier](images/determineanitemfiletype.png)

Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) effectue les étapes suivantes pour mapper un élément à un type de fichier :

-   Identifiez si l’élément doit être traité comme un fichier ou un lien Web.
-   Identifiez l’extension de nom de fichier correcte à utiliser.

Par exemple, si l’élément a une URL de lien qui utilise un chemin d’accès de système de fichiers (tel que `file:///\\server\share\etc\item.ext` ), le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) traite le lien comme un fichier et détermine le type en fonction de l’extension de nom de fichier utilisée dans le chemin d’accès (. ext dans cet exemple).

Si l’élément utilise le boîtier RSS standard ou **MediaRSS Media : content** , le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) suppose que l’élément est un fichier et identifie l’extension de nom de fichier comme suit :

-   Si la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) a été mappée pour l’élément, le fournisseur utilise cette extension de nom de fichier.
-   Si la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) n’a pas été mappée, le fournisseur utilise l’attribut **type** spécifié dans le boîtier ou l’élément de contenu. Cet élément doit contenir une `MIMEType` chaîne, telle que `"image/jpeg"` . Si le `MIMEType` est associé à une extension de nom de fichier inscrite sur l’ordinateur client, l’élément est considéré comme un fichier de ce type. Si le `MIMEType` n’est pas associé à une extension de nom de fichier inscrite sur l’ordinateur client, l’élément est traité comme un type de lien Web. Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) n’essaie pas d’analyser l’attribut **URL** pour localiser l’extension de nom de fichier.
-   Si le `MIMEType` est associé à une extension de nom de fichier inscrite sur l’ordinateur client, le fournisseur détermine si l’extension de nom de fichier est un type de fichier Web connu (. htm,. html,. asp,. aspx,. php,. swf,. stm). Dans ce cas, le type de fichier est considéré comme un type de lien Web ; dans le cas contraire, il est considéré comme un type de fichier. Par exemple, si le `MIMEType "text/html"` est associé à l’extension de nom de fichier. htm, cet élément est considéré comme un lien Web et non comme un type de fichier. htm.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Éviter les obstacles potentiels à l’activation d’un magasin de données

Certains magasins de données ne fournissent pas de service Web compatible [OpenSearch](https://github.com/dewitt/opensearch), mais ils peuvent toujours être connectés à Windows Federated Search. Ces magasins de données sont les suivants :

-   Les index distants avec des méthodes d’authentification qui ne sont pas prises en charge dans la recherche fédérée de Windows 7.

    Les exemples incluent l’authentification basée sur les formulaires et d’autres méthodes d’authentification personnalisées.

-   Si un magasin public de valeur élevée possède des API Web publiques, n’importe qui peut écrire un autre service Web compatible [OpenSearch](https://github.com/dewitt/opensearch)et appelle ces API en arrière-plan.

    Exemples : la bibliothèque de congrès et les bases de données de recherche médicale.

-   Les magasins de données d’entreprise propriétaires, les index et les magasins de gestion de contenu hérités, pour lesquels il peut être impossible d’implémenter un serveur frontal.

Toutefois, il existe des alternatives qui peuvent éviter les obstacles à l’activation d’un magasin de données. Voici quelques-unes de ces alternatives :

**Pour écrire un service Web intermédiaire lorsque vous ne pouvez pas modifier le service Web pour la source de données existante, ou si le service Web fournit une API personnalisée :**

1.  Écrire un service Web intermédiaire qui peut accepter une requête Windows 7.
2.  Connectez-vous à votre source de données et récupérez les résultats de la requête.
3.  Reformatez les résultats au format RSS ou Atom.
4.  Retournez les résultats au client Windows 7.
5.  Notez que pour les services de données d’entreprise et de nombreux services de données Internet, vous devrez peut-être transmettre les informations d’identification de l’utilisateur via pour le compte du service Web afin d’effectuer une suppression des résultats en fonction des autorisations de l’utilisateur.

**Pour utiliser un moteur de recherche existant lorsque vous ne pouvez pas activer un magasin de données public :**

1.  Utilisez un moteur de recherche public qui prend déjà en charge [OpenSearch](https://github.com/dewitt/opensearch) avec RSS. Pour ce faire, vous devez fournir à vos utilisateurs un fichier. fichier osdx avec un modèle d’URL qui limite les résultats à ceux de votre domaine spécifique.
2.  Consultez l’exemple suivant d’une description [OpenSearch](https://github.com/dewitt/opensearch) pour rechercher uniquement le contenu d’aide pour Windows à l’aide d’une requête sur Live.com.

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

    

**Pour utiliser un serveur d’indexation existant qui prend en charge OpenSearch quand vous ne pouvez pas activer des magasins de données d’entreprise propriétaires ou des index :**

1.  Sélectionnez un serveur d’indexation existant qui prend en charge [OpenSearch](https://github.com/dewitt/opensearch) pour indexer votre contenu, tel que le serveur de recherche SharePoint.
2.  Créez un fichier. fichier osdx qui limite les résultats de l’index SharePoint à ceux de votre serveur à l’aide de leur syntaxe de mot clé dans le modèle d’URL.

**Pour écrire une banque de données côté client si une solution côté serveur uniquement ne fonctionne pas :**

1.  Écrivez une source de données [OpenSearch](https://github.com/dewitt/opensearch) côté client qui se situe entre le fournisseur Windows [OpenSearch](https://github.com/dewitt/opensearch) et la source de données externe.
2.  Utilisez l’API de l' [interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) dans la SDK Windows pour créer un fichier. searchconnector-MS correctement configuré par le biais duquel l’Explorateur Windows peut appeler votre implémentation avec les paramètres de requête. Votre implémentation peut ensuite retourner des résultats au format RSS ou Atom. Cela permet à votre implémentation de fournir une interface utilisateur d’authentification personnalisée et de se connecter à la source de données à l’aide de son API propriétaire.

> [!Note]  
> L’ouverture d’un fichier. fichier osdx crée un fichier. searchconnector-ms (connecteur de recherche) dans le répertoire% USERPROFILE%/Searches et y place un lien dans le répertoire% USERPROFILE%/links.

 

## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Meilleures pratiques suivantes dans Windows Federated Search](-search-fedsearch-best.md)
</dt> <dt>

[Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
