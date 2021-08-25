---
title: Windows Desktop Search 2. x
description: comprendre Windows Desktop Search 2. x. pour les versions de Windows ultérieures à Windows XP et Windows Server 2003, utilisez Windows Search à la place.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3298d668266d913a427c74f605435257c1a4cfba56fae82c809bd9127e7ecf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829099"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

l’utilisation de et du développement pour les versions 2. x de Microsoft Windows Desktop Search (WDS) est fortement déconseillée en faveur de la [recherche Windows](../search/-search-3x-wds-overview.md).

WDS est un service d’indexation et une plate-forme qui permet de rechercher rapidement des fichiers et des données dans différents emplacements et sources de données. WDS aide les utilisateurs et les autres applications à trouver pratiquement n’importe quel contenu sur leurs ordinateurs, messages électroniques, rendez-vous de calendrier, photos, documents, etc. en outre, WDS peut retourner des résultats de plusieurs sources de données dans un environnement Windows Explorer afin que vos utilisateurs puissent rapidement afficher un aperçu, filtrer et agir sur les résultats de la recherche.

WDS indexe les données d’une étendue d’analyse donnée, les emplacements spécifiés au sein d’un ordinateur local et d’un réseau partagé que l’indexeur doit analyser. Cette étendue d’analyse peut être contrôlée par des options définies par l’utilisateur, des API de gestion et des stratégies de groupe, que les administrateurs réseau peuvent configurer pour contrôler les autorisations d’accès utilisateur et les paramètres d’indexation. Les stratégies de groupe peuvent limiter l’accès à certaines ressources réseau et définir des ressources à indexer.

Cette section contient les rubriques suivantes :

-   [Vue d'ensemble](#windows-desktop-search-2x)
    -   [À propos de l’indexeur WDS](#about-the-wds-indexer)
    -   [À propos du catalogue WDS](#about-the-wds-catalog)
    -   [À propos du moteur de recherche et des résultats](#about-the-search-engine-and-results)
-   [Développement avec WDS](#developing-with-wds)
    -   [Ajout de données à l’index à l’aide de compléments](#adding-data-to-the-index-with-add-ins)
    -   [Interrogation de l’index](#querying-the-index)
-   [Exigences de compatibilité](#compatibility-requirements)
    -   [Configuration requise](#system-requirements)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

### <a name="about-the-wds-indexer"></a>À propos de l’indexeur WDS

lors de la première installation, l’indexeur analyse les fichiers les plus courants de l’utilisateur dans le dossier mes Documents, microsoft Outlook et microsoft Outlook dossiers de messagerie Express et les emplacements spécifiés dans stratégie de groupe. Les utilisateurs peuvent également spécifier de nouveaux fichiers et emplacements à inclure (ou exclure) par l’indexeur dans des analyses successives. Chaque emplacement inclus est identifié par une URL, et l’indexeur commence à cette URL et itère de manière récursive tous les sous-dossiers ou emplacements jusqu’à ce que tous les éléments aient été indexés. Une étendue est un ensemble d’URL. Les API de gestion peuvent être utilisées par les applications personnalisées pour définir leur étendue d’analyse, un ensemble d’URL pointant vers les chemins d’accès au sein d’un protocole, par exemple `file://` pour les dossiers sur un lecteur ou `mapi:// ` pour les magasins de courrier électronique MAPI comme Outlook. WDS utilise des gestionnaires de protocole pour accéder aux magasins de données et aux filtres pour analyser et indexer le texte et les propriétés des éléments. Ces données sont ensuite stockées dans le catalogue.

### <a name="about-the-wds-catalog"></a>À propos du catalogue WDS

Le catalogue WDS est un index du texte et des propriétés collectées à partir d’éléments dans la messagerie spécifiée, les lecteurs locaux, les ressources réseau et d’autres banques de données locales. Le contenu du catalogue est basé sur les options et les règles définies par WDS, les applications basées sur la plateforme WDS, les préférences utilisateur et les stratégies de groupe. Il existe plus de 200 propriétés disponibles pour chaque élément indexé, telles que la date de création, la taille et les propriétés spécifiques au type (« de » pour les messages électroniques). Pour obtenir la liste de ces propriétés, consultez les informations de référence sur les [schémas](-search-2x-wds-schematable.md)WDS.

### <a name="about-the-search-engine-and-results"></a>À propos du moteur de recherche et des résultats

à partir de la barre de recherche WDS ou de Windows Explorer, les utilisateurs peuvent rechercher le contenu de texte intégral et les métadonnées de propriété des éléments indexés. Les mêmes types de recherche peuvent également être lancés à partir de la ligne de commande, d’une page Web ou d’une application personnalisée. le moteur de recherche WDS localise les éléments correspondant aux critères de recherche et les retourne sous la forme de jeux de résultats Microsoft ActiveX Data Objects (ADO). WDS affiche les éléments correspondant aux critères de recherche et peut présenter un aperçu complet de l’élément. Vous pouvez créer des applications pour intercepter la requête de recherche, effectuer la recherche et/ou afficher le jeu de résultats.

## <a name="developing-with-wds"></a>Développement avec WDS

Il existe deux principaux types d’intégration avec WDS : l’ajout de données à l’index et l’interrogation du contenu de l’index pour récupérer les enregistrements correspondant à des critères de recherche.

### <a name="adding-data-to-the-index-with-add-ins"></a>Ajout de données à l’index avec Add-Ins

Il existe essentiellement deux types de sources de données : les magasins du système de fichiers et les magasins de systèmes non-fichiers. Un groupe de fichiers dans mes documents est un magasin de système de fichiers simple. WDS peut rechercher des informations dans les fichiers stockés dans un système de fichiers de ce type s’il peut localiser un filtre pour le type de fichier. Vous pouvez autoriser WDS à indexer un nouveau type de fichier propriétaire si vous fournissez une implémentation de l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour ce type de fichier.

Un magasin de système non-fichier, comme une base de données, requiert un gestionnaire de protocole pour permettre à WDS de naviguer et d’indexer les données dans le magasin de données. par exemple, si vous avez un client de messagerie qui stocke sa liste de messages reçus dans son propre fichier (par exemple, des fichiers PST dans Outlook), vous pouvez fournir un gestionnaire de protocole pour indexer et rechercher chaque e-mail en fournissant un gestionnaire de protocole. Si le magasin de données est hiérarchique, vous devez également implémenter une interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour énumérer les éléments dans le magasin. Pour une meilleure expérience utilisateur, vous pouvez implémenter une extension de Shell pour fournir des menus contextuels et des icônes à partir de l’affichage des résultats.

Actuellement, WDS contient des filtres pour plus de 200 types d’éléments (y compris des éléments en texte brut tels que HTML, XML et des fichiers de code source) et utilise la même technologie [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)et le même gestionnaire de protocole que SharePoint Services. Si vous avez déjà installé des filtres pour les types de fichiers propriétaires, WDS peut utiliser les interfaces de filtre existantes pour indexer ces données.

### <a name="querying-the-index"></a>Interrogation de l’index

WDS fournit des applications avec des jeux de résultats personnalisés de données à partir de l’index en fonction des valeurs de schéma disponibles. Les résultats sont retournés sous forme de jeux d’enregistrements ADO. Il existe quatre façons d’incorporer des requêtes WDS dans une application, chacune offrant différents niveaux de personnalisation et de robustesse.

-   interface ISearchDesktop : les api dans cette interface sont utilisées pour appeler WDS par programmation en spécifiant une chaîne de requête, une liste de colonnes à retourner, des restrictions de portée similaires à une clause de langage SQL (SQL) where et le nom de la colonne à trier. Ces API sont disponibles pour le code natif et managé.
-   contrôle de ActiveX wds : ce contrôle dessine l’interface de recherche wds et gère la recherche et l’affichage des résultats. Cette méthode est plus simple que d’utiliser les API, mais elle est moins flexible. pour utiliser ce contrôle dans une application Microsoft Visual Studio, accédez à la boîte de dialogue **choisir des éléments de boîte à outils** dans le menu **outils** et ajoutez « Windows Desktop Search-visionneuse des résultats » à la **boîte à outils** à partir de l’onglet **composants COM** . Ajoutez ensuite le contrôle au formulaire sur lequel vous souhaitez l’inclure. le contrôle de ActiveX wds est compatible avec wds 2. x et 3. x sur Windows XP uniquement.
-   Paramètres de ligne de commande : les applications peuvent appeler l’exécutable WDS avec différents paramètres pour rechercher et afficher les résultats. Une fenêtre WDS s’ouvre et les résultats s’affichent. Il s’agit du moyen le plus simple d’ajouter une recherche à une application, mais ne retourne pas à l’application appelante des informations sur ce que fait l’utilisateur dans la fenêtre WDS.
-   Objet d’assistance du navigateur WDS (BHO) : de même, les pages Web peuvent utiliser le BHO pour envoyer des requêtes à WDS ou à l’application de recherche inscrite. Après la validation de l’URL de pages Web par rapport à la liste sécurisée de domaine WDS, WDS exécute la requête et affiche les résultats à l’aide de l’interface de recherche standard, ou transmet la requête à l’application de recherche inscrite.

Les utilisateurs peuvent utiliser la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md) pour interroger le catalogue de façon plus puissante en contrôlant l’étendue des recherches et en combinant des paramètres de recherche avec des opérateurs booléens. Par exemple, un utilisateur peut rechercher une pièce jointe dans un e-mail de John qui comprend soit « planification de projet », soit « plan de projet » avec une requête semblable à la suivante : `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Exigences de compatibilité

WDS 2.6.5 est disponible pour les Windows 2000, Windows Server 2003 et Windows XP uniquement. WDS est un téléchargement distinct disponible gratuitement auprès de Microsoft pour une utilisation personnelle et professionnelle. Il doit être installé et utilisé pour l’indexation du compte d’utilisateur avant que les applications générées pour WDS 2.6.5 ne fonctionnent.

### <a name="system-requirements"></a>Configuration requise

les éléments suivants sont requis pour utiliser Windows Desktop Search :

-   Windows Internet Explorer ou version ultérieure.
-   pour inclure vos messages électroniques dans le catalogue, vous devez avoir microsoft microsoft Outlook 2000 ou une version ultérieure, ou bien microsoft Outlook Express 6,0 ou version ultérieure.
-   la version préliminaire complète des documents Microsoft Microsoft Office dans l’affichage des résultats requiert Office XP ou version ultérieure.
-   Processeur Pentium 500 MHz minimum (1 GHz recommandé).
-   Windows XP, Windows 2000 SP4 ou version ultérieure, ou Windows Server 2003 Service Pack 1.
-   Minimum 128 Mo de RAM (256 Mo recommandés).
-   500 Mo d’espace libre sur le disque dur recommandé. La taille de votre index dépend de la quantité de contenu que vous avez indexée.
-   résolution d’écran 1024 x 768 recommandée.

## <a name="related-topics"></a>Rubriques connexes

1.  Interrogation de l’index

    -   [Appel de WDS par programmation (via ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Appel de WDS à partir de pages Web](-search-2x-wds-browserhelpobject.md)
    -   [Appel de WDS à partir de la ligne de commande](-search-2x-wds-fromcommandline.md)

2.  [Extension de l’index (vue d’ensemble)](-search-2x-wds-extendingtheindex.md)

    -   [Développement de compléments IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Développement de gestionnaires de protocole](-search-2x-wds-phaddins.md)

3.  Références générales

    -   [Schéma WDS](-search-2x-wds-schematable.md)
    -   [Syntaxe de requête avancée](-search-2x-wds-aqsreference.md)
    -   [Types de WDS perçus](-search-2x-wds-perceivedtype.md)

 

 