---
description: Windows utilisateurs peuvent enregistrer des recherches dans un dossier de recherche généré par un fichier XML qui stocke la requête dans un formulaire qui peut être utilisé par le sous-système de recherche Windows.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Format de fichier de recherche enregistré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863722"
---
# <a name="saved-search-file-format"></a>Format de fichier de recherche enregistré

dans Windows Vista et versions ultérieures, les utilisateurs peuvent enregistrer des recherches dans un dossier de recherche généré par un fichier XML qui stocke la requête dans un formulaire qui peut être utilisé par le sous-système de recherche Windows. Cette rubrique décrit le format de fichier ( \* . search-ms) et comprend les sections suivantes :

- [Vue d’ensemble des recherches enregistrées](#overview-of-saved-searches)
- [\<viewInfo> Appartient](/windows)
  - [\<viewInfo> Attributs](/windows)
  - [\<viewInfo> Éléments enfants](/windows)
- [\<query> Appartient](/windows)
  - [\<query> Éléments enfants](/windows)
- [\<properties> Appartient](/windows)
- [Spécification complète de la recherche-format de fichier MS](#full-specification-of-the-search-ms-file-format)
- [Exemples de recherches enregistrées](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Vue d’ensemble des recherches enregistrées

les utilisateurs peuvent enregistrer une requête de recherche en tant que dossier de recherche, un dossier virtuel affiché dans Windows Explorer sous le dossier recherches. L’ouverture d’un dossier de recherche exécute la recherche enregistrée et affiche les résultats mis à jour. le fichier de recherche enregistré stocke la requête dans un format Windows la recherche peut agir, en spécifiant les éléments à rechercher, l’emplacement de la recherche et la manière de présenter les résultats.

La recherche enregistrée est générée à partir d’un fichier XML ( \* . search-ms) dans le dossier% UserProfile% \\ Searches. Les données sont divisées en trois éléments principaux dans le fichier XML :

- \<viewInfo> spécifie les informations de présentation
- \<query> spécifie (Rechercher les informations de requête
- \<properties> spécifie les propriétés du \* fichier. search-ms lui-même

L’exemple suivant illustre la structure de haut niveau d’un fichier de recherche enregistré.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>Élément \<viewInfo>

L' \<viewInfo> élément spécifie la façon dont les résultats sont présentés à l’utilisateur final. L’exemple suivant illustre la structure de l’élément.

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Attributs

Le tableau suivant décrit les attributs d’un de l’élément \<viewInfo>.

| Attribut     | Description                                                                     | Valeurs                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| viewMode      | Spécifie l’affichage des dossiers.                                                      | \|Vignettes des icônes de détails \|  |
| iconSize      | Contrôle la taille par défaut des icônes et des miniatures des éléments en l’absence de pile. | Entier compris entre 16 et 256 |
| stackIconSize | À usage interne uniquement. Ne pas utiliser.                                              | n/a                        |
| displayName   | À usage interne uniquement. Ne pas utiliser.                                              | n/a                        |
| autoListFlags | À usage interne uniquement. Ne pas utiliser.                                              | n/a                        |
| folderFlags   | À usage interne uniquement. Ne pas utiliser.                                              | n/a                        |
| taskFlags     | À usage interne uniquement. Ne pas utiliser.                                              | n/a                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Éléments enfants

les éléments enfants de l' \<viewInfo> élément spécifient les colonnes qui s’affichent dans les résultats de recherche de l’explorateur de Windows et la manière dont les résultats sont regroupés et triés. Chaque élément enfant contient un ensemble ordonné de colonnes, identifiées par des noms canoniques de propriétés système (par exemple, System. DisplayName). S’ils ne sont pas définis dans le fichier de recherche enregistré, les résultats de la recherche sont présentés avec un ensemble de colonnes par défaut approprié pour les types de fichiers affichés.

| Élément               | Description                                                                                        | Valeurs                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | Spécifie une liste triée de colonnes à afficher dans la vue résultats. L’utilisateur peut modifier cette liste. | Toute propriété système.                                         |
| frequentlyUsedColumns | À usage interne uniquement. Ne pas utiliser.                                                                 | n/a                                                          |
| columnChooserColumns  | À usage interne uniquement. Ne pas utiliser.                                                                 | n/a                                                          |
| Comportant               | Spécifie une propriété système unique par laquelle grouper les résultats. L’utilisateur peut modifier cette valeur.  | Toute propriété système.                                         |
| sortList              | Spécifie une liste triée des colonnes par lesquelles trier les résultats.                                       | Jusqu’à quatre propriétés système. L’utilisateur peut modifier cette liste. |
| stackList             | À usage interne uniquement. Ne pas utiliser.                                                                 | n/a                                                          |

## <a name="query-element"></a>Élément \<query>

L' \<query> élément spécifie les attributs qui définissent la façon dont les résultats sont interrogés. L’exemple suivant illustre la structure de l’élément.

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Éléments enfants

La table suivante décrit les éléments enfants de l’élément \<scope>.

| Élément    | Description                                                                                                               | Valeur                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fournisseurs  | À usage interne uniquement. Ne pas utiliser.                                                                                        | n/a                                                                                                                                                                                                                                                            |
| Sous-requêtes | À usage interne uniquement. Ne pas utiliser.                                                                                        | n/a                                                                                                                                                                                                                                                            |
| Étendue      | Identifie les emplacements à inclure ou exclure dans la recherche.                                                                 | Un chemin d’accès ou un [ID de dossier connu](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) de l’emplacement à inclure ou à exclure. Cet élément peut également spécifier si la recherche doit inclure ou exclure des chemins enfants (une recherche superficielle ou profonde). |
| kindList   | Identifie le type de fichier (s) à rechercher.                                                                             | Toute valeur System. Kind.                                                                                                                                                                                                                                         |
| conditions | Spécifie les règles de filtrage des résultats. Par exemple, les résultats peuvent être limités aux e-mails envoyés par ou à une personne particulière. | andCondition, orCondition, notCondition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>Élément \<scope>

L' \<scope> élément identifie les emplacements à inclure ou à exclure de la recherche. L' \<scope> élément doit contenir au moins un \<include> élément enfant présent et zéro, un ou plusieurs \<exclude> éléments. Les emplacements peuvent être spécifiés en tant que chemin d’accès (les variables d’environnement sont prises en charge) ou en tant qu' [identificateur de dossier connu](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid). En outre, chacun de ces emplacements peut être spécifié pour être recherché en profondeur ou superficielle en affectant à la valeur « true » ou « false » (valeur par défaut). Les parties de la liste d’emplacements incluse peuvent être exclues en spécifiant des éléments d’exclusion.

L’exemple suivant montre un \<scope> élément qui recherche le dossier spécial documents, mais pas ses enfants, le volume « e : » et ses enfants, mais pas le répertoire « e : \\ Windows » ou l’un de ses enfants :

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>Élément \<kindList>

Ces éléments définissent l’Union du « genre » d’éléments qui doivent apparaître dans la bibliothèque. Les valeurs valides sont les suivantes :

- calendrier
- communication
- contact
- document
- email
- feed
- dossier
- SideWinder
- instantmessage
- journaux
- link
- film
- music
- remarque
- picture
- programme
- recordedtv
- SearchFolder
- tâche
- video
- webhistory
- item
- other

### <a name="conditions-element"></a>Élément \<conditions>

Les conditions sont des filtres par rapport auxquels les résultats de recherche sont comparés. Par exemple, vous pouvez filtrer les résultats qui répondent à certains critères, tels que le nom de l’auteur ou la taille du fichier. L’ensemble de conditions est intégré à une arborescence de condition unique avec des branches logiques AND, OR et NOT.

L’exemple suivant illustre la structure de l' \<condition> élément.

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

Le type de condition peut être l’un des suivants :

| Type          | Description                                 | Attributs disponibles                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| andCondition  | Combinaison de deux ou plusieurs conditions enfants | n/a                                                |
| orCondition   | Disjonction de deux autres conditions enfants | n/a                                                |
| notCondition  | Négation d’une condition enfant               | n/a                                                |
| leafCondition | Compare une propriété à la valeur                | Property, propertyType, Operator, value, ValueType |

Les \<leafCondition> attributs de l’élément identifient les propriétés et les valeurs par rapport auxquelles les résultats sont filtrés.

### <a name="example-conditions-element"></a>Exemple : \<conditions> élément

L’exemple suivant filtre les résultats pour tous les éléments non lus créés par John. Autrement dit, la propriété System. IsRead a la valeur false et la chaîne « John » apparaît dans les propriétés System. Author ou System. ItemAuthors.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>Élément \<properties>

L' \<properties> élément décrit les propriétés de la recherche enregistrée elle-même. Les fichiers de recherche enregistrés prennent en charge quatre propriétés : \<author> ,, \<kind> \<description> et \<tags> . Ils sont destinés à un usage interne uniquement.

## <a name="full-specification-of-the-search-ms-file-format"></a>Spécification complète de la recherche-format de fichier MS

Voici un exemple de code XML complet pour un fichier de recherche enregistré.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Exemples de recherches enregistrées

Voici des exemples de \* fichiers. search-ms.

### <a name="recent-documentssearch-ms"></a>Documents récents. search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>récents Musique. search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Récemment partagés par moi. search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
