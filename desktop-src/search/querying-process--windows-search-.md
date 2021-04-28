---
description: Interrogation du processus dans la recherche Windows
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Interrogation du processus dans la recherche Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3585f2cca2a6d5d8548a85ae8fac759ec94b4fa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117327"
---
# <a name="querying-process-in-windows-search"></a>Interrogation du processus dans la recherche Windows

Cette rubrique est organisée comme suit :

-   [À propos de l’interrogation dans Windows Search](#about-querying-in-windows-search)
    -   [Requêtes locales et distantes](#local-and-remote-queries)
    -   [Vue d’ensemble de l’API de requête structurée](#structured-query-api-overview)
-   [Interrogation des scénarios](#querying-scenarios)
    -   [Extraction de condition et analyse de requête](#condition-extraction-and-query-parsing)
    -   [Interrogation de l’index](#querying-the-index)
-   [Rubriques connexes](#related-topics)

## <a name="about-querying-in-windows-search"></a>À propos de l’interrogation dans Windows Search

L’interrogation dans la recherche Windows est basée sur les quatre approches suivantes :

-   [Syntaxe de requête avancée](-search-3x-advancedquerysyntax.md) (AQS)
-   Syntaxe de requête naturelle (NQS)
-   SQL (Structured Query Language)
-   Interfaces de requête structurée

AQS est la syntaxe de requête par défaut utilisée par Windows Search pour interroger l’index et affiner et limiter les paramètres de recherche. AQS est principalement utilisé par l’utilisateur et peut être utilisé par les utilisateurs pour créer des requêtes AQS, mais il peut également être utilisé par les développeurs pour créer des requêtes par programmation. Dans Windows 7, le AQS canonique a été introduit et doit être utilisé pour générer des requêtes AQS par programmation. Dans Windows 7 et versions ultérieures, une option de menu contextuel peut être disponible selon qu’une condition AQS est remplie ou non. Pour plus d’informations, consultez « obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée » dans [création de gestionnaires de menus contextuels](../shell/context-menu-handlers.md). Les requêtes AQS peuvent être limitées à des types de fichiers spécifiques, connus sous le nom de types de fichiers. Pour plus d’informations, consultez [types de fichiers et associations](../shell/fa-intro.md). Pour obtenir une documentation de référence sur les propriétés appropriées, consultez [System. Kind](../properties/props-system-kind.md)et [System. KindText](../properties/props-system-kindtext.md).

NQS est une syntaxe de requête qui est plus stricte que AQS, et est semblable à la langue humaine. NQS peut être utilisé par Windows Search pour interroger l’index si NQS est sélectionné à la place de la valeur par défaut, AQS.

SQL est un langage de texte qui définit des requêtes. SQL est commun entre de nombreuses technologies de base de données. Windows Search utilise SQL, en implémente un sous-ensemble et l’étend en ajoutant des éléments au langage. Windows Search SQL étend la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles. Toutes les fonctionnalités de Windows Search SQL sont compatibles avec Windows Search sur Windows XP et Windows Server 2003, et versions ultérieures. Pour plus d’informations sur Windows Search SQL, consultez [interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md)et [vue d’ensemble de la syntaxe SQL de Windows Search](-search-sql-ovwofsearchquery.md).

Les API de requête structurée sont décrites plus loin dans cette rubrique. Pour obtenir une documentation de référence sur les API de requête structurées, consultez [interrogation d’interfaces](-search-querying-interfaces-entry-page.md). Les interfaces telles que [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) permettent de construire des chaînes SQL à partir d’un ensemble de valeurs d’entrée. Cette interface convertit les requêtes utilisateur AQS en SQL de recherche Windows et spécifie les restrictions de requête qui peuvent être exprimées dans SQL, mais pas dans AQS. [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) obtient également une chaîne de connexion OLE DB pour se connecter à la base de données de recherche Windows.

### <a name="local-and-remote-queries"></a>Requêtes locales et distantes

Vous pouvez exécuter vos requêtes localement ou à distance. Une requête locale utilisant la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant. Une requête locale interroge le catalogue SystemIndex local uniquement.


```
FROM SystemIndex
```



Une requête distante à l’aide de la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant. L’ajout de NomOrdinateur transforme l’exemple précédent en une requête distante.


```
FROM [<ComputerName>.]SystemIndex
```



Par défaut, Windows XP et Windows Server 2003 n’ont pas installé Windows Search. Seul Windows Search 4 (WS4) fournit une prise en charge des requêtes distantes. Les versions précédentes de Windows Desktop Search (WDS), telles que 3,01 et antérieures, ne prennent pas en charge l’interrogation à distance. Avec l’Explorateur Windows, vous pouvez interroger l’index local d’un ordinateur distant pour les éléments du système de fichiers (éléments gérés par le protocole « fichier : »).

Pour récupérer un élément à l’aide d’une requête distante, l’élément doit remplir les conditions suivantes :

-   Être accessible via le chemin d’accès UNC (Universal Naming Convention).
-   Existent sur l’ordinateur distant auquel le client a accès.
-   A sa sécurité définie pour autoriser le client à avoir un accès en lecture.

L’Explorateur Windows possède des fonctionnalités de partage d’éléments, y compris un partage « public » ( \\ \\ ordinateur \\ public \\ ...) dans le **Centre réseau et partage**, et un partage « utilisateurs » ( \\ \\ \\ utilisateurs \\ de l’ordinateur...) pour les éléments partagés via l’Assistant partage. Une fois que vous avez partagé le ou les dossiers, vous pouvez interroger l’index local en spécifiant le nom d’ordinateur de l’ordinateur distant dans la clause FROM et un chemin d’accès UNC sur l’ordinateur distant dans la clause SCOPE. Une requête distante utilisant les clauses FROM et SCOPE est présentée dans l’exemple suivant.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Les exemples fournis ici utilisent SQL.

### <a name="structured-query-api-overview"></a>Vue d’ensemble de l’API de requête structurée

Une requête structurée offre la possibilité de rechercher des informations par combinaisons booléennes de requêtes sur des propriétés individuelles. Dans cette rubrique, nous décrivons les fonctionnalités des API et des méthodes de requête structurées les plus importantes. Pour obtenir une documentation de référence sur les API de requête structurées, consultez [interrogation d’interfaces](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

La méthode [**IQueryParser ::P**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) faible analyse une chaîne d’entrée utilisateur et produit une interprétation sous la forme d’un [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Si le paramètre *pCustomProperties* de cette méthode n’a pas la valeur null, il s’agit d’une énumération d’objets [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (un pour chaque propriété personnalisée reconnue). Les autres méthodes [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) permettent à l’application de définir plusieurs options, telles que les paramètres régionaux, un schéma, un analyseur lexical et des gestionnaires pour différents types d’entités nommées. [**IQueryParser :: GetSchemaProvider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) retourne une interface [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) pour parcourir le schéma chargé.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution : IConditionFactory

L’interface [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) fournit toutes les informations sur le résultat de l’analyse d’une chaîne d’entrée. Étant donné que **IQuerySolution** est également une interface [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) , d’autres nœuds de l’arborescence des conditions peuvent être créés. La méthode [**IQuerySolution :: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) produit une arborescence de conditions pour l’interprétation. **IQuerySolution :: GetQuery** retourne également le type sémantique.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) crée des nœuds d’arborescence de conditions. Si le paramètre *simplifier* de [**IConditionFactory :: MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) a **la \_ valeur true**, alors le [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) résultant est simplifié et n’a pas besoin d’être un nœud de négation. Si le paramètre *pSubConditions* de [**IConditionFactory :: MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) n’a pas la valeur null, ce paramètre doit être une énumération d’objets [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) et devenir des sous-arbres. [**IConditionFactory :: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) construit un nœud terminal avec un nom de propriété, une opération et une valeur spécifiés. La chaîne dans le paramètre *pValueType* doit être le nom d’un type sémantique du schéma. Si le paramètre *expand* a **la \_ valeur true** et que la propriété est virtuelle, l’arborescence de condition résultante est généralement une disjonction résultant de l’extension de la propriété à ses composants définis. Si la valeur n’est pas null, les paramètres *pPropertyNameTerm*, *pOperatorTerm* et *pValueTerm* doivent identifier les termes indiquant la propriété, l’opération et la valeur.

### <a name="icondition--ipersiststream"></a>ICondition : IPersistStream

L’interface [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) est un nœud unique dans une arborescence de conditions. Le nœud peut être un nœud de négation, un nœud, un nœud ou un nœud terminal. Pour un nœud non-terminal, [**ICondition :: GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) retourne une énumération des sous-arborescences. Pour un nœud terminal, les méthodes suivantes de [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) retournent les valeurs suivantes :

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) retourne le nom, l’opération et la valeur de la propriété.
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) retourne le type de sémantique de la valeur, qui a été specificied dans le paramètre *pszValueType* de [**IConditionFactory :: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) retourne un format de chaîne de la valeur. (Si la valeur était déjà une chaîne, cette forme sera normalisée par rapport à la casse, les accents, etc.)
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) retourne des informations sur les parties de la phrase d’entrée qui ont généré le nom de la propriété, l’opération et la valeur.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) retourne une copie complète d’une arborescence de conditions.

### <a name="irichchunk"></a>IRichChunk

Chaque objet [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifie une étendue de jeton et une chaîne. **IRichChunk** est une interface utilitaire qui représente des informations sur une étendue (généralement une étendue de jetons) identifiée par une position de départ et une longueur. Ces informations d’étendue incluent une chaîne et/ou une **variante**.

### <a name="iconditiongenerator"></a>IConditionGenerator

L’interface [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) est fournie par l’application pour gérer la génération de l’arborescence de la reconnaissance et des conditions pour un type d’entité nommé. Un générateur de condition est donné à un [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) via [**IQueryParser :: SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) appelle [**IConditionGenerator :: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) avec un [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) pour le schéma actuellement chargé. Cela permet à [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) d’obtenir les informations de schéma requises. Lors de l’analyse d’une chaîne d’entrée, **IQueryParser** appelle la méthode [**IConditionGenerator :: RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) de chaque [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), de sorte que l’occurrence des entités nommées qu’il reconnaît dans la chaîne d’entrée peut être signalée. **IQueryParser** peut utiliser les paramètres régionaux actuels et utiliser la création de jetons de l’entrée telle qu’elle doit signaler les étendues de jeton des entités nommées.

Quand [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) est sur le paragraphe d’émettre un nœud terminal et que le type sémantique de la valeur correspond au type d’entité nommé pour un [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), **IQueryParser** appelle [**IConditionGenerator :: GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) avec les informations du nœud à générer. Si la [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) retourne la valeur \_ OK, elle doit retourner une arborescence de condition (qui ne doit pas nécessairement être un nœud terminal) et informer **IQueryParser** s’il faut supprimer l’interprétation de chaîne alternative qu’elle générerait normalement comme précaution.

### <a name="itokencollection"></a>ITokenCollection

La méthode [**ITokenCollection :: NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) retourne le nombre de jetons. [**ITokenCollection :: GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) retourne des informations sur le jeton *i* th. Le début et la longueur sont des positions de caractères dans la chaîne d’entrée. Le texte retourné ne sera pas NULL uniquement s’il existe un texte substituant les caractères de la chaîne d’entrée. Cela est utilisé, par exemple, pour remplacer un tiret dans la chaîne d’entrée par NOT quand ce tiret est dans un contexte où il doit être interprété comme une négation.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) appelle [**INamedEntityCollector :: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) pour chaque entité nommée reconnue. Les étendues sont des étendues de jeton. Cela doit toujours être le cas de *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* et *endSpan* peuvent différer de *beginActual* et *endActual* si l’entité nommée commence et/ou se termine par des jetons sémantiquement non significatifs, tels que des guillemets (qui sont néanmoins couverts par l’entité nommée). La valeur doit être exprimée sous la forme d’une chaîne et apparaîtra par la suite dans un appel à [**IConditionGenerator :: GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>ISchemaProvider

L’interface [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) peut être utilisée pour parcourir un schéma chargé pour les entités (types) et les relations (propriétés). Voici ce que font les méthodes individuelles :

-   Les [**entités**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) retournent une énumération de chaque entité ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) dans le schéma.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) retourne l’entité racine du schéma. Pour un schéma plat, le type principal de chaque [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) est retourné.
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) recherche une entité par nom et retourne S \_ false s’il n’existe aucune entité de ce type dans le schéma.
-   Les [**métadonnées**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) retournent une énumération des interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) .

### <a name="ientity"></a>IEntity

L’interface [**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) est une entité de schéma qui représente un type ayant un nom, qui a un certain nombre de relations nommées avec d’autres types (propriétés) et qui dérive d’une entité de base. Voici les différentes méthodes :

-   [**IEntity :: Relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) retourne une énumération d’objets [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) , un pour chaque relation sortante de ce type. Chaque relation sortante d’une entité a un nom.
-   [**IEntity :: GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) recherche une relation par nom et retourne S \_ false s’il n’existe aucune relation de ce type pour cette entité.
-   [**IEntity :: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) retourne une énumération d’interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , une pour chaque paire de métadonnées de cette entité.
-   [**IEntity ::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) retourne une phrase par défaut pour faciliter la génération d’un AQS ou d’un reconditionnement NQS d’une arborescence de conditions.

### <a name="irelationship"></a>IRelationship

L’interface [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) représente une relation entre deux entités : une source et une destination. Voici ce que font les méthodes individuelles :

-   [**IRelationship :: IsReal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) indique si une relation est réelle. Par exemple, si l’entité A dérive de l’entité B et qu’elle hérite d’une relation nommée R de celle-ci, un peut encore avoir sa propre relation nommée R. Toutefois, la relation beween A et R doit avoir le même type de destination que celui de B, et la seule raison pour l’existence est de stocker les métadonnées spécifiques à B. Une telle relation de B est dite non réelle.
-   [**IRelationship :: métadonnée**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) retourne une énumération d’interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , une pour chaque paire de métadonnées de cette entité.
-   [**IRelationship ::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) retourne l’expression par défaut à utiliser pour cette relation dans les restatements. Chaque relation a une phrase par défaut qui la désigne pour faciliter la génération d’un AQS ou d’un NQS Restatement d’une arborescence de conditions.

### <a name="imetadata"></a>IMetaData

Les métadonnées sont des paires clé-valeur qui sont associées à une entité, à une relation ou à l’ensemble du schéma. Étant donné que les clés ne sont pas nécessairement uniques, une collection de métadonnées peut être considérée comme un mappage multiple. [**IMetaData :: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) est appelé pour récupérer la clé et la valeur d’une paire refléter.

## <a name="querying-scenarios"></a>Interrogation des scénarios

Les scénarios suivants décrivent l’utilisation des API de requête structurée dans Windows Search dans des scénarios d’interrogation courants, tels que la création d’une arborescence de conditions et l’interrogation de l’index.

### <a name="condition-extraction-and-query-parsing"></a>Extraction de condition et analyse de requête

Lorsqu’une requête est créée, son étendue est définie en indiquant au système où la recherche doit être apportée. Cela limite les résultats de la recherche. Une fois l’étendue définie, un filtre est appliqué et un ensemble de filtres est retourné. Les résultats de la recherche sont limités par la création d’une arborescence de conditions avec des nœuds terminaux, similaire à un graphique. Ces conditions sont ensuite extraites. Une arborescence de condition est une combinaison booléenne (AND, OR, NOT) des conditions feuilles, qui associent chacune une propriété, par le biais d’une opération, à une valeur. Un nœud terminal représente une restriction sur une propriété unique à une valeur par le biais de certaines opérations.

Une restriction de filtre requiert une expression logique qui décrit la restriction. La définition de cette expression commence par l’interface [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) , qui est utilisée pour créer un nœud unique dans une arborescence de conditions. Étant donné qu’il n’existe qu’une seule condition dans l’exemple suivant, l’arborescence ne change pas.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



S’il existe plusieurs conditions de filtre, et et d’autres opérateurs booléens sont utilisés pour obtenir une arborescence unique. Les arborescences et ou-arbres représentent les conjonctions et les disjonctions de leurs sous-arborescences. Un non-arbre représente la négation de sa sous-arborescence unique. AQS fournit une approche textuelle pour obtenir des expressions logiques avec des opérateurs booléens, et est souvent plus simple.

Dans l’exemple suivant, nous allons convertir l’arborescence de condition ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) en forme visuelle. L’analyseur de requête, à l’aide de l’interface [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) , convertit le [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) en chaîne de requête au format RTF (Rich Text formatted). La méthode [**IQueryParser :: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) retourne le texte de la requête, tandis que la méthode [**IQueryParser ::P**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) faible produit une interface [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) . L’exemple suivant montre comment procéder.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



La principale entrée de [**IQueryParser ::P**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) faible est une chaîne d’entrée utilisateur à analyser, mais l’application peut également informer l’analyseur de requête de toutes les propriétés qu’il a identifiées dans l’entrée (à partir de la syntaxe spécifique à l’application). La sortie de **IQueryParser ::P** faible est un [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), qui fournit toutes les informations relatives à cet appel d’analyse. Il existe des méthodes pour obtenir la chaîne d’entrée, la manière dont la chaîne d’entrée a été signalée, toutes les erreurs d’analyse et la requête analysée comme arborescence de conditions, représentée par un [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). L’exemple suivant montre...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



Dans l’exemple précédent, [**IQuerySolution :: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) peut obtenir des informations sur la requête, notamment le texte d’origine, les jetons qui composent le texte ou l’arborescence de condition. Le tableau suivant répertorie des exemples de valeurs de requête retournées possibles.



| Exemples de valeurs de requête retournées                        | Description                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Le texte de la requête renvoyé par [**IQueryParser :: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | La répartition des jetons                                                                                  |
| ![arborescence de condition non résolue](images/queryvalues1.png) | Arborescence de condition non résolue                                                                              |



 

L’arborescence de condition initiale qui est retournée n’est pas résolue. Dans une arborescence de condition non résolue, les références de date et d’heure, telles que `date:yesterday` , ne sont pas converties en heure absolue. En outre, les propriétés virtuelles ne sont pas développées. Les propriétés virtuelles sont des propriétés qui jouent le rôle d’agrégats de plusieurs propriétés.

Par exemple, la requête `kind:email from:reljai` produit les arborescences de condition non résolues et résolues suivantes. L’arborescence de condition non résolue est à gauche et l’arborescence de condition résolue est à droite.

![arborescences de condition non résolues et résolues](images/conditiontree.png)

L’arborescence résolue peut être obtenue en appelant [**IConditionFactory :: Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Toutefois, le passage de SQRO ne pas [**\_ \_ résoudre \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) conserve la date et l’heure non résolues. Une arborescence de condition non résolue présente des avantages, car une arborescence de condition non résolue contient des informations sur la requête. Chaque nœud terminal pointe vers les jetons retournés par [**IQuerySolution :: GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), qui correspondent à la propriété, à l’opérateur et à la valeur lors de l’utilisation de l’interface [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) . L’exemple suivant montre...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Interrogation de l’index

Il existe plusieurs approches pour interroger l’index. Certains sont basés sur le SQL et d’autres sont basés sur AQS. Vous pouvez également interroger l’index de recherche Windows par programme à l’aide d' [interfaces d’interrogation](./-search-querying-interfaces-entry-page.md). Trois interfaces sont spécifiques à l’interrogation de l’index : [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)et [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Pour obtenir des informations conceptuelles, consultez [interrogation de l’index par programmation](-search-3x-wds-qryidx-overview.md).

Vous pouvez développer une classe de composant ou d’assistance pour interroger l’index à l’aide de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Cette interface est implémentée en tant que classe d’assistance pour [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (et [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), et est obtenue en appelant [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Pour obtenir des informations conceptuelles, consultez [interrogation de l’index à l’aide de ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md).

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) vous permet d’effectuer les opérations suivantes :

-   Obtenez une chaîne de connexion OLE DB pour vous connecter à la base de données de recherche Windows.
-   Convertissez les requêtes de l’utilisateur AQS en SQL de Windows Search.
-   Spécifiez les restrictions de requête qui peuvent être exprimées dans SQL, mais pas dans AQS.

La hiérarchisation des index et les événements d’ensemble de lignes sont pris en charge dans Windows 7 et versions ultérieures. Avec [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) , il existe une pile de priorité qui permet au client de demander que les étendues utilisées dans une requête particulière reçoivent une priorité plus élevée que la normale. [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) fournit une notification des modifications apportées aux éléments dans les ensembles de lignes, y compris l’ajout de nouveaux éléments, la suppression des éléments et la modification des données de l’élément. L’utilisation de notifications d’événements d’ensemble de lignes garantit que les résultats des requêtes existantes sont aussi à jour que possible. Pour obtenir des informations conceptuelles, consultez [indexation des priorités et des événements d’ensemble de lignes dans Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexation, interrogation et notifications dans Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Ce qui est inclus dans l’index](-search-indexing-process-overview.md)
</dt> <dt>

[Processus d’indexation dans la recherche Windows](-search-indexing-process-overview.md)
</dt> <dt>

[Processus de notification dans Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Configuration requise pour la mise en forme des URL](url-formatting-requirements.md)
</dt> </dl>

 

 
