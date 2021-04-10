---
description: 'Vous pouvez utiliser l’interface ISearchQueryHelper pour interroger l’index. Cette interface est implémentée en tant que classe d’assistance pour ISearchCatalogManager (et ISearchCatalogManager2), et est obtenue en appelant ISearchCatalogManager :: GetQueryHelper.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Interrogation de l’index avec ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201301"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Interrogation de l’index avec ISearchQueryHelper

Vous pouvez utiliser l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) pour interroger l’index. Cette interface est implémentée en tant que classe d’assistance pour [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (et [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), et est obtenue en appelant [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Cette interface vous permet d’effectuer les opérations suivantes :

-   Obtenez une chaîne de connexion OLE DB pour vous connecter à la base de données de recherche Windows.
-   Convertit les requêtes utilisateur de la syntaxe de requête avancée (AQS) en langage SQL de recherche Windows (SQL).
-   Spécifiez les restrictions de requête qui peuvent être exprimées en SQL, mais pas dans AQS.

Cette rubrique est organisée comme suit :

-   [Prise en main avec ISearchQueryHelper](#getting-started-with-isearchqueryhelper)
-   [Utilisation de la méthode GenerateSqlFromUserQuery](#using-the-generatesqlfromuserquery-method)
-   [Utilisation des identificateurs de paramètres régionaux](#working-with-locale-identifiers)
-   [Utilisation des propriétés et des colonnes](#working-with-properties-and-columns)
-   [Utilisation de l’expansion de terme de requête](#working-with-query-term-expansion)
-   [Utilisation d’autres méthodes ISearchQueryHelper](#working-with-other-isearchqueryhelper-methods)
-   [Rubriques connexes](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Prise en main avec ISearchQueryHelper

Il existe quelques méthodes et interfaces clés que vous devez connaître avant de commencer à interroger par programmation la recherche Windows à l’aide de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . À un niveau élevé, vous devez suivre les étapes suivantes :

1.  Instanciez une instance [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Obtenez une instance de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) à l’aide de [**ISearchManager :: getCatalog,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). Le nom du catalogue système pour la recherche Windows est `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Obtenez une instance de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) à l’aide de [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Une fois que vous disposez d’une instance de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), vous pouvez obtenir la chaîne de connexion utilisée pour se connecter à l’index de recherche Windows OLE DB connecteur.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Utilisation de la méthode GenerateSqlFromUserQuery

La méthode [**ISearchQueryHelper :: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforme l’entrée d’utilisateur en une chaîne de requête SQL, qui peut ensuite être envoyée au fournisseur OLE DB pour la recherche Windows. Cette méthode traduit la requête de [syntaxe de requête avancée](-search-3x-advancedquerysyntax.md) (AQS) ou la syntaxe de requête naturelle (NQS) entrée par l’utilisateur en SQL, et vous permet d’ajouter d’autres fragments SQL en fonction des besoins.

La chaîne de requête SQL est retournée sous la forme suivante :


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



Voici un exemple de la chaîne SQL retournée par l’appel `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> La méthode génère les prédicats FREETEXT et CONTAINs, car CONTAINs seul ne génère pas de classement significatif.

 

## <a name="working-with-locale-identifiers"></a>Utilisation des identificateurs de paramètres régionaux



| Méthode                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper :: obtient \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper ::p ut \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Obtient/place l’identificateur LCID (Language code identifier) de la requête. Cela permet d’obtenir le séparateur de mots et le biais corrects pour comparer les termes de requête à l’index catalogue/inversé. La valeur par défaut est le paramètre régional d’entrée actuel. |
| [**ISearchQueryHelper :: obtient \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper ::p ut \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Obtient/place le LCID de la langue à utiliser lors de l’analyse des mots clés de la syntaxe de requête avancée (AQS). La valeur par défaut est la valeur par défaut des paramètres régionaux utilisateur.                                                                              |



 

Les paramètres régionaux de **contenu** et les **Mots clés régionaux** sont des identificateurs de paramètres régionaux (LCID) qui aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des termes de la requête et la langue des mots clés AQS. Ce ne sont pas toujours les mêmes LCID, car Windows Search est proposé dans plusieurs versions internationales et comprend des packs MUI (Multilingual User Interface) pour d’autres langues. Les paramètres régionaux de contenu identifient le LCID pour les utilisateurs de langue qui saisissent leur requête de recherche dans, tandis que le mot clé local identifie le LCID utilisé par le moteur de recherche lors de l’analyse des mots clés de la syntaxe de requête avancée (AQS).

Par exemple, si vous disposez de la version anglaise (États-Unis) sans packs MUI, les paramètres régionaux de contenu et les paramètres régionaux de mot clé sont 1033. Si vous disposez de la version allemande sans packs MUI, les paramètres régionaux de contenu et les paramètres régionaux de mot-clé sont 1031 (GR-gr). Toutefois, si vous disposez de la version anglaise avec le Pack MUI roumain, les paramètres régionaux de contenu sont 2072 (RO) et les mots clés régionaux sont 1033 (en-US).

## <a name="working-with-properties-and-columns"></a>Utilisation des propriétés et des colonnes



| Méthodes                                                                                                                                                                                                                                                  | Description                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper :: obtient \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper ::p ut \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Obtient/définit les propriétés de contenu pour la recherche (colonne de propriété figurant dans les clauses CONTAINs ou FREETEXT).                                   |
| [**ISearchQueryHelper :: obtient \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper ::p ut \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Obtient/définit les colonnes (ou propriétés) demandées dans l’instruction SELECT. La valeur par défaut est System. ItemUrl et les propriétés utilisées dans la clause WHERE. |



 

Les éléments sont représentés dans le magasin de propriétés sous la forme d’une ligne. Chaque ligne contient plusieurs colonnes qui représentent les propriétés de cet élément. Tous les éléments n’ont pas de valeur pour une propriété donnée. Par exemple, un fichier audio ne contient généralement pas de valeur pour la propriété System. Property. FromName, mais il peut contenir des informations relatives à System. Music. Artist.

Avec ces méthodes, vous accédez ou modifiez la propriété avec une chaîne Unicode délimitée par des virgules, se terminant par un caractère null, qui spécifie un ou plusieurs noms de colonnes de la Banque de propriétés : «System.Document. Auteur, System.Document. Titre».

## <a name="working-with-query-term-expansion"></a>Utilisation de l’expansion de terme de requête



| Méthodes                                                                                                                                                                                                                                 | Description                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper :: obtient \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper ::p ut \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Obtient/définit l’indicateur de développement de terme de recherche. |



 

Cette méthode permet d’étendre certains termes de requête avec des caractères génériques, similaires à l’expansion d’expressions régulières. L’expansion de préfixe recherche des mots avec le même préfixe (fun/entonnoir). Si la valeur n’est pas définie, la valeur par défaut est le \_ préfixe de terme de recherche \_ \_ . Les valeurs prises en charge pour l’énumération de l' [**\_ \_ expansion des termes recherchés**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) sont les suivantes :

-   Rechercher \_ \_ le préfixe du terme \_ tous-tous les termes de recherche sont développés
-   \_Terme \_ de recherche sans \_ expansion-aucun terme de recherche n’est développé

## <a name="working-with-other-isearchqueryhelper-methods"></a>Utilisation d’autres méthodes ISearchQueryHelper

La plupart des méthodes de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) sont utilisées pour définir des arguments de requête ou définir les propriétés retournées.



| Méthodes                                                                                                                                                                                                                                                 | Description                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper :: obtient \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Retourne la chaîne de connexion OLE DB. Il s’agit de la méthode recommandée pour obtenir une chaîne de connexion correctement mise en forme et correcte.                                  |
| [**ISearchQueryHelper :: obtient \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper ::p ut \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Obtient/définit le nombre maximal de résultats qui doivent être retournés par une requête (autrement dit, sélectionnez TOP n). La valeur par défaut est-1, ce qui signifie qu’aucune clause de résultats maximale n’est générée. |
| [**ISearchQueryHelper :: obtient \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper ::p ut \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Obtient/définit l’ordre de tri du jeu de résultats de la requête (ORDER BY). S’il n’existe aucune clause ORDER BY, les résultats sont retournés dans un ordre non déterministe.                   |
| [**ISearchQueryHelper :: obtient \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper ::p ut \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Obtient/définit la syntaxe de la requête : la syntaxe de requête avancée ou la syntaxe de requête naturelle.                                                                                  |
| [**ISearchQueryHelper :: obtient \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper ::p ut \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Obtient/définit les restrictions ajoutées à l’aide des clauses WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Utilisation des approches SQL et AQS pour interroger l’index](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Utilisation de la syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




