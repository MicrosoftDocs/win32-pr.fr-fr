---
description: Windows La recherche est une plateforme de recherche de bureau qui offre des fonctionnalités de recherche instantanée pour la plupart des types de données et types de données courants, et les développeurs tiers peuvent étendre ces fonctionnalités aux nouveaux types de fichiers et types de données.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Vue d’ensemble de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313258"
---
# <a name="windows-search-overview"></a>Vue d’ensemble de Windows Search

Windows La recherche est une plateforme de recherche de bureau qui offre des fonctionnalités de recherche instantanée pour la plupart des types de données et types de données courants, et les développeurs tiers peuvent étendre ces fonctionnalités aux nouveaux types de fichiers et types de données.

Cette rubrique est organisée comme suit :

-   [Introduction](#introduction)
    -   [Service Windows Search](#windows-search-service)
    -   [Plateforme de développement](#development-platform)
    -   [Interface utilisateur](#user-interface)
-   [Prérequis techniques](#technical-prerequisites)
    -   [Téléchargement et contenu du SDK](#sdk-download-and-contents)
-   [Windows Rechercher dans la documentation du SDK](#windows-search-sdk-documentation)
-   [historique de la recherche de Windows](#history-of-windows-search)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Windows la recherche est un composant standard de Windows 7 et Windows Vista, et est activée par défaut. Windows la recherche remplace Windows Desktop search (WDS), qui était disponible en tant que complément pour Windows XP et Windows Server 2003.

Windows La recherche est composée de trois composants :

-   [Search Service Windows](#windows-search-service) (WSS)
-   [Plateforme de développement](#development-platform)
-   [Interface utilisateur](#user-interface)

### <a name="windows-search-service"></a>Service Windows Search

le WSS organise les fonctionnalités extraites d’une collection de documents. le protocole de recherche Windows permet à un client de communiquer avec un serveur qui héberge un WSS, à la fois pour émettre des requêtes et pour permettre à un administrateur de gérer le serveur d’indexation. lors du traitement de fichiers, WSS analyse un ensemble de documents, extrait des informations utiles, puis organise les informations extraites afin que les propriétés de ces documents puissent être retournées efficacement en réponse aux requêtes.

une collection de documents qui peuvent être interrogés comprend un catalogue, qui est l’unité de niveau le plus élevé de l’organisation dans Windows recherche. Un catalogue représente un ensemble de documents indexés qui peuvent être interrogés. Un catalogue se compose d’une table de propriétés avec le texte ou la valeur et l’emplacement (paramètres régionaux) correspondant stockés dans les colonnes de la table. Chaque ligne de la table correspond à un document distinct dans l’étendue du catalogue, et chaque colonne de la table correspond à une propriété. Un catalogue peut contenir un index inversé (pour la correspondance de mot rapide) et un cache de propriétés (pour une récupération rapide des valeurs de propriété).

le processus de l’indexeur est implémenté en tant que service Windows s’exécutant dans le compte LocalSystem et est toujours en cours d’exécution pour tous les utilisateurs (même si aucun utilisateur n’est connecté), ce qui permet à Windows recherche d’effectuer les opérations suivantes :

-   Conserver un index partagé entre tous les utilisateurs.
-   Maintien des restrictions de sécurité sur l’accès au contenu.
-   Traitez les requêtes distantes à partir d’ordinateurs clients sur le réseau.

Le service de recherche est conçu pour protéger l’expérience utilisateur et les performances système lors de l’indexation. Les conditions suivantes entraînent le basculement du service ou la suspension de l’indexation :

-   Utilisation élevée du processeur par des processus qui ne sont pas liés à la recherche.
-   Taux d’e/s du système élevé, y compris les lectures et écritures de fichiers, les e/s de fichier d’échange et de cache de fichiers, ainsi que les e/s de fichier mappées.
-   Faible disponibilité de la mémoire.
-   Faible durée de vie de la batterie.
-   Espace disque faible sur le lecteur qui stocke l’index.

### <a name="development-platform"></a>Plateforme de développement

la meilleure façon d’accéder aux api de recherche et de créer des applications de recherche Windows se fait via une source de données Shell. Une source de données Shell est un composant qui est utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données. Un magasin de données est un référentiel de données. Un magasin de données peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur qui utilise une source de données Shell. les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.

Par exemple, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) est un composant qui peut créer des instances de la source de données du dossier de recherche, qui est un type de source de données « virtuelles » fourni par le shell qui peut exécuter des requêtes sur d’autres sources de données dans l’espace de noms Shell et énumérer les résultats. Pour ce faire, il peut utiliser l’indexeur ou l’énumération et l’inspection manuelle des éléments dans les étendues spécifiées. Cette interface vous permet de configurer les paramètres de la recherche à l’aide de méthodes qui créent et modifient des dossiers de recherche. Si les méthodes de cette interface ne sont pas appelées, les valeurs par défaut sont utilisées à la place.

il est préférable d’accéder indirectement à la fonctionnalité de recherche de Windows via le modèle de données shell, car elle permet d’accéder aux fonctionnalités complètes de l’interpréteur de commandes au niveau du modèle de données shell. par exemple, vous pouvez définir l’étendue d’une recherche sur une bibliothèque (fonctionnalité disponible dans Windows 7 et versions ultérieures) pour utiliser les dossiers de bibliothèque comme étendue de la requête. Windows La recherche regroupe ensuite les résultats de la recherche à partir de ces emplacements, s’ils se trouvent dans des index différents (si les dossiers se trouvent sur des ordinateurs différents). La couche de données de Shell crée également une vue plus complète des propriétés des éléments, en synthétisant certaines valeurs de propriété. il fournit également un accès aux fonctionnalités de recherche pour les magasins de données qui ne sont pas indexés par Windows recherche. Par exemple, vous pouvez rechercher un périphérique de stockage USB (Universal Serial Bus), un appareil portable qui utilise le protocole MTP ou un serveur protocole FTP (FTP) via les sources de données de l’interpréteur de commandes qui permettent d’accéder à ces systèmes de stockage. Cela garantit une meilleure expérience utilisateur.

Windows la recherche a un cache de valeurs de propriété qui est utilisé dans l’implémentation du Search Service Windows (WSS). ces valeurs de propriété peuvent être interrogées par programme à l’aide du fournisseur de OLE DB de recherche Windows, ou via [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), qui représente des éléments dans les résultats de recherche et les vues basées sur des requêtes. Windows La recherche collecte et stocke ensuite les propriétés émises par les gestionnaires de filtres ou les gestionnaires de propriétés lorsqu’un élément, tel qu’un document Word, est indexé. Ce magasin est supprimé et reconstruit lors de la reconstruction de l’index.

les développeurs tiers peuvent créer des applications qui consomment les données de l’index par le biais de requêtes de programmation et peuvent étendre les données dans l’index pour les types de fichiers et d’éléments personnalisés à indexer par Windows recherche. si vous souhaitez afficher les résultats de la requête dans l’explorateur de Windows, vous devez implémenter une source de données Shell avant de pouvoir créer un gestionnaire de protocole pour étendre l’index. Toutefois, si toutes les requêtes sont par programmation (par exemple OLE DB) et interprétées par le code de l’application plutôt que par le shell, un espace de noms Shell est toujours préféré, mais pas obligatoire.

un gestionnaire de protocole est requis pour Windows pour obtenir des informations sur le contenu des fichiers, tels que des éléments dans les bases de données ou des types de fichiers personnalisés. si Windows recherche peut indexer le nom et les propriétés du fichier, Windows n’a pas d’informations sur le contenu du fichier. par conséquent, ces éléments ne peuvent pas être indexés ou exposés dans le Shell Windows. En implémentant un gestionnaire de protocole personnalisé, vous pouvez exposer ces éléments. pour obtenir la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, consultez « vue d’ensemble des gestionnaires » dans [Windows la recherche en tant que plateforme de développement](-search-3x-wds-development-ovr.md).

> [!Note]  
> Une source de données Shell est parfois appelée extension d’espace de noms Shell. Un gestionnaire est parfois appelé extension d’interpréteur de commandes ou gestionnaire d’extensions de Shell.

 

### <a name="user-interface"></a>Interface utilisateur

dans Windows Vista et versions ultérieures, Windows recherche est intégrée à toutes les fenêtres de l’explorateur de Windows pour un accès instantané à la recherche. Cela permet aux utilisateurs de rechercher rapidement des fichiers et des éléments par leur nom de fichier, leurs propriétés et leur contenu de texte intégral. Les résultats peuvent également être filtrés plus en détail pour affiner la recherche. voici d’autres fonctionnalités de Windows Search :

-   Une zone de recherche instantanée dans chaque fenêtre active le filtrage instantané de tous les éléments actuellement en vue. les zones de recherche instantanée s’affichent dans la menu Démarrer pour rechercher des programmes ou des fichiers, et dans le coin supérieur droit de toutes les fenêtres de l’explorateur de Windows pour filtrer les résultats affichés. la recherche instantanée est également intégrée à d’autres fonctionnalités de Windows, telles que Lecteur Windows Media, pour rechercher des fichiers associés.
-   Les documents peuvent être balisés avec des mots clés pour les regrouper selon des critères personnalisés définis par l’utilisateur. Les balises sont des éléments de métadonnées qui sont assignés par l’utilisateur ou les applications pour faciliter la recherche de fichiers en fonction de mots clés qui ne se trouvent peut-être pas dans le nom ou le contenu de l’élément. Par exemple, un ensemble d’images peut être marqué comme « Arizona vacances 2009 » pour récupérer rapidement par la suite en recherchant l’un des mots inclus.
-   les en-têtes de colonnes améliorés dans les vues de Windows Explorer permettent de trier et de regrouper des documents de différentes façons. Par exemple, les fichiers peuvent être triés en fonction du nom, de la date de modification, du type, de la taille et des balises. Les documents peuvent également être regroupés en fonction de l’une de ces propriétés, et chaque groupe peut être filtré (masqué ou affiché) comme vous le souhaitez.
-   Les documents peuvent être empilés en fonction du nom, de la date de modification, du type, de la taille et des balises. Les piles incluent tous les documents qui ont la propriété spécifiée et qui se trouvent dans un sous-dossier du dossier sélectionné.
-   les recherches peuvent être enregistrées (pour être récupérées ultérieurement) en cliquant sur le bouton **enregistrer la recherche** dans le volet de recherche de l’explorateur de Windows. Les résultats seront repeuplés de manière dynamique en fonction des critères d’origine lors de l’ouverture de la recherche enregistrée. Pour obtenir des instructions, consultez [enregistrer les résultats de votre recherche](https://windows.microsoft.com/windows-vista/Save-your-search-results).
-   les gestionnaires d’aperçus et les gestionnaires de miniatures permettent aux utilisateurs d’afficher un aperçu des documents dans Windows Explorer sans avoir à ouvrir l’application qui les a créés.

## <a name="technical-prerequisites"></a>Prérequis techniques

avant de commencer à lire la documentation du kit de développement logiciel (SDK) Windows Search, vous devez comprendre les concepts suivants :

-   Comment implémenter une source de données Shell.
-   Comment implémenter un gestionnaire.
-   Comment travailler en code natif.

Une source de données Shell est un composant qui est utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données. Dans le passé, la source de données Shell était appelée extension d’espace de noms Shell. Un gestionnaire est un objet COM (Component Object Model) qui fournit les fonctionnalités d’un élément de Shell. pour obtenir la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, consultez « vue d’ensemble des gestionnaires » dans [Windows la recherche en tant que plateforme de développement](-search-3x-wds-development-ovr.md).

pour plus d’informations sur l’assembly d’interopérabilité du kit de développement logiciel (SDK) de recherche Windows pour travailler avec des objets COM exposés par Windows recherche et d’autres programmes qui utilisent du code managé, consultez [utilisation de code managé avec des données de Shell et recherche de Windows](-search-3x-wds-managed-code.md). Toutefois, Notez que les filtres, les gestionnaires de propriétés et les gestionnaires de protocole doivent être écrits en code natif. Cela est dû à des problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent. les développeurs qui découvrent C++ peuvent commencer à utiliser le [centre](https://msdn.microsoft.com/vstudio//default.aspx) de développement Visual C++ et les [Prise en main de développement Windows](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Téléchargement et contenu du SDK

en plus de respecter les conditions techniques mentionnées, vous devez également télécharger le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour obtenir les bibliothèques de recherche Windows. les [exemples du kit de développement logiciel (SDK) de recherche Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contiennent des exemples de code utiles et un assembly d’interopérabilité pour le développement avec du code managé. pour plus d’informations sur l’utilisation des exemples de code, consultez [Windows des exemples de code de recherche](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Windows Rechercher dans la documentation du SDK

le contenu de la documentation du kit de développement logiciel Windows Search est le suivant :

-   [Windows Search en tant que plateforme de développement](-search-3x-wds-development-ovr.md)

    décrit les principaux scénarios de développement dans Windows recherche. Fournit la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, des instructions du programme d’installation de compléments et des remarques d’implémentation.

-   [Windows Rechercher dans le Guide du développeur](-search-developers-guide-entry-page.md)

    Fournit des explications pour [la gestion de l’index](-search-3x-wds-mngidx-overview.md), l' [interrogation de l’index par programmation](-search-3x-wds-qryidx-overview.md), [l’extension de l’index et l'](-search-3x-wds-extidx-overview.md) [extension des ressources de langue](extending-language-resources-in-windows-search.md).

-   [Windows Référence de recherche](-search-reference-entry-page.md)

    documente les catégories suivantes d’Windows interfaces de recherche : [gestionnaires de protocole](-search-protocol-handlers-interfaces-entry-page.md), [interrogation](-search-querying-interfaces-entry-page.md), étendue de l' [analyse](-search-crawl-scope-interfaces-entry-page.md), [compléments de données](-search-data-addins-interfaces-entry-page.md), gestion des [Index](-search-index-mgt-interfaces-entry-page.md)et [notifications](-search-notifications-interfaces-entry-page.md). La documentation de référence comprend également des [constantes, des énumérations](-search-constants-and-enumerations-entry-page.md), des [structures](-search-structures-entry-page.md), des [mappages de propriétés](-search-3x-wds-propertymappings.md)et le [format de fichier de recherche enregistré](-search-savedsearchfileformat.md).

-   [Windows Rechercher des exemples de code](-search-samples-ovw.md)

    Décrit les exemples de code d’API de recherche disponibles.

-   [Recherche fédérée dans Windows](-search-federated-search-overview.md)

    décrit la prise en charge de Windows 7 pour la fédération des recherches aux magasins de données distants à l’aide de technologies OpenSearch qui permettent aux utilisateurs d’accéder à leurs données distantes à partir de Windows Explorer et d’interagir avec eux.

-   [Technologies de recherche associées](-search-3x-wds-sampleentry.md)

    répertorie les technologies liées à la recherche Windows : recherche Enterprise, recherche de Enterprise SharePoint et applications héritées telles que Windows Desktop search 2. x et platform SDK : Service d’indexation.

-   [Windows Rechercher dans le Glossaire](search-glossary.md)

    définit les termes essentiels utilisés dans les technologies de recherche et de Shell Windows.

## <a name="history-of-windows-search"></a>historique de la recherche de Windows

Windows la recherche remplace Windows Desktop search (WDS), qui était disponible en tant que complément pour Windows XP et Windows Server 2003. WDS a remplacé le Service d’indexation hérité des versions précédentes de Windows avec des améliorations apportées aux performances, à la convivialité et à l’extensibilité. La nouvelle plateforme de développement prend en charge des exigences qui produisent un système plus sécurisé et plus stable. alors que la nouvelle plateforme de requête n’est pas compatible avec Microsoft Windows Desktop Search (WDS) 2. x, les filtres et les gestionnaires de protocole écrits pour les versions précédentes de WDS peuvent être mis à jour pour fonctionner avec Windows Search. Windows La recherche prend également en charge un nouveau système de propriétés. Pour plus d’informations sur les filtres, les gestionnaires de propriétés et les gestionnaires de protocole, consultez [extension de l’index](-search-3x-wds-extidx-overview.md).

Windows la recherche est intégrée à Windows Vista et versions ultérieures, et est disponible en tant que mise à jour redistribuable de WDS 2. x, pour prendre en charge les systèmes d’exploitation suivants :

-   versions 32 bits de Windows XP avec Service Pack 2 (SP2).
-   toutes les versions x64 de Windows XP.
-   Windows Serveur 2003 avec Service Pack 1 (SP1) et versions ultérieures.
-   toutes les versions x64 de Windows Server 2003.

les systèmes qui exécutent ces systèmes d’exploitation doivent disposer d’Windows recherche installée afin d’exécuter des applications écrites pour la recherche Windows. pour plus d’informations, consultez [l’article 917013 de la base de connaissances : Description de Windows desktop search 3,01 et le Pack d’interface utilisateur multilingue pour Windows desktop search 3,01](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions//bb776815(v=vs.85)).
-   Pour plus d’informations sur [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) et la source de données du dossier de base de données, consultez la description de la \_ constante d’analyse Str \_ avec des \_ Propriétés dans les [clés de chaîne de contexte de liaison](../shell/str-constants.md). Voir aussi [tableaux d’association](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) et [IPropertySystem :: GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019)de la programmation. pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez la documentation de l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   pour obtenir une vue d’ensemble des gestionnaires de type de fichier (également appelés gestionnaires d’extension de Shell et gestionnaires de recherche), consultez [Windows la recherche en tant que plateforme de développement](-search-3x-wds-development-ovr.md).
-   pour les tableaux de messages pris en charge par la communauté sur les technologies de recherche, consultez le [Forum MSDN : Windows Desktop search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   pour obtenir des exemples de code associés, consultez [Windows des exemples de code de recherche](-search-samples-ovw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Search en tant que plateforme de développement](-search-3x-wds-development-ovr.md)
</dt> <dt>

[langues prises en charge par la recherche de Windows](-search-3x-wds-language-support.md)
</dt> <dt>

[Utilisation de code managé avec Shell Data et Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
