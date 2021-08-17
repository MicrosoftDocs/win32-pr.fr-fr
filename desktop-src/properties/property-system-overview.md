---
description: le système de propriétés Windows est un système extensible en lecture/écriture de définitions de données qui offre un moyen uniforme d’exprimer des métadonnées sur les éléments de l’interpréteur de commandes.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Cliquez sur Vue d’ensemble du système de propriétés.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742eebbdb05541a3cfcc1468cd0f93d255f13b67b4bfe777729d1d02d2ed70a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460029"
---
# <a name="property-system-overview"></a>Cliquez sur Vue d’ensemble du système de propriétés.

le système de propriétés Windows est un système extensible en lecture/écriture de définitions de données qui offre un moyen uniforme d’exprimer des métadonnées sur les éléments de l’interpréteur de commandes. le système de propriétés Windows dans Windows Vista et versions ultérieures vous permet de stocker et de récupérer des métadonnées pour les éléments de Shell. Un élément de Shell est un élément de contenu unique, tel qu’un fichier, un dossier, un message électronique ou un contact. Une propriété est un élément de métadonnées individuel associé à un élément de Shell. Les valeurs de propriété sont exprimées sous la forme d’une structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Cette rubrique est organisée comme suit :

-   [Introduction](#introduction)
-   [Scénarios de développement](#development-scenarios)
-   [propriétés et Windows la recherche](#properties-and-windows-search)
-   [Remarque à l’attention des implémenteurs](#note-to-implementers)
-   [Windows Documentation du système de propriétés](#windows-property-system-documentation)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Les propriétés sont identifiées de manière unique par leur nom canonique (tel que `System.Document.LastAuthor` ) et la clé de propriété (par exemple, `PKEY_Document_LastAuthor` ). Une clé de propriété (groupe de caractères) est la partie nom d’une paire nom-valeur qui se compose d’un type d’emplacement/de PROPVARIANT ou d’une chaîne/PROPVARIANT, où la chaîne est le nom canonique du groupe de caractères (par exemple `System.Document.LastAuthor` ). Un élément de tableau est une définition qui indique au système de propriétés tout ce qu’il doit savoir sur la propriété, tandis que la valeur est une instance réelle de la propriété. Un groupe de la groupe contient en interne un formatID et un propID.

Une propriété individuelle se compose des trois éléments suivants :

-   Nom canonique, tel que `System.Music.Artist` .
-   Description de schéma, spécifiée au format de fichier XML. propDesc et exprimée par programme par le biais de [**IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Valeur, telle que le nom d’un singe.

La description du schéma se compose d’informations sur la propriété, telles que le nom de la propriété, le type de données, les contraintes, des informations sur la façon dont la propriété interagit avec les vues et le système de recherche, etc. Le nom et la description du schéma sont définis globalement, et sont les mêmes pour tous les éléments et types. Une valeur est spécifique à un élément individuel. Autrement dit, la `System.Music.Artist` propriété est toujours définie comme une chaîne à valeurs multiples, mais elle peut avoir une valeur différente (ou aucune valeur) pour chaque élément.

un gestionnaire de propriétés traduit les données stockées dans un fichier dans un schéma structuré qui est reconnu par et est accessible par Windows Explorer, Windows Search et d’autres applications. Ces systèmes peuvent ensuite interagir avec le gestionnaire de propriétés pour écrire et lire les propriétés vers et à partir du fichier. les données traduites sont exposées par programme et présentées à l’utilisateur par le biais de l’explorateur de Windows dans divers contextes, notamment le mode détails, info-bulles, le volet détails, les pages de propriétés, etc. Chaque gestionnaire de propriétés est associé à un type de fichier particulier, qui est identifié par l’extension de nom de fichier. Les développeurs doivent implémenter un gestionnaire de propriétés qui produit et utilise le format natif de son type de fichier, par exemple .jpg ou .png, ou utiliser le magasin de propriétés In-Memory, qui produit et utilise le format binaire MS-PROPSTORE.

le système de propriétés Windows crée un modèle de données abstrait qui fournit un niveau d’abstraction à partir de formats de fichier individuels. le modèle de données abstrait fourni par le système de propriétés Windows est une méthode permettant de lire et d’écrire un ensemble extensible de valeurs nommées associées à un élément de Shell. L’expression de valeur est flexible, prend en charge de nombreux types de données et est extensible, ce qui permet d’exprimer des données arbitraires (**\_ objet BLOB VT**) et des objets sous la forme d’une valeur.

En raison de l’abstraction, vous pouvez interroger les attributs ou les métadonnées d’un élément. parmi les exemples d’éléments pouvant être abstraits, citons Microsoft Office documents, les balises ID3 et les AutoCAD et d’autres logiciels propriétaires tiers. De même, si vous avez un fichier. jpeg, vous pouvez utiliser les codecs. jpeg et EXIF pour lire les octets du fichier afin de découvrir les dimensions de l’image. Si vous avez un fichier .png à la place, vous avez besoin d’un codec différent et de code différent pour le faire. l’utilisation du système de propriétés Windows évite ce type de problème. si vous implémentez un nouveau type de fichier, vous avez la possibilité de brancher l’abstraction uniforme offerte par le système de propriétés Windows et de spécifier comment rendre vos métadonnées consommables. pour ces raisons, il est toujours préférable d’utiliser la plateforme commune fournie par le système de propriétés Windows.

## <a name="development-scenarios"></a>Scénarios de développement

Les propriétés sont exprimées par les producteurs et par les consommateurs. dans ce contexte, les producteurs sont les conventes de propriétés dans le Windows le système de propriétés et les consommateurs sont des applications (et leurs développeurs) qui consomment les informations de propriété de ce système. les utilisations de et des participants au système de propriétés Windows sont identifiées dans le tableau suivant.



| utilisation du système de propriétés Windows                                                                                                                                                                                            | Participant |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Un bloc de construction qui fournit un registre extensible des descriptions de propriété, une implémentation de magasin de propriétés en mémoire et des services pour la liaison à des gestionnaires de propriétés, la conversion de types et la sérialisation des magasins de propriétés. | Consommateur    |
| Applications qui veulent lire et écrire des propriétés de manière abstraite.                                                                                                                                                       | Consommateur    |
| La propriété inventorie qui définit de nouvelles propriétés pour le système de propriétés en définissant des schémas de propriétés personnalisées et en développant leurs propres gestionnaires de propriétés.                                                                          | Producer    |
| Propriétaires de format de fichier qui souhaitent activer l’accès aux propriétés stockées dans leurs formats de fichiers personnalisés.                                                                                                                           | Producer    |



 

Les consommateurs utilisent des propriétés, des schémas et des gestionnaires de propriétés existants. Les propriétés disponibles pour la consommation incluent les propriétés en lecture/écriture des gestionnaires de propriétés pour les types de fichiers pris en charge et peuvent également inclure des propriétés personnalisées. Les schémas disponibles incluent au moins le schéma système, et parfois d’autres encore. Un consommateur peut créer une application pour consommer les métadonnées et générer une vue basée sur l’artiste, quels que soient les dossiers dans lesquels les éléments sont stockés. La hiérarchie des dossiers de fichiers n’est pas pertinente. Par exemple, vous pouvez spécifier tous les éléments de chanson d’un type d’élément particulier sans vous préoccuper de l’emplacement de ces éléments. ce scénario complexe de bout en bout n’est pas limité au système de propriétés Windows, mais il implique plusieurs composants différents, tels que les dossiers d’indexation et de recherche.

les conventes de propriété, ou développeurs tiers, sont des producteurs dans le système de propriétés Windows. lorsque vous préparez la définition d’une nouvelle propriété, inspectez d’abord le jeu de propriétés que Windows définit. Si vous en trouvez un qui répond à vos besoins, du type et de la sémantique qui correspondent à votre utilisation requise, utilisez cette propriété et n’inventez pas une nouvelle. Si vous définissez une nouvelle propriété personnalisée, essayez d’obtenir un accord avec d’autres développeurs qui peuvent l’utiliser et publier le résultat de ce contrat afin qu’ils puissent rejoindre la communauté des utilisateurs de cette propriété.

les producteurs peuvent tirer parti de la fonctionnalité de l’explorateur de Windows. par exemple, si vous écrivez un nouveau format d’image et que vous implémentez un gestionnaire de propriétés, votre nouveau format de fichier devient disponible dans l’explorateur de Windows. les utilisateurs peuvent ensuite baliser leurs photographies et faire pivoter leur collection de photographies selon n’importe quelle propriété dans le système de propriétés Windows. En fait, tout ce que l’interpréteur de commandes utilise avec les propriétés, les développeurs tiers peuvent le faire dans leurs propres applications. Cela comprend le regroupement, le tri, l’interrogation et l’affichage des propriétés complètes. l’expérience utilisateur que Windows Explorer fournit peut être largement implémentée par des tiers avec des api disponibles publiquement. Windows L’Explorateur peut être remplacé ou étendu à l’aide de ces API.

du point de vue d’une application qui utilise le modèle de données Shell, il existe un grand nombre de scénarios qui impliquent l’utilisation du système de propriétés Windows. Les applications de gestion des médias sont un exemple évident. Les scénarios de système de propriétés principaux incluent des scénarios tels que la lecture de la propriété de mot clé d’une photographie ou la définition de la propriété DateTaken. exemples de scénarios d’intégration de bout en bout que le système de propriétés Windows active, mais qui requièrent plusieurs autres composants pour fonctionner, incluent l’indication de toutes les images ou la recherche d’un document qui contient un mot clé.

## <a name="properties-and-windows-search"></a>propriétés et Windows la recherche

les propriétés servent les producteurs et les consommateurs lorsqu’ils interagissent avec Windows recherche et l’indexation. Windows la recherche a un cache de valeurs de propriétés qui sont utilisées dans l’implémentation du Search Service Windows (WSS). ces valeurs de propriété peuvent être interrogées par programme à l’aide du fournisseur de OLE DB de recherche Windows, ou via [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), qui représente des éléments dans les résultats de recherche et les vues basées sur des requêtes. Windows La recherche collecte et stocke ensuite les propriétés émises par les gestionnaires de filtres ou les gestionnaires de propriétés lorsqu’un élément, tel qu’un document Word, est indexé. Ce magasin est supprimé et reconstruit lors de la reconstruction de l’index.

> [!Note]  
> N’oubliez pas que lorsque vous réinscrivez un schéma, les modifications apportées aux attributs des propriétés précédemment définies peuvent ne pas être respectées par l’indexeur. La solution consiste soit à reconstruire l’index, soit à introduire de nouvelles propriétés reflétant les modifications au lieu de mettre à jour les anciennes. Pour plus d’informations, consultez la section [Remarque à l’attention des implémenteurs](#note-to-implementers) plus loin dans cette rubrique.

 

Par exemple, un développeur qui crée une application multimédia souhaite montrer aux utilisateurs de l’application toutes les musiques disponibles par un artiste particulier. L’application fournit à l’utilisateur une liste des artistes disponibles, puis génère une liste de toutes les musiques disponibles par l’artiste que l’utilisateur sélectionne. Ou un utilisateur final peut vouloir effectuer une requête pour ? Artist : Beethoven ?, et être exposé à la liste complète des propriétés disponibles au cours de la recherche. Cet exemple implique l’utilisation de l’espace de noms Shell, des gestionnaires de propriétés et/ou de l’interrogation de l’index par le biais de l’un des éléments suivants :

-   Source de données Shell.
-   Fournisseur OLE DB.
-   fichier de recherche enregistré (. search-ms) utilisé pour lancer une requête en accédant au fichier de recherche dans Windows Explorer ou en liant par programmation à [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

> [!Note]  
> Bien que la `System.Kind` propriété ne participe pas à ce scénario d’application multimédia, elle peut être utilisée pour générer une requête qui retourne tous les fichiers. search-ms dans une étendue particulière.

 

la meilleure façon d’accéder aux api de recherche et de créer des applications de recherche Windows se fait via une source de données Shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) est un composant qui peut créer des instances de la source de données du dossier de recherche, qui est un type de source de données « virtuelles » fourni par le shell qui peut exécuter des requêtes sur d’autres sources de données dans l’espace de noms Shell et énumérer les résultats. Il peut le faire à l’aide de l’indexeur ou en énumérant manuellement et en inspectant des éléments dans les étendues spécifiées.

les développeurs tiers peuvent créer des applications qui consomment les données de l’index par le biais de requêtes de programmation et peuvent étendre les données dans l’index pour les types de fichiers et d’éléments personnalisés à indexer par Windows recherche. si vous souhaitez afficher les résultats de la requête dans l’explorateur de Windows, vous devez implémenter une source de données Shell avant de pouvoir créer un gestionnaire de protocole pour étendre l’index. Toutefois, si toutes les requêtes sont par programmation (par exemple OLE DB) et interprétées par le code de l’application plutôt que par le shell, un espace de noms Shell est toujours préféré, mais pas obligatoire. un gestionnaire de protocole est requis pour Windows pour obtenir des informations sur le contenu des fichiers, tels que des éléments dans les bases de données ou des types de fichiers personnalisés. si Windows recherche peut indexer le nom et les propriétés du fichier, Windows n’a pas d’informations sur le contenu du fichier. par conséquent, ces éléments ne peuvent pas être indexés ou exposés dans le Shell Windows. En implémentant un gestionnaire de protocole personnalisé, vous pouvez exposer ces éléments. pour obtenir la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, consultez « vue d’ensemble des gestionnaires » dans [Windows la recherche en tant que plateforme de développement](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Une source de données Shell est parfois appelée extension d’espace de noms Shell. Un gestionnaire est parfois appelé extension d’interpréteur de commandes ou gestionnaire d’extensions de Shell.

 

## <a name="note-to-implementers"></a>Remarque à l’attention des implémenteurs

En raison des problèmes potentiels que l’indexeur peut avoir lors de l’utilisation du schéma du système de propriétés, il est essentiel de définir des attributs avec soin et de façon stratégique pour la première version du schéma. Toutes les modifications apportées aux attributs (type, largeur de colonne, qu’il s’agisse de indexible) ne seront pas reflétées dans la base de données après l’inscription d’un schéma. Pour que ces modifications soient reconnues après que le schéma a été inscrit une fois sur un système, il suffit de reconstruire l’index, puis d’inscrire le nouveau schéma, ou d’inscrire le schéma, puis de créer une nouvelle propriété pour chaque version ultérieure. par exemple `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , et ainsi de suite. Nous vous déconseillons de créer de nouvelles propriétés de cette manière, car plusieurs colonnes superflues peuvent avoir un impact sur les performances du système.

## <a name="windows-property-system-documentation"></a>Windows Documentation du système de propriétés

Le reste de cette documentation contient les sections suivantes :

-   [Windows Guide du développeur de système de propriétés](property-system-developer-s-guide.md)

    décrit en détail comment implémenter les principaux scénarios de développement à l’aide du système de propriétés Windows.

-   [Référence du système de propriétés](property-system-reference.md)

    documente [les propriétés de Windows](props.md), le schéma de Description de [propriété](property-description-schema.md), les [Interfaces](interfaces.md), les [fonctions](functions.md), les [Structures](structures.md), les [constantes, les énumérations et les indicateurs](constants--enumerations--and-flags.md) du système de propriétés Windows.

-   [Exemples de code du système de propriétés](property-system-code-samples.md)

    décrit des exemples qui montrent comment utiliser le système de propriétés Windows.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la réutilisation du magasin de propriétés In-Memory, consultez [initialisation des gestionnaires de propriétés](building-property-handlers-property-handlers.md) et [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Pour obtenir une spécification du format de fichier binaire de la Banque de propriétés Microsoft, consultez [ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   la relation entre les Windows la recherche et l’indexation, et la façon d’étendre l’index, sont expliquées dans les rubriques suivantes de Windows Search :
    -   [développement de gestionnaires de filtres pour la recherche de Windows](../search/-search-ifilter-conceptual.md)
    -   [développement de gestionnaires de protocole pour la recherche de Windows](../search/-search-3x-wds-phaddins.md)
    -   [développement de gestionnaires de propriétés pour la recherche de Windows](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   pour le téléchargement du kit de développement logiciel (SDK) Windows 7 ou mis à jour Windows Vista, consultez le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Guide du développeur de système de propriétés](property-system-developer-s-guide.md)
</dt> <dt>

[Référence du système de propriétés](property-system-reference.md)
</dt> <dt>

[Exemples de code du système de propriétés](property-system-code-samples.md)
</dt> </dl>

 

 
