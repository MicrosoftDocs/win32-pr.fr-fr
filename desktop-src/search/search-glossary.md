---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Windows Rechercher dans le Glossaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efe8bbe07badc7575cc3aba83100814d601bc5c8ebca24961b198950b2e5e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844649"
---
# <a name="windows-search-glossary"></a>Windows Rechercher dans le Glossaire

## <a name=""></a>\#

**fichier. OSD**

OpenSearch Fichier de descripteur.

**fichier. fichier osdx**

fichier XML de description OpenSearch qui décrit les connexions de serveur et les formats de résultats disponibles pour une source de données web spécifique. elle est utilisée pour interagir avec le Shell Windows. voir aussi : descripteur de OpenSearch.

## <a name="a"></a>A

**Syntaxe de requête avancée (AQS)**

la syntaxe de requête par défaut utilisée par Windows recherche pour interroger l’index et affiner et limiter les paramètres de recherche. AQS est principalement orienté utilisateur et peut être utilisé par les utilisateurs pour créer des requêtes AQS, mais il peut également être utilisé par programme. Voir aussi : syntaxe de requête naturelle (NQS).

**AQS**

Consultez la définition de : syntaxe de requête avancée (AQS).

**Association**

Mappage d’une extension de nom de fichier (par exemple, .mp3) ou protocole (par exemple, http) à un identificateur programmatique (ProgID). Ce mappage est stocké dans le Registre sous la forme d’un paramètre par utilisateur avec une solution de secours pour chaque ordinateur. Les applications qui participent au système de programmes par défaut définissent le mappage d’association pour l’extension de nom de fichier ou le protocole de manière à pointer vers les clés ProgID dont ils sont propriétaires.

**Tableau d’association**

Liste ordonnée d’emplacements du Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type. par exemple, un fichier de .jpg a le tableau d’association suivant sur un système de Windows par défaut : « hkcr \\ jpgfile », « hkcr \\ SystemFileAssociations \\.jpg », « hkcr \\ SystemFileAssociations \\ image », « hkcr \\ \* », « hkcr \\ AllFileSystemObjects ».

**Atom**

Schéma XML utilisé pour les flux Web et la distribution de contenu, développé comme alternative à RSS (Really Simple Syndication). Le format de syndication Atom a été publié en tant que norme proposée par l’IETF dans le document RFC 4287.

## <a name="b"></a>B

**bind**

Pour charger ou associer du code à des données. Par exemple, un gestionnaire peut être associé à une source de données Shell.

**liant**

Requête dans une requête de recherche pour une colonne dans un ensemble de lignes retourné. La liaison spécifie une propriété à inclure dans les résultats de la recherche.

**bookmark**

Indicateur qui identifie de façon unique une ligne dans un ensemble de lignes.

## <a name="c"></a>C

**nom canonique**

Nom unique d’une ressource. Canonique signifie « selon les règles ». Voir aussi : nom de verbe canonique.

**nom de verbe canonique**

Nom indépendant du langage qui peut être utilisé par programme pour faire référence à un verbe, quelle que soit la chaîne localisée dans l’interface utilisateur. Voir aussi : nom canonique, verbe.

**catalog**

unité de niveau le plus élevé de l’organisation dans Windows recherche. Un catalogue représente un ensemble de documents indexés qui peuvent être interrogés. Un catalogue se compose d’une table de propriétés avec le texte ou la valeur et l’emplacement correspondant stocké dans les colonnes de la table. Chaque ligne de la table correspond à un document distinct dans l’étendue du catalogue, et chaque colonne de la table correspond à une propriété. voir aussi : index, service de recherche de Windows.

**category**

Regroupement hiérarchique de lignes. Par exemple, un résultat de requête qui contient des colonnes d’auteur et de titre peut être classé en fonction de l’auteur. Dans cet exemple, chaque groupe de lignes qui contient la même valeur pour Author constitue une catégorie.

**chapitre**

Collection de lignes au sein d’un ensemble de lignes. Voir aussi : catalogue, catégorie.

**column**

Conteneur pour un seul type d’informations dans une ligne. Les colonnes sont mappées à des noms de propriété et spécifient les propriétés qui sont utilisées pour les éléments de l’arborescence de commandes de la requête de recherche. Voir aussi : catégorie.

**arborescence de commandes**

Combinaison de restrictions, catégories et ordres de tri spécifiés pour la requête de recherche. Voir aussi : catégorie.

**container**

Type d’élément de Shell qui peut contenir d’autres éléments. Les éléments d’un conteneur sont exposés à l’espace de noms Shell à l’aide d’une source de données Shell. Les exemples incluent les dossiers, les lecteurs, les serveurs réseau et les fichiers compressés avec une extension de nom de fichier .zip. Voir aussi : source de données Shell, dossier, élément Shell.

**content**

Texte et propriétés associés à un élément de Shell ou à une source de contenu qui peut être indexée.

**source du contenu**

Élément auquel l’indexeur peut accéder. Les sources de contenu sont adressables par une URL et sont fournies à l’indexeur par un gestionnaire de protocole. voici quelques exemples : fichiers et dossiers du système de fichiers, éléments et dossiers de microsoft Outlook, enregistrements de base de données et éléments stockés dans microsoft SharePoint. Une source de contenu peut être exposée en tant qu’élément de Shell en implémentant une source de données Shell. Voir aussi : contenu, élément de Shell.

**content view (affichage du contenu)**

vue dans Windows Explorer (proposée dans Windows 7 et versions ultérieures) qui affiche le contenu le plus pertinent pour chaque élément de la liste en fonction de son extension de nom de fichier ou de son association de type. L’affichage du contenu utilise une logique de redimensionnement qui supprime des propriétés lorsque la taille de la fenêtre diminue pour s’assurer que les propriétés les plus critiques disposent toujours de suffisamment de place pour être clairement lisibles. Voir aussi : modèle de disposition, genre, Association de genres.

**mode d’affichage du contenu**

Consultez la définition de : vue de contenu.

**menu contextuel**

Ce terme est parfois utilisé pour signifier le menu contextuel. Consultez la définition de : menu contextuel.

**Gestionnaire de menu contextuel**

Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel. Consultez la définition de : gestionnaire de menu contextuel.

**analyse**

Pour itérer au sein d’une étendue d’analyse, en identifiant les sources de contenu qui requièrent l’indexation ou la réindexation.

**étendue de l’analyse**

Collection de magasins de données (identifiables par URL) qui représente le contenu que l’indexeur analyse et indexe.

**cursor**

Dans le contexte de l’index local, un curseur est un indicateur qui permet de travailler avec une ligne ou un petit bloc de lignes à la fois dans un jeu de données retourné dans un jeu de résultats. Une fois que le curseur est positionné sur une ligne, les opérations peuvent être effectuées sur cette ligne ou sur un bloc de lignes à partir de cette position.

## <a name="d"></a>D

**Gestion des données, exploration et exploration de données**

Consultez la définition de : Database Mining Extensions (DMX).

**gestionnaire d’objets de données**

Gestionnaire qui fournit des formats de presse-papiers supplémentaires pour l’objet de données (IDataObject) d’un élément. Les objets de données sont utilisés dans les scénarios de glisser-déplacer et de copier/coller.

**source de données**

Ce terme est parfois utilisé pour signifier le magasin de données ou la source de données Shell. Consultez la définition de : magasin de données, source de données Shell.

**magasin de données**

Référentiel de données. Un magasin de données peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur à l’aide d’une source de données Shell. les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.

**DMX (Database Mining Extensions)**

Langage de requête utilisé pour créer et manipuler l’exploration de données. les modèles d’administration pour Windows 7, Windows Search et Windows Explorer sont des fichiers. admx et s’appuient sur la technologie DMX. Les modèles suivants peuvent être personnalisés à l’aide de stratégie de groupe : Search. admx, Explorer. admx et WindowsExplorer. admx.

**DMR**

Consultez la définition de : extensions d’exploration de données.

**document**

Élément de Shell qui contient du texte et pour lequel l’interface IFilter peut être implémentée.

**supprimer le gestionnaire**

Gestionnaire qui permet à un type d’élément particulier de prendre en charge les scénarios de glisser-déplacer et de copier/coller.

**déplacer la cible**

Objet de données qui est glissé et déposé dans un fichier. Voir aussi : gestionnaire de données, Drop handler.

**verbe dynamique**

Verbe qui dépend de l’état d’un élément de Shell ou du système ; l’apparence de l’élément est basée sur l’État et requiert que le code en cours d’exécution détermine si l’élément doit apparaître. Voir aussi : gestionnaire de menu contextuel, verbe statique, verbe.

## <a name="e"></a>E

**Commande Explorer**

objet qui peut être présenté sous la forme d’un bouton près du haut de la fenêtre de l’explorateur de Windows qui fournit des fonctionnalités pour les éléments et les conteneurs de cette fenêtre. une source de données Shell fournit les objets de commande Windows Explorer pour un élément de conteneur particulier. Les commandes sont parfois utilisées comme verbes.

## <a name="f"></a>F

**recherche fédérée**

modèle d’extensibilité qui permet de rechercher des magasins de données et de représenter les résultats en tant qu’éléments de Shell dans Windows Explorer. voir aussi : fournisseur de recherche fédéré, connecteur de recherche, OpenSearch descripteur OpenSearch standard.

**connecteur de recherche fédérée**

Consultez la définition de : connecteur de recherche.

**moteur de recherche fédéré**

service web, implémenté par un magasin de données, qui prend en charge les protocoles utilisés par Windows 7 afin que Windows 7 et versions ultérieures puissent effectuer une recherche à distance dans le magasin de données. voir aussi : deOpenSearch descripteur, OpenSearch standard.

**Association de fichiers**

Consultez la définition de : Association de types de fichiers.

**format de fichier**

Format des données stockées dans un fichier dont la spécification de format est documentée. Les exemples incluent OLE DocFile, OPC, XML, ZIP et d’autres spécifications de format de fichier connues. Les créateurs de type de fichier utilisent généralement un format de fichier existant comme base d’un nouveau type de fichier. Un format de fichier peut être simplement une définition qui n’est pas instanciée en tant que type de fichier.

**Gestionnaire de format de fichier**

Ce terme est un synonyme du gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

**extension de nom de fichier**

Consultez la définition de : extension de nom de fichier.

**extension de nom de fichier**

Indicateur principal d’un type de fichier pour les éléments du système de fichiers. il s’agit de la partie du nom de fichier qui suit le point final. L’extension de nom de fichier ne peut pas contenir d’espaces ou de caractères non ASCII et s’applique uniquement aux fichiers (et non aux dossiers). Les extensions de nom de fichier sont comparées à l’aide d’une fonction de comparaison qui ne respecte pas la casse ou les paramètres régionaux. Voir aussi : format de fichier, type de fichier.

**type de fichier**

Une valeur d’extension de nom de fichier particulière, telle que « .htm » ou « .jpg », définit une classe de fichiers qui sont du même type et qui ont un ensemble commun d’associations. Voir aussi : genre, Association de type de fichier.

**association de types de fichier**

Pour une extension de nom de fichier particulière, les éléments de tableau d’association qui définissent où les gestionnaires et d’autres attributs peuvent être inscrits. Voir aussi : tableau d’association, type de fichier.

**personnalisation du type de fichier**

Association qui permet à Shell de personnaliser la manière dont l’interpréteur de commandes traite un type de fichier. Les personnalisations de type de fichier incluent la spécification de l’application utilisée pour ouvrir le fichier lorsque vous double-cliquez dessus, l’ajout de commandes au menu contextuel pour un type de fichier, la spécification d’une icône personnalisée, la spécification d’un type de contenu MIME à associer à un type de fichier, la spécification d’un type perçu et la spécification d’une ou plusieurs applications associées à un type Voir aussi : PerceivedType.

**Gestionnaire de type de fichier**

Gestionnaire inscrit pour un type de fichier. Voir aussi : handler.

**filter**

Implémentation de l’interface IFilter. Il ouvre les fichiers d’un type de fichier particulier et filtre les propriétés et les blocs de texte de l’indexeur. Les filtres sont associés à des types de fichiers, tels qu’ils sont signalés par des extensions de nom de fichier, des types MIME ou des identificateurs de classe (CLSID). Bien qu’un filtre puisse gérer plusieurs types de fichiers, chaque type de fichier fonctionne avec un seul filtre.

**Répertoire**

Consultez la définition de : Container.

## <a name="h"></a>H

**gestionnaire**

Objet COM qui fournit les fonctionnalités d’un élément de Shell. La plupart des sources de données Shell offrent un système extensible pour lier les gestionnaires aux éléments. Par exemple, le dossier de système de fichiers utilise le système d’association pour rechercher les gestionnaires pour un type de fichier particulier. Voir aussi : Association de fichier, type de fichier, personnalisation de type de fichier.

## <a name="i"></a>I

**gestionnaire d’icône**

Gestionnaire qui fournit les informations nécessaires pour générer et mettre en cache une icône pour un élément. Le magasin de données du système de fichiers prend en charge le chargement d’un gestionnaire d’icône pour un élément en fonction du type de fichier, ce qui permet à ce gestionnaire de fournir une icône qui est utilisée pour toutes les instances de ce type de fichier.

**index**

n. Catalogue qui stocke le contenu et les propriétés des éléments de l’interpréteur de commandes pour permettre des recherches rapides. Voir aussi : catalogue, indexeur, indexation, index inversé. v. pour accéder aux sources de contenu, filtrez les sources pour le contenu et les propriétés et insérez les valeurs extraites dans l’index (pour le texte) et le magasin de propriétés de recherche Windows (pour les propriétés). Voir aussi : source de contenu, index, indexeur, index inversé.

**indexeur**

Application qui effectue l’indexation ou la coordination de l’indexation. Voir aussi : index, indexation, index inversé.

**gestionnaire d’info-bulle**

Gestionnaire qui fournit le texte contextuel lorsque l’utilisateur place le pointeur de la souris sur un objet d’interface utilisateur.

**index inversé**

structure persistante qui contient le contenu extrait de fichiers en Windows la recherche. Le texte est organisé en un index qui établit une correspondance entre un mot d’une propriété et une liste de documents et d’emplacements dans un document qui contient ce mot. Par conséquent, un index inversé est l’inverse du processus d’extraction du texte et des propriétés du document et de leur insertion dans l’indexeur. Voir aussi : index, indexeur, indexation.

**item**

Consultez la définition de : élément de Shell.

**Item (classe)**

Consultez la définition de : type de fichier.

## <a name="k"></a>K

**Type**

Propriété qui fournit un nom de genre convivial et qui peut être associée à une liste de propriétés et un modèle de disposition. le genre a été introduit dans Windows Vista pour exprimer une notion plus conviviale de type de fichier par l’utilisateur final et il a été défini comme étant une propriété de chaîne à valeurs multiples (valeurs de chaîne canoniques). vous pouvez donc avoir une valeur de type « audio, vidéo » ou « liaison ; document ». Certains noms de genres conviviaux sont déjà associés à des propriétés et des modèles de disposition. Par exemple, les éléments associés au type. Picture et aux éléments associés à Kind.Document affichent des propriétés différentes, même s’ils se trouvent dans la même vue. Chaque genre d’élément peut être associé à l’un des quatre modèles de disposition uniques qui définissent le nombre de propriétés affichées pour chaque élément et leur disposition. Voir aussi : Association de genres, vue de contenu, modèle de disposition.

**Association de genres**

Une propriété dans le système de propriétés, appelée System. Kind, qui détermine les modèles d’expérience utilisateur qui sont affichés pour un fichier. Cette propriété fournit également un nom convivial pour le type de l’élément et est lié à l’extension de nom de fichier. Voir aussi : genre.

## <a name="l"></a>L

**modèle de disposition**

L’un des nombreux mécanismes d’affichage des propriétés. dans Windows 7 et versions ultérieures, lorsque vous inscrivez un nouveau type de fichier, vous pouvez utiliser l’affichage de contenu pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier. Vous pouvez choisir parmi quatre modèles de disposition différents : alpha (pour les résultats de recherche de documents qui contiennent des extraits de code), la version bêta (pour les résultats de recherche par courrier électronique avec extraits de code), gamma (semblable à alpha mais avec une disposition sur deux lignes au lieu de quatre) et Delta Voir aussi : vue de contenu, genre, Association de genres.

## <a name="m"></a>M

**Gestionnaire de métadonnées**

Ce terme est parfois utilisé pour signifier le gestionnaire de propriétés. Consultez la définition de : gestionnaire de propriétés.

## <a name="n"></a>N

**extension de l’espace de noms**

Consultez la définition de : source de données Shell.

**parcours de l’espace de noms**

Processus d’assistance qui parcourt l’espace de noms d’un conteneur ou d’un ensemble de conteneurs, découvre chaque élément et peut effectuer une opération avec chacun. l’interface INamespaceWalk peut être utilisée pour parcourir n’importe quelle partie de l’espace de noms Windows Explorer ou pour découvrir les éléments référencés par un objet de données ou une vue. Les verbes de conteneur (comme « Play » sur les conteneurs Artists) parcourent l’espace de noms et découvrent les éléments.

**requête en langage naturel**

Consultez la définition de : syntaxe de requête naturelle (NQS).

**Syntaxe de requête naturelle (NQS)**

Une syntaxe de requête qui est plus stricte que AQS et ressemble davantage à la langue humaine. NQS peut être utilisé par Windows recherche pour interroger l’index si NQS est sélectionné à la place de la valeur par défaut, AQS. Voir aussi : syntaxe de requête avancée (AQS).

**mot parasite**

mot qui est ignoré par Windows rechercher lorsqu’il est présent dans les restrictions spécifiées pour la requête de recherche, car il a peu de valeur discriminatoire. Exemples : « and » et « The ».

**NQS**

Consultez la définition de : syntaxe de requête naturelle (NQS).

## <a name="o"></a>O

**Base de données de liaison et d’incorporation d’objets (OLE DB)**

Ensemble standard d’interfaces qui fournit un accès hétérogène à des sources disparates d’informations situées n’importe où, comme les systèmes de fichiers, les dossiers de messagerie et les bases de données.

**OLE DB**

Consultez la définition de : liaison objet et incorporation d’une base de données.

**descripteur de OpenSearch**

Fichier XML qui décrit les connexions de serveur et les formats de résultats disponibles pour une source de données Web spécifique. ce fichier contient un ou plusieurs modèles d’URL et utilise une extension de nom de fichier. fichier osdx lors de l’interaction avec le Shell Windows. une description de OpenSearch est parfois appelée connecteur de recherche, bien qu’il s’agisse uniquement de la partie description d’un connecteur. Voir aussi : connecteur de recherche.

**OpenSearch standard**

Collection de formats et de protocoles simples utilisés pour le partage des résultats de recherche. pour plus d’informations, consultez le site web OpenSearch ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Catégorie étendue de types de format de fichier. PerceivedType a été introduit dans Windows XP et prend en charge un ensemble limité de types de fichiers connus (par exemple, les types de fichier Image, texte, Audio et fichiers compressés). Les types de fichiers, généralement les types de fichiers publics, peuvent également avoir un type perçu. Par exemple, les types de fichiers image .bmp, .png, .jpg et .gif sont également du type perçu, image. Au niveau de la couche de programmation, PerceivedType est exprimé sous la forme d’un entier. Étant donné que du code utilise Kind et PerceivedType, les propriétaires de format de fichier doivent inscrire les deux. Par exemple, « lire tout » dépend de PerceivedType. Voir aussi : type de fichier.

**gestionnaire d’aperçus**

gestionnaire qui produit rapidement une vue simplifiée en lecture seule de l’élément de Shell à afficher dans le volet de visualisation de l’explorateur de Windows.

**générateur d’aperçu**

Ce terme est parfois utilisé pour signifier un gestionnaire d’aperçus. Consultez la définition de : gestionnaire d’aperçus.

**Gestionnaire de propriétés**

gestionnaire qui traduit les données stockées dans un fichier dans un schéma structuré qui est reconnu par et qui est accessible par Windows Explorer, Windows Search et d’autres applications. Ces systèmes peuvent ensuite interagir avec le gestionnaire de propriétés pour écrire et lire les propriétés vers et à partir du fichier. Les données traduites comprennent la vue détails, info-bulles, le volet Détails, les pages de propriétés, etc. Chaque gestionnaire de propriétés est associé à un type de fichier particulier, identifié par l’extension de nom de fichier. Voir aussi : système de propriétés.

**Gestionnaire de feuille de propriétés**

Gestionnaire utilisé pour créer des feuilles de propriétés personnalisées avec des images et des contrôles d’interface utilisateur qui autorisent une interaction personnalisée avec un type de fichier.

**système de propriétés**

Système extensible de lecture/écriture de définitions de données qui utilise des propriétés implémentées en tant que paires nom-valeur. Voir aussi : gestionnaire de propriétés, élément de Shell.

**valeur de la propriété**

Valeur associée à un nom de propriété pour un élément de Shell. Par exemple, « auteur », « taille » et « date de prise » sont des propriétés. Les valeurs de propriété sont exprimées sous la forme d’une structure PROPVARIANT.

**Gestionnaire de protocole**

Gestionnaire qui accède aux sources de contenu et fournit un objet IUrlAccessor pour un protocole et une URL spécifiés. les gestionnaires de protocole étendent Windows fonctionnalité de recherche et peuvent fournir des notifications de modifications aux indexeurs. Différents gestionnaires de protocole sont requis pour indexer des types spécifiques de magasins de données. Pour fournir une expérience utilisateur raisonnable, vous devez également fournir une source de données Shell pour le magasin de données en plus de l’implémentation de votre gestionnaire de protocole. Le gestionnaire de protocole expose les éléments de la Banque de données à l’indexeur, tandis que la source de données Shell expose les éléments de la Banque de données au shell.

## <a name="r"></a>R

**restrictive**

condition qu’un fichier doit remplir pour être inclus dans les résultats de recherche retournés par Windows recherche.

**row**

Colonnes qui contiennent les valeurs de propriété qui décrivent un résultat unique à partir de l’ensemble d’objets qui correspondent aux restrictions spécifiées dans une requête de recherche.

**OpenXml**

Ensemble de lignes retournées dans les résultats de la recherche.

## <a name="s"></a>S

**connecteur de recherche**

Fichier XML qui contient des informations sur un magasin de données. Les connecteurs de recherche sont déployés pour la recherche fédérée.

**Rechercher dans le client**

Composant ou application qui interroge l’index.

**Rechercher dans la Fédération**

Consultez la définition de : fournisseur de recherche fédéré.

**moteur de recherche**

composant ou application qui fournit des données à Windows rechercher.

**étendue de recherche**

Ce terme est parfois utilisé pour signifier l’étendue de l’analyse. Consultez la définition de : étendue de l’analyse.

**Source de données Shell**

Composant utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données. Dans le passé, la source de données Shell était appelée extension d’espace de noms Shell. Voir aussi : conteneur, gestionnaire, élément de Shell.

**Extension de l’interpréteur de commandes**

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

**Gestionnaire d’extensions de Shell**

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

**Gestionnaire de Shell**

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

**Élément de Shell**

Une seule partie du contenu. Certains éléments de l’interpréteur de commandes sont des sources de contenu, et d’autres non. Un dossier est une source de contenu, par exemple, mais un fichier .jpg ne l’est pas. Les gestionnaires de types de fichiers exposent les éléments de Shell. Dans certains contextes, l’élément est utilisé pour distinguer les conteneurs des non-conteneurs. Voir aussi : conteneur, source de contenu, gestionnaire de type de fichier.

**Extension de l’espace de noms Shell**

Ce terme est parfois utilisé pour signifier la source de données Shell. Consultez la définition de : source de données Shell.

**menu contextuel**

Interface utilisateur utilisée pour présenter une collection de verbes associés à un élément d’interface utilisateur, tel qu’un fichier ou un dossier.

**Gestionnaire de menu contextuel**

Gestionnaire qui ajoute des verbes pour un élément ou des éléments. Ces verbes sont généralement affichés dans un menu contextuel. Voir aussi : menu contextuel.

**verbe statique**

Verbe qui s’applique à un élément de Shell sans avoir à inspecter l’état actuel d’un élément ou d’un système. Un verbe statique est basé sur une inscription statique des éléments associés d’un élément et ne change pas.

## <a name="t"></a>T

**Gestionnaire de miniatures**

Gestionnaire qui fournit une image statique pour représenter un élément de Shell.

**fournisseur de miniatures**

Ce terme est parfois utilisé pour signifier un gestionnaire de miniatures. Consultez la définition de : gestionnaire de miniatures.

## <a name="u"></a>U

**URL template**

Chaîne de connexion basée sur une URL qui est utilisée pour interroger un serveur Web afin d’obtenir les résultats de la recherche. Le modèle ressemble à une URL, mais contient plusieurs valeurs d’espace réservé (telles que {searchTerms}) que le client doit remplacer par les données relatives aux résultats qu’il souhaite récupérer. la définition des modèles d’URL est essentielle à l’implémentation de la recherche fédérée et des normes de OpenSearch.

**nom du type convivial de l’utilisateur**

Consultez la définition de : Kind.

## <a name="v"></a>V

**verbe**

Action individuelle qui peut être appelée par un élément de Shell. Exemples : ouvrir et imprimer. Les verbes sont parfois appelés commandes ou tâches. Voir aussi : verbe dynamique, gestionnaire de menu contextuel, verbe statique.

**Gestionnaire de verbes**

Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel. Consultez la définition de : gestionnaire de menu contextuel.

## <a name="w"></a>W

**avancer**

Consultez la définition de : parcours de l’espace de noms.

**Windows Search**

consultez la définition de : service de recherche de Windows.

**Windows Stocker les propriétés de recherche**

cache des valeurs de propriété utilisées dans l’implémentation du service de recherche Windows. ces valeurs de propriété peuvent être interrogées par programme à l’aide du fournisseur de OLE DB de recherche Windows. le magasin de propriétés de recherche Windows collecte et stocke les propriétés émises par les gestionnaires de filtres ou les gestionnaires de propriétés lorsqu’un élément, tel qu’un document Word, est indexé. Ce magasin est supprimé et reconstruit lors de la reconstruction de l’index.

**Windows Service de recherche**

fait référence à Windows Search 3,0 et versions ultérieures. Ce service analyse un ensemble de documents, extrait des informations utiles, puis organise les informations extraites afin que les propriétés de ces documents puissent être retournées efficacement en réponse aux requêtes. Voir aussi : catalogue.
