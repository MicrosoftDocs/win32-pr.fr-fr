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
# <a name="getting-started-with-federated-search-in-windows"></a>Prise en main avec la recherche fédérée dans Windows

La prise en charge de Windows 7 pour la Fédération des recherches dans des magasins de données distants à l’aide des technologies OpenSearch permet aux utilisateurs d’accéder à leurs données distantes à partir de l’Explorateur Windows. Vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et permettre une intégration enrichie de vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou déployer de code côté client Windows.

Cette rubrique est organisée comme suit :

-   [Qu’est-ce que la recherche fédérée ?](#what-is-federated-search)
-   [Étapes de création d’une recherche fédérée](#steps-for-building-federated-search)
-   [Fonctionnement de la recherche fédérée](#how-federated-search-works)
-   [Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Exemples de recherche fédérée](#federated-search-examples)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-federated-search"></a>Qu’est-ce que la recherche fédérée ?

Windows 7 prend en charge la connexion de sources externes au client Windows via le protocole [OpenSearch](https://github.com/dewitt/opensearch) . Cela permet aux utilisateurs de rechercher dans un magasin de données distant et d’afficher les résultats à partir de l’Explorateur Windows. Le standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 définit des formats de fichiers simples qui peuvent être utilisés pour décrire comment un client doit interroger le service Web pour le magasin de données et comment le service doit retourner les résultats à afficher par le client. La recherche fédérée Windows se connecte aux services Web qui reçoivent des requêtes [OpenSearch](https://github.com/dewitt/opensearch) et retourne les résultats au format RSS ou Atom XML.

La capture d’écran suivante illustre les résultats de recherche obtenus après la recherche à distance sur un site SharePoint.

![capture d’écran qui affiche les résultats de la recherche à partir d’un site SharePoint tel qu’il apparaît dans l’Explorateur Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Étapes de création d’une recherche fédérée

Pour créer une recherche fédérée, procédez comme suit :

1.  Autorisez la recherche dans votre banque de données à partir de l’Explorateur Windows en fournissant un service Web compatible [OpenSearch](https://github.com/dewitt/opensearch)qui peut retourner des résultats au format RSS ou Atom.
2.  Créez un fichier de description OpenSearch (. fichier osdx) qui décrit comment se connecter au service Web et comment mapper des éléments personnalisés dans votre fichier XML RSS ou Atom.
3.  Déployez les connecteurs de recherche sur les ordinateurs clients Windows avec un fichier. fichier osdx.

Le diagramme suivant illustre les étapes de création d’une recherche fédérée.

![diagramme du processus de création d’une recherche fédérée](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Fonctionnement de la recherche fédérée

La communication entre l’Explorateur Windows et votre service Web [OpenSearch](https://github.com/dewitt/opensearch) s’effectue via la couche de données Windows. La couche de données Windows peut communiquer avec différents types de magasins de données via des fournisseurs Windows Store. Chaque fournisseur est spécialisé dans la communication avec les magasins de données qui prennent en charge un protocole particulier et qui possèdent des fonctionnalités spécifiques. Par exemple, l’illustration suivante explique comment le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) communique avec les magasins de données qui fournissent un service Web qui prend en charge la norme [OpenSearch](https://github.com/dewitt/opensearch) .

![Diagramme montrant la communication à partir de l’Explorateur Windows sur le client via le magasin de données OpenSearch sur le serveur distant](images/windowssearchfederationfunctionality.png)

Pour permettre à votre magasin de données de prendre en charge la recherche fédérée dans Windows 7, vous devez effectuer un certain nombre de tâches. Le tableau suivant répertorie les tâches d’activation de votre magasin de données, ce qui est nécessaire pour accomplir chaque tâche et où trouver de la documentation.



| Tâche                                                                                                     | Condition requise                                                                                                                                                                                            | Documentation                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Activez la recherche de votre banque de données par l’Explorateur Windows.<br/>                                    | Créez un service Web compatible OpenSearch.<br/> Créez un fichier de description OpenSearch (. fichier osdx).<br/>                                                                                       | [Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)<br/> [Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)<br/> |
| Déployez activement votre service Web pour les utilisateurs au sein d’une entreprise.<br/>                               | Fournissez un fichier. fichier osdx à vos utilisateurs, copiez-le localement et rendez-le accessible à l’utilisateur via un raccourci.<br/>                                                                                     | [Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Énumérer les résultats de la recherche dans l’Explorateur Windows en réponse à une requête.<br/>                          | Implémentez un service Web qui accepte une chaîne de requête et retourne les résultats au format RSS ou Atom.<br/>                                                                                              | [Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Permettre aux utilisateurs d’ajouter votre magasin de données à leur Explorateur Windows.<br/>                                | Créez un fichier. fichier osdx et fournissez-le à vos utilisateurs.<br/>                                                                                                                                           | [Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Affichez vos éléments en tant qu’éléments de type fichier dans l’Explorateur Windows.<br/>                                    | Retourner une URL vers le fichier ou le flux de contenu à l’aide d’un **boîtier** ou d’un **média :** éléments de contenu<br/> Fournissez une extension de nom de fichier ou un type MIME que l’ordinateur client reconnaît.<br/> | [Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Affichez les propriétés personnalisées dans l’Explorateur Windows, au-delà de celles définies dans les normes RSS ou Atom.<br/> | Fournir des métadonnées supplémentaires à l’aide d’un autre espace de noms XML dans votre sortie RSS/Atom.<br/> Ajoutez un mappage des propriétés à votre fichier. fichier osdx.<br/>                                                       | [Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personnaliser les propriétés affichées pour vos éléments dans l’Explorateur Windows.<br/>               | Ajoutez des mappages PropList à votre fichier. fichier osdx.<br/>                                                                                                                                                   | [Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Affichez une vue de page Web personnalisée de vos éléments dans le volet de visualisation.<br/>                              | Retourne des valeurs de lien et de boîtier distinctes.<br/> Mappez une valeur d’URL à la propriété de l’interpréteur de commandes Windows **System. WebPreviewUrl** .<br/>                                                               | [Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Affichez un bouton de barre de commandes dans l’Explorateur Windows qui restaure la requête sur votre site Web.<br/>   | Fournissez un `Url format="text/html"` modèle dans le fichier. fichier osdx.<br/>                                                                                                                              | [Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Envoi de requêtes et retour des résultats de recherche dans RSS ou Atom

Lorsque l’utilisateur tape un terme dans la zone de recherche dans l’angle supérieur droit de l’Explorateur Windows, la requête est envoyée au fournisseur [OpenSearch](https://github.com/dewitt/opensearch) , qui envoie ensuite la requête au magasin de données distant. Le service Web distant répond à la requête en fournissant des résultats dans un document XML, généralement appelé flux, dans l’un des deux formats pris en charge (RSS ou Atom). Chaque élément de résultat dans le flux contient des éléments enfants XML pour représenter ou décrire des métadonnées d’élément, telles que le titre, l’URL, la description, l’image miniature, etc. Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) est chargé de mapper les valeurs des éléments XML aux propriétés système du shell Windows qui peuvent être utilisées par les applications Windows.

## <a name="federated-search-examples"></a>Exemples de recherche fédérée

L’exemple suivant de fichier de description OpenSearch (. fichier osdx) se compose des `ShortName` `Url` éléments et, qui sont les éléments enfants requis minimum pour connecter un magasin de données externe au client Windows via le protocole OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



L’exemple suivant montre comment effectuer une recherche dans un magasin de données compatible avec le Web au format RSS et comment spécifier qu’un élément de recherche doit être retourné :


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



L’exemple suivant montre comment mapper des propriétés à des propriétés système par défaut afin que les éléments affichés soient triés et regroupés :


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



L’exemple suivant montre comment ajouter un affichage d’image miniature à chaque élément dans l’Explorateur Windows :


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Meilleures pratiques suivantes dans Windows Federated Search](-search-fedsearch-best.md)
</dt> <dt>

[Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 




