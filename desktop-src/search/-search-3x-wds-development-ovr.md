---
description: pour indexer le contenu et les propriétés de nouveaux formats de fichier et de banques de données, vous devez étendre la recherche Microsoft Windows à l’aide de compléments.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search en tant que plateforme de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313290"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search en tant que plateforme de développement

pour indexer le contenu et les propriétés de nouveaux formats de fichier et de banques de données, vous devez étendre la recherche Microsoft Windows à l’aide de compléments.

pour qu’un développeur tiers de nouveaux formats de fichier et de magasins de données puisse faire apparaître ces formats et magasins dans les résultats de la requête dans Windows Explorer, le développeur doit effectuer les trois opérations suivantes :

-   Implémentez une source de données Shell pour étendre l’espace de noms Shell.
-   Exposer des éléments dans un magasin de données (s’ils ajoutent un nouveau magasin de données, car il doit être indexé).
-   développez un gestionnaire de protocole afin que Windows recherche puisse accéder aux données pour l’indexation.

Cette rubrique est organisée comme suit :

-   [Prise en main](#getting-started)
-   [Vue d’ensemble des scénarios de développement de recherche](#overview-of-search-development-scenarios)
    -   [Ajout d’un nouveau magasin de données](#adding-a-new-data-store)
    -   [Ajout d’un nouveau format de fichier](#adding-a-new-file-format)
    -   [utilisation des résultats de la recherche Windows](#consuming-windows-search-results)
-   [Vue d’ensemble des gestionnaires](#overview-of-handlers)
-   [Instructions du programme d’installation du complément](#add-in-installer-guidelines)
-   [Remarque à l’attention des implémenteurs](#note-to-implementers)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="getting-started"></a>Mise en route

avant de commencer à créer une application de recherche Windows, n’oubliez pas que la meilleure façon de procéder consiste à utiliser une source de données Shell. Une source de données Shell étend l’espace de noms Shell et expose les éléments dans un magasin de données. les éléments dans le magasin de données peuvent ensuite être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole. cette approche indirecte permettant d’accéder à Windows recherche en implémentant une source de données shell est préférable, car elle permet d’accéder aux fonctionnalités complètes de l’interpréteur de commandes. Cela garantit une expérience utilisateur raisonnable.

si vous souhaitez que les résultats de la requête s’affichent dans l’explorateur de Windows, vous devez implémenter une source de données Shell avant de pouvoir créer un gestionnaire de protocole pour étendre l’index. Toutefois, si toutes les requêtes sont par programmation (par exemple OLE DB) et interprétées par le code de l’application plutôt que par le shell, un espace de noms Shell est toujours préféré, mais pas obligatoire.

un gestionnaire de protocole est requis pour Windows pour obtenir des informations sur le contenu d’un fichier, comme des éléments dans des bases de données ou des types de fichiers personnalisés. si Windows recherche peut indexer le nom et les propriétés du fichier, Windows n’a aucune connaissance du contenu du fichier. par conséquent, ces éléments ne peuvent pas être indexés ou exposés dans le Shell Windows. En implémentant un gestionnaire de protocole personnalisé, vous pouvez exposer ces éléments. Pour obtenir la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, consultez [vue d’ensemble des gestionnaires](#overview-of-handlers).

## <a name="overview-of-search-development-scenarios"></a>Vue d’ensemble des scénarios de développement de recherche

les scénarios de développement les plus courants dans Windows Search sont les suivants :

-   [Ajout d’un nouveau magasin de données](#adding-a-new-data-store)
-   [Ajout d’un nouveau format de fichier](#adding-a-new-file-format)
-   [utilisation des résultats de la recherche Windows](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Ajout d’un nouveau magasin de données

vous avez besoin d’un magasin de données Shell pour Windows la recherche uniquement si vous ajoutez un nouveau magasin de données à indexer. Un magasin de données est un référentiel de données qui peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur à l’aide d’une source de données Shell. les éléments d’un magasin de données peuvent ensuite être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole. Le gestionnaire de protocole implémente le protocole d’accès à une source de contenu dans son format natif. Les interfaces [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) et [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) permettent d’implémenter un gestionnaire de protocole personnalisé pour développer les sources de données qui peuvent être indexées. Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Ajout d’un nouveau format de fichier

Si vous ajoutez un nouveau format de fichier personnalisé, vous devez développer un gestionnaire de filtres ou un gestionnaire de propriétés, mais pas les deux. Un filtre est une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Il ouvre les fichiers d’un type de fichier particulier et filtre les propriétés et les blocs de texte de l’indexeur. Les filtres sont associés à des types de fichiers, tels qu’ils sont signalés par des extensions de nom de fichier, des types MIME ou des identificateurs de classe (CLSID). Bien qu’un filtre puisse gérer plusieurs types de fichiers, chaque type de fichier fonctionne avec un seul filtre.

un gestionnaire de propriétés traduit les données stockées dans un fichier dans un schéma structuré qui est reconnu par et est accessible par Windows Explorer, Windows Search et d’autres applications. Ces systèmes peuvent ensuite interagir avec le gestionnaire de propriétés pour écrire et lire des propriétés vers et à partir d’un fichier. Les données traduites comprennent la vue détails, info-bulles, le volet Détails, les pages de propriétés, etc. Chaque gestionnaire de propriétés est associé à un type de fichier particulier, identifié par l’extension de nom de fichier. Vous avez besoin d’un gestionnaire de propriétés pour effectuer les opérations suivantes :

-   Affichez les propriétés des éléments non indexés dans l’interface utilisateur.
-   Prise en charge de l’écriture des propriétés.

### <a name="consuming-windows-search-results"></a>utilisation des résultats de la recherche Windows

les sections suivantes décrivent plusieurs manières de consommer Windows les résultats de la recherche :

-   [Interrogation des données](#querying-data)
-   [Interrogation des magasins de données distants (recherche fédérée)](#querying-remote-data-stores-federated-search)
-   [Indexation des fichiers et des éléments](#indexing-files-and-items)
-   [Indexation d’un magasin de données](#indexing-a-data-store)
-   [Gestion du processus d’indexation](#managing-the-indexing-process)
-   [intégration du système de propriétés Windows avec les applications de recherche Windows](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Interrogation des données

les développeurs écrivant des applications en plus de la recherche de Windows et du système de propriétés Windows peuvent accéder aux fichiers et aux éléments, quel que soit le type d’application ou de fichier. Il existe deux façons pour les applications d’accéder aux données de l’indexeur :

-   les Applications communiquent directement avec OLE DB en envoyant des requêtes de langage SQL de recherche Windows (SQL) au fournisseur Windows de recherche pour récupérer les résultats. les requêtes peuvent être construites manuellement ou à l’aide de l’interface [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) pour générer le SQL à partir de mots clés de recherche et de la syntaxe de requête avancée (AQS).
-   Les applications fonctionnent par le biais de la couche de Shell. L’avantage de la couche de Shell est qu’elle prend également en charge d’autres sources telles que grep. Toutefois, l’inconvénient est que toutes les fonctionnalités de l’indexeur ne sont pas disponibles.

une autre option consiste à utiliser les protocoles search-ms://et search://, qui exécutent des recherches basées sur les URL rendues via Windows Explorer. Cette option active le développement le plus clair, mais ne retourne pas les résultats ou les sélections de l’utilisateur de la vue des résultats à l’application appelante. De même, comme d’autres protocoles, les applications de recherche tierces peuvent reprendre les protocoles search-ms://et search://si les applications sont conformes à l’ensemble de fonctionnalités requis. pour plus d’informations sur l’interrogation, consultez [processus d’interrogation dans Windows rechercher](querying-process--windows-search-.md) et [interroger l’Index par programmation](-search-3x-wds-qryidx-overview.md).

### <a name="querying-remote-data-stores-federated-search"></a>Interrogation des magasins de données distants (recherche fédérée)

dans Windows 7 et versions ultérieures, la recherche fédérée offre un nouveau moteur de recherche qui interroge les magasins de données distants via des serveurs web, via le protocole [OpenSearch](https://github.com/dewitt/opensearch) , et énumère les résultats sous forme de flux RSS ou atom XML. Les connecteurs de recherche sont des jonctions d’espaces de noms qui simulent le comportement des dossiers à l’aide d’un moteur de recherche. pour plus d’informations sur la fédération des recherches aux magasins de données distants dans Windows 7, consultez [recherche fédérée dans Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indexation des fichiers et des éléments

le contenu indexé est basé sur les types de fichiers et de données pris en charge par le biais des compléments inclus avec Windows recherche et les règles d’inclusion et d’exclusion par défaut pour les dossiers dans le système de fichiers. par exemple, les filtres inclus dans la recherche de fenêtre prennent en charge plus de 200 types de données courants, y compris les documents Microsoft Office, Microsoft Outlook la messagerie électronique (conjointement avec le gestionnaire de protocole MAPI), les fichiers en texte brut, le code HTML et bien plus encore. Pour obtenir la liste complète des types de fichiers pris en charge en mode natif, consultez [ce qui est inclus dans l’index](-search-3x-wds-included-in-index.md).

l’index peut être étendu à l’aide de gestionnaires de propriétés et de filtres pour exposer le contenu et les propriétés de nouveaux formats de fichier à l’index et à l’explorateur de Windows. Les filtres sont une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Il existe deux types de filtres : un qui interagit avec des éléments individuels tels que des fichiers et un autre qui interagit avec des conteneurs tels que des dossiers. Les filtres sont polyvalents en ce sens qu’ils prennent en charge la segmentation des données, du texte, des propriétés et des langues multiples.

En revanche, les gestionnaires de propriétés ont un objectif plus spécifique : pour exposer les propriétés de types de fichiers spécifiques qui sont identifiés par les extensions de nom de fichier. Un gestionnaire de propriétés pour un type de fichier peut activer les propriétés obtenir et définir, et peut énumérer les propriétés associées à ce type de fichier. Contrairement aux filtres, les gestionnaires de propriétés ne prennent pas en charge le contenu de données ou de texte, et les gestionnaires de propriétés n’ont aucun moyen d’indiquer le langage dans lequel se trouve une propriété de texte, sauf s’ils prennent en charge l’écriture de propriétés.

### <a name="indexing-a-data-store"></a>Indexation d’un magasin de données

L’index peut être étendu à l’aide de gestionnaires de protocole pour fournir l’accès aux magasins de données propriétaires. Par exemple, les fichiers et les éléments contenus dans des magasins de données non-système de fichiers (tels que les bases de données et les magasins de courrier électronique) requièrent un gestionnaire de protocole pour mapper une URL vers un flux. Les gestionnaires de protocole peuvent également déterminer les filtres corrects à utiliser pour extraire des informations d’un flux. Les filtres énumèrent les URL du magasin de données. Les éléments sont ensuite indexés individuellement à l’aide du filtre et/ou du gestionnaire de propriétés approprié. Pour plus d’informations, consultez [extension de l’index](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Gestion du processus d’indexation

les développeurs d’applications peuvent contrôler l’étendue et la fréquence de Windows l’indexation de la recherche à l’aide de différentes interfaces de gestion. Ces interfaces incluent des fonctionnalités permettant d’ajouter et de supprimer les répertoires dans lesquels l’indexeur analyse les modifications, de notifier manuellement l’index des modifications apportées aux données, de vérifier l’état de l’indexeur et de forcer la réindexation d’une partie ou de la totalité des données. Pour plus d’informations, consultez [gestion de l’index](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>intégration du système de propriétés Windows avec les Applications de recherche Windows

le système de propriétés Windows est un système extensible en lecture/écriture de définitions de données qui offre un moyen uniforme d’exprimer des métadonnées sur les éléments de l’interpréteur de commandes. le système de propriétés Windows dans Windows Vista et versions ultérieures vous permet de stocker et de récupérer des métadonnées pour les éléments de Shell. Un élément de Shell est un élément de contenu unique, tel qu’un fichier, un dossier, un message électronique ou un contact. Une propriété est un élément de métadonnées individuel associé à un élément de Shell. Les valeurs de propriété sont exprimées sous la forme d’une structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Une liste complète de propriétés communes est incluse pour un certain nombre de types d’éléments courants tels que des photos, de la musique, des documents, des messages, des contacts et des fichiers. Les développeurs peuvent également présenter leurs propres propriétés à la plateforme si aucune propriété existante ne répond à leurs besoins. pour plus d’informations sur l’intégration d’applications avec le système de propriétés Windows, consultez [développement de gestionnaires de propriétés](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Vue d’ensemble des gestionnaires

Un gestionnaire est un objet COM (Component Object Model) qui fournit les fonctionnalités d’un élément de Shell. La plupart des sources de données Shell offrent un système extensible pour lier les gestionnaires aux éléments. Par exemple, le dossier de système de fichiers utilise le système d’association pour rechercher les gestionnaires pour un type de fichier particulier. Un gestionnaire spécifique est requis pour chaque type de fichier. Un gestionnaire de filtre est requis pour le type de fichier Adobe Acrobat .pdf, par exemple, un autre gestionnaire de filtres est requis pour le format de fichier .doc, et ainsi de suite.

Différents gestionnaires présentent des similitudes. dans Windows Vista et versions ultérieures, tous les gestionnaires doivent utiliser l’une des interfaces suivantes pour initialiser le gestionnaire : [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

Le tableau suivant répertorie les principales tâches de développement, le type de gestionnaire requis pour chaque tâche et fournit un lien vers des informations conceptuelles sur l’exécution de chaque tâche.



| Tâche                                                                                                                                                            | Handler                          | Informations conceptuelles                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accès aux propriétés d’un fichier pour l’indexation                                                                                                                 | Gestionnaire de propriétés                 | [Développement de gestionnaires de propriétés](-search-3x-wds-extidx-propertyhandlers.md)<br/> [Propriétés définies par le système pour les formats de fichiers personnalisés](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Ajout de formats de presse-papiers pour l’objet de données ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) d’un élément (les objets de données sont utilisés dans les scénarios de glisser-déplacer et de copier/coller.) | Gestionnaire d'objets de données              | [Création de gestionnaires de données](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Ajout de verbes pour un élément qui sont généralement affichés dans un menu contextuel                                                                                         | Gestionnaire de menu contextuel            | [Création de gestionnaires de menu contextuel](../shell/context-menu-handlers.md)<br/> [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Association d’un type de fichier à une icône spécifique                                                                                                                    | Gestionnaire d’icône                     | [Créer des gestionnaires d’icône](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Création de feuilles de propriétés avec des images et des contrôles d’interface utilisateur qui autorisent une interaction personnalisée avec un type de fichier                                                          | Gestionnaire de feuille de propriétés           | [Gestionnaires de feuille de propriétés](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Activation d’un type d’élément pour prendre en charge les scénarios de glisser-déplacer et de copier/coller                                                                                         | Supprimer le gestionnaire                     | [Transfert d’objets Shell avec glisser-déplacer et le presse-papiers](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Extraction de segments de texte et de propriétés de document pour l’indexation                                                                                                  | Gestionnaire de filtres                   | [Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indexation d’un nouveau type de fichier                                                                                                                                        | Gestionnaire de filtres, gestionnaire de propriétés | [Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)<br/> [Développement de gestionnaires de propriétés](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indexation du contenu d’un magasin de données                                                                                                                           | Gestionnaire de protocole                 | [Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)                                                                                                                                            |
| aperçu d’une vue simplifiée de l’élément de Shell dans le volet de visualisation de l’explorateur de Windows                                                                             | Gestionnaire d’aperçus                  | [Gestionnaires d’aperçus](../shell/preview-handlers.md)                                                                                                                                                             |
| Fournir du texte contextuel quand une souris pointe sur un objet d’interface utilisateur                                                                                                      | Gestionnaire d'info-bulle                  | [Création de gestionnaires d’extension de Shell](../shell/handlers.md) (personnalisation de l’info-bulle)                                                                                                                            |
| Fournir une image statique pour représenter un élément de Shell                                                                                                              | Gestionnaire de miniatures                | [Gestionnaires de miniatures](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

Le tableau suivant répertorie les gestionnaires et les interfaces permettant d’implémenter chaque type de gestionnaire.



| Handler                | Interfaces                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supprimer le gestionnaire           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), [**IDropTargetHelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Gestionnaire d'objets de données    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Gestionnaire de filtres         | [**Filtres**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Gestionnaire d’icône           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Facultatif : [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| Gestionnaire d'info-bulle        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Gestionnaire d’aperçus        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Gestionnaire de propriétés       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Gestionnaire de protocole       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol), [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Facultatif : [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2), [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2), [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3), [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Gestionnaire de feuille de propriétés | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Gestionnaire de menu contextuel  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Gestionnaire de miniatures      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> Un gestionnaire de propriétés est parfois kown comme un gestionnaire de métadonnées. Une source de données Shell est parfois appelée extension d’espace de noms Shell. Un gestionnaire de type de fichier est parfois appelé gestionnaire d’extensions de Shell ou extension de Shell.

 

Pour plus d’informations sur la création de gestionnaires, consultez [création de gestionnaires d’extension de Shell](../shell/handlers.md). pour plus d’informations sur les propriétés, consultez [Windows système de propriétés](../properties/windows-properties-system.md).

## <a name="add-in-installer-guidelines"></a>Instructions du programme d’installation du complément

Pour créer un programme d’installation de complément, suivez les instructions ci-dessous :

-   Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.
-   Des notes de publication doivent être fournies.
-   Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.
-   Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.
-   Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.
-   Si un complément plus récent a remplacé un complément précédent, l’utilisateur doit être en mesure de restaurer les fonctionnalités du complément précédent et de le rendre à nouveau dans le complément par défaut pour ce type de fichier ou ce magasin.

## <a name="note-to-implementers"></a>Remarque à l’attention des implémenteurs

Avant de créer un gestionnaire de filtres ou de propriétés, les développeurs doivent tenir compte des éléments suivants :

-   ces gestionnaires sont des extensions in-process qui sont chargées dans des processus que vous ne contrôlez pas, tels que le processus de démon de filtre, l’explorateur de Windows (recherche grep) et des hôtes tiers comme Windows Mail).
-   Vous devez écrire un code sécurisé suffisamment robuste pour gérer les formes arbitrairement endommagées de votre format de fichier qui ont été créées pour attaquer le système.
-   Votre complément ne doit pas entraîner de fuite de ressources qui génèrent des problèmes pour les processus hôtes.
-   Votre complément ne doit pas se bloquer, car cela entraînera également le blocage des processus de l’hôte et ralentira le processus de filtrage.
-   Étant donné que ces gestionnaires sont exécutés dans un processus système en arrière-plan, ils doivent fonctionner rapidement avec un minimum d’UC et d’e/s consommées pour répondre aux exigences de performances du système.

Par conséquent, ces compléments doivent être écrits par les développeurs ayant une expertise dans la création de code au niveau du système.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   Pour les sources de données qui doivent utiliser l’objet de vue du dossier système par défaut de l’interpréteur de commandes (DefView), consultez [implémentation d’un affichage des dossiers](../lwef/nse-folderview.md), fonction [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) et [**SFV \_ créer**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) une structure. Les sources de données qui utilisent l’objet de vue du dossier système par défaut de l’interpréteur de commandes (DefView) doivent implémenter l’ensemble d’interfaces suivant : [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)et (éventuellement) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Si votre implémentation de **IShellFolder** n’utilise pas **SHCreateShellFolderView** pour créer le DefView, l’objet de vue de Shell peut avoir besoin de [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview).
-   [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) est l’interface principale pour les consommateurs de la source de données Shell appelée DBFolder. Pour plus d’informations sur DBFolder, consultez la description de la \_ constante d’analyse Str \_ avec des \_ Propriétés dans les [**clés de chaîne de contexte de liaison**](../shell/str-constants.md). Voir aussi [tableaux d’association](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) et [**IPropertySystem :: GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)de la programmation. pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez la documentation de l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .
-   pour les tableaux de messages pris en charge par la communauté sur les technologies de recherche, consultez [Windows : rechercher des forums](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) sur MSDN.
-   pour obtenir des exemples de code associés, consultez [Windows des exemples de code de recherche](-search-samples-ovw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[langues prises en charge par la recherche de Windows](-search-3x-wds-language-support.md)
</dt> <dt>

[Utilisation de code managé avec Shell Data et Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Windows Rechercher dans le Guide du développeur](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 
