---
description: présente le schéma de Description du connecteur de recherche utilisé par les bibliothèques Windows Explorer et les fournisseurs de recherche fédérés.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Schéma de la description du connecteur de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226380"
---
# <a name="search-connector-description-schema"></a>Schéma de la description du connecteur de recherche

présente le schéma de Description du connecteur de recherche utilisé par les bibliothèques Windows Explorer et les fournisseurs de recherche fédérés. Le schéma spécifie la structure et la configuration requise pour les fichiers de description du connecteur de recherche ( \* . searchConnector-ms) et pour les éléments **searchConnectorDescriptionType** des fichiers de description de la bibliothèque de l’interpréteur de commandes ( \* . Library-ms).

Cette rubrique décrit le schéma en ce qui concerne les connecteurs de recherche fédérés. Pour plus d’informations sur les bibliothèques et le schéma de description de la bibliothèque, consultez [schéma de description](../shell/library-schema-entry.md)de la bibliothèque.

Cette rubrique comporte les sections suivantes :

-   [Que sont les connecteurs de recherche ?](#what-are-search-connectors)
-   [Comment fonctionnent les fichiers de description du connecteur de recherche ?](#search-connector-description-schema)
-   [Qu’est-ce que le schéma de description du connecteur de recherche ?](#what-is-the-search-connector-description-schema)
-   [Quelles sont les principales parties du schéma ?](#what-are-the-major-parts-of-the-schema)
-   [Exemples de fichiers de description de connecteur de recherche](#examples-of-search-connector-description-files)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="what-are-search-connectors"></a>Que sont les connecteurs de recherche ?

Les connecteurs de recherche connectent les utilisateurs aux données stockées dans les services Web ou les emplacements de stockage distant. avec Windows 7, les utilisateurs peuvent installer des connecteurs de recherche pour des emplacements tels que des services web, afin qu’ils recherchent ces emplacements directement à partir de Windows Explorer. Les connecteurs de recherche sont des fichiers de description de connecteur de recherche ( \* . searchConnector-ms) qui spécifient comment se connecter à, envoyer des requêtes à et recevoir des résultats de l’emplacement.

En plus des services Web, les connecteurs de recherche peuvent être utilisés pour rechercher des étendues d’index locales créées par des gestionnaires de protocole. Par exemple, les utilisateurs peuvent rechercher des messages électroniques indexés localement avec le gestionnaire de protocole MAPI à l’aide d’un connecteur de recherche pour ce magasin de courrier électronique.

## <a name="how-do-search-connector-description-files-work"></a>Comment fonctionnent les fichiers de description du connecteur de recherche ?

lorsque la recherche de fichiers de Description de connecteur est installée sur les systèmes des utilisateurs, les utilisateurs peuvent ouvrir Windows Explorer, cliquer sur le connecteur de recherche dans le volet de navigation, puis entrer une requête de recherche. Windows L’Explorateur envoie la requête à l’aide des informations du fichier de description du connecteur de recherche, telles que le fournisseur à utiliser et l’étendue de la recherche. Les résultats sont retournés en tant qu’éléments de flux RSS ou Atom et affichés aux utilisateurs comme s’il s’agissait d’éléments de Shell normaux.

Le mode de déploiement du fichier de description du connecteur de recherche dépend du type d’emplacement pris en charge par le connecteur de recherche :

-   dans un fichier de configuration OpenSearch ( \* . fichier osdx) pour votre service web
-   Dans le cadre de l’installation du gestionnaire de protocole

Vous devez vous assurer que les événements suivants se produisent lorsqu’un utilisateur ouvre le fichier. fichier osdx ou installe le gestionnaire de protocole :

-   le fichier. searchconnector-ms est créé dans le dossier **recherches Windows** des utilisateurs (% userprofile%/Searches).
-   Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier **des liens des** utilisateurs (% UserProfile%/Links).

## <a name="what-is-the-search-connector-description-schema"></a>Qu’est-ce que le schéma de description du connecteur de recherche ?

Le schéma de la description du connecteur de recherche est un schéma XML qui définit la structure des fichiers de description du connecteur de recherche ( \* . searchConnector-ms). Chaque connecteur de recherche doit avoir un fichier de description de connecteur de recherche qui spécifie comment se connecter à, envoyer des requêtes à et recevoir des résultats de l’emplacement.

## <a name="what-are-the-major-parts-of-the-schema"></a>Quelles sont les principales parties du schéma ?

Le tableau suivant répertorie les principales parties du schéma.



| Éléments enfants                                                                         | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Indique si les emplacements pris en charge par le connecteur de recherche sont uniquement de recherche ou de recherche et de navigation.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Pour l’utilisation de la bibliothèque uniquement.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Pour l’utilisation de la bibliothèque uniquement.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Décrit le connecteur de recherche.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifie l’emplacement d’une icône personnalisée pour le connecteur de recherche.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifie l’emplacement d’une miniature personnalisée pour le connecteur de recherche.                                                                                                                 |
| [auteur](search-schema-sconn-author.md)                                               | Identifie l’auteur du connecteur de recherche.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Identifie la date à laquelle le connecteur de recherche a été créé.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Spécifie un type de dossier pour le connecteur de recherche.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Spécifie le moteur de recherche à utiliser par ce connecteur de recherche.                                                                                                                      |
| [scope](search-schema-sconn-scope.md)                                                 | Spécifie les emplacements à inclure dans l’étendue de recherche et à exclure de celle-ci.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Spécifie l’emplacement d’un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basé sur XML pour ce connecteur de recherche. **IPropertyStore** prend en charge les métadonnées ouvertes du connecteur de recherche. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | spécifie si l’emplacement représenté par le connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer.                                                                 |
| [Domain](search-schema-sconn-domain.md)                                               | Identifie le domaine de premier niveau du connecteur de recherche.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Spécifie si le connecteur de recherche prend en charge la syntaxe de requête avancée (AQS).                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | Spécifie si l’emplacement représenté par le connecteur de recherche est indexé.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Exemples de fichiers de description de connecteur de recherche

Voici un exemple de fichier de description de connecteur de recherche pour un service Web de recherche fédérée.


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



Voici un exemple de fichier de description de connecteur de recherche pour un gestionnaire de protocole MAPI.


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



## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur le schéma de description de la bibliothèque, consultez [schéma de description](../shell/library-schema-entry.md)de la bibliothèque.
-   Pour plus d’informations sur l’installation d’un connecteur de recherche, consultez [recherche fédérée dans Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
