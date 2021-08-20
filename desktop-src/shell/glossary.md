---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
title: Glossaire de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9ef488a715532372592606f31dcfe1925a93dc29de78a54c869db83c21433c08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049862"
---
# <a name="shell-glossary"></a>Glossaire de l’interpréteur de commandes

## <a name="a"></a>A

<dl> <dt>

**Association**
</dt> <dd>

Mappage d’une extension de nom de fichier (par exemple, .mp3) ou protocole (par exemple, http) à un identificateur programmatique (ProgID). Ce mappage est stocké dans le Registre sous la forme d’un paramètre par utilisateur avec une solution de secours pour chaque ordinateur. Les applications qui participent au système de programmes par défaut définissent le mappage d’association pour l’extension de nom de fichier ou le protocole de manière à pointer vers les clés ProgID dont ils sont propriétaires.

</dd> <dt>

**Tableau d’association**
</dt> <dd>

Liste ordonnée d’emplacements du Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type. par exemple, un fichier de .jpg a le tableau d’association suivant sur un système de Windows par défaut : « hkcr \\ jpgfile », « hkcr \\ SystemFileAssociations \\.jpg », « hkcr \\ SystemFileAssociations \\ image », « hkcr \\ \* », « hkcr \\ AllFileSystemObjects ».

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Pour charger ou associer du code à des données. Par exemple, un gestionnaire peut être associé à une source de données Shell.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**nom canonique**
</dt> <dd>

Nom unique d’une ressource. Canonique signifie « selon les règles ». Voir aussi : nom de verbe canonique.

</dd> <dt>

**nom de verbe canonique**
</dt> <dd>

Nom indépendant du langage qui peut être utilisé par programme pour faire référence à un verbe, quelle que soit la chaîne localisée dans l’interface utilisateur. Voir aussi : nom canonique, verbe.

</dd> <dt>

**container**
</dt> <dd>

Type d’élément de Shell qui peut contenir d’autres éléments. Les éléments d’un conteneur sont exposés à l’espace de noms Shell à l’aide d’une source de données Shell. Les exemples incluent les dossiers, les lecteurs, les serveurs réseau et les fichiers compressés avec une extension de nom de fichier .zip. Voir aussi : source de données Shell, dossier, élément Shell.

</dd> <dt>

**content**
</dt> <dd>

Texte et propriétés associés à un élément de Shell ou à une source de contenu qui peut être indexée.

</dd> <dt>

**source du contenu**
</dt> <dd>

Élément auquel l’indexeur peut accéder. Les sources de contenu sont adressables par une URL et sont fournies à l’indexeur par un gestionnaire de protocole. voici quelques exemples : fichiers et dossiers du système de fichiers, éléments et dossiers de microsoft Outlook, enregistrements de base de données et éléments stockés dans microsoft SharePoint. Une source de contenu peut être exposée en tant qu’élément de Shell en implémentant une source de données Shell. Voir aussi : contenu, élément de Shell.

</dd> <dt>

**content view (affichage du contenu)**
</dt> <dd>

vue dans Windows Explorer (proposée dans Windows 7 et versions ultérieures) qui affiche le contenu le plus pertinent pour chaque élément de la liste en fonction de son extension de nom de fichier ou de son association de type. L’affichage du contenu utilise une logique de redimensionnement qui supprime des propriétés lorsque la taille de la fenêtre diminue pour s’assurer que les propriétés les plus critiques disposent toujours de suffisamment de place pour être clairement lisibles. Voir aussi : modèle de disposition, genre, Association de genres.

</dd> <dt>

**mode d’affichage du contenu**
</dt> <dd>

Consultez la définition de : vue de contenu.

</dd> <dt>

**menu contextuel**
</dt> <dd>

Ce terme est parfois utilisé pour signifier le menu contextuel. Consultez la définition de : menu contextuel.

</dd> <dt>

**Gestionnaire de menu contextuel**
</dt> <dd>

Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel. Consultez la définition de : gestionnaire de menu contextuel.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**gestionnaire d’objets de données**
</dt> <dd>

Gestionnaire qui fournit des formats de presse-papiers supplémentaires pour l’objet de données (IDataObject) d’un élément. Les objets de données sont utilisés dans les scénarios de glisser-déplacer et de copier/coller.

</dd> <dt>

**source de données**
</dt> <dd>

Ce terme est parfois utilisé pour signifier le magasin de données ou la source de données Shell. Consultez la définition de : magasin de données, source de données Shell.

</dd> <dt>

**magasin de données**
</dt> <dd>

Référentiel de données. Un magasin de données peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur à l’aide d’une source de données Shell. les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.

</dd> <dt>

**composition du Bureau**
</dt> <dd>

fonctionnalité Windows Vista qui permet aux fenêtres individuelles d’être dessinées sur des surfaces hors écran dans la mémoire vidéo au lieu d’être directement dessinées sur le périphérique d’affichage principal.

</dd> <dt>

**document**
</dt> <dd>

Élément de Shell qui contient du texte et pour lequel l’interface IFilter peut être implémentée.

</dd> <dt>

**supprimer le gestionnaire**
</dt> <dd>

Gestionnaire qui permet à un type d’élément particulier de prendre en charge les scénarios de glisser-déplacer et de copier/coller.

</dd> <dt>

**déplacer la cible**
</dt> <dd>

Objet de données qui est glissé et déposé dans un fichier. Voir aussi : gestionnaire de données, Drop handler.

</dd> <dt>

**verbe dynamique**
</dt> <dd>

Verbe qui dépend de l’état d’un élément de Shell ou du système ; l’apparence de l’élément est basée sur l’État et requiert que le code en cours d’exécution détermine si l’élément doit apparaître. Voir aussi : gestionnaire de menu contextuel, verbe statique, verbe.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Commande Explorer**
</dt> <dd>

objet qui peut être présenté sous la forme d’un bouton près du haut de la fenêtre de l’explorateur de Windows qui fournit des fonctionnalités pour les éléments et les conteneurs de cette fenêtre. une source de données Shell fournit les objets de commande Windows Explorer pour un élément de conteneur particulier. Les commandes sont parfois utilisées comme verbes.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Association de fichiers**
</dt> <dd>

Consultez la définition de : Association de types de fichiers.

</dd> <dt>

**format de fichier**
</dt> <dd>

Format des données stockées dans un fichier dont la spécification de format est documentée. Les exemples incluent OLE DocFile, OPC, XML, ZIP et d’autres spécifications de format de fichier connues. Les créateurs de type de fichier utilisent généralement un format de fichier existant comme base d’un nouveau type de fichier. Un format de fichier peut être simplement une définition qui n’est pas instanciée en tant que type de fichier.

</dd> <dt>

**Gestionnaire de format de fichier**
</dt> <dd>

Ce terme est un synonyme du gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

</dd> <dt>

**extension de nom de fichier**
</dt> <dd>

Indicateur principal d’un type de fichier pour les éléments du système de fichiers. il s’agit de la partie du nom de fichier qui suit le point final. L’extension de nom de fichier ne peut pas contenir d’espaces ou de caractères non ASCII et s’applique uniquement aux fichiers (et non aux dossiers). Les extensions de nom de fichier sont comparées à l’aide d’une fonction de comparaison qui ne respecte pas la casse ou les paramètres régionaux. Voir aussi : format de fichier, type de fichier.

</dd> <dt>

**type de fichier**
</dt> <dd>

Une valeur d’extension de nom de fichier particulière, telle que « .htm » ou « .jpg », définit une classe de fichiers qui sont du même type et qui ont un ensemble commun d’associations. Voir aussi : genre, Association de type de fichier.

</dd> <dt>

**association de types de fichier**
</dt> <dd>

Pour une extension de nom de fichier particulière, les éléments de tableau d’association qui définissent où les gestionnaires et d’autres attributs peuvent être inscrits. Voir aussi : tableau d’association, type de fichier.

</dd> <dt>

**personnalisation du type de fichier**
</dt> <dd>

Association qui permet à Shell de personnaliser la manière dont l’interpréteur de commandes traite un type de fichier. Les personnalisations de type de fichier incluent la spécification de l’application utilisée pour ouvrir le fichier lorsque vous double-cliquez dessus, l’ajout de commandes au menu contextuel pour un type de fichier, la spécification d’une icône personnalisée, la spécification d’un type de contenu MIME à associer à un type de fichier, la spécification d’un type perçu et la spécification d’une ou plusieurs applications associées à un type Voir aussi : PerceivedType.

</dd> <dt>

**Gestionnaire de type de fichier**
</dt> <dd>

Gestionnaire inscrit pour un type de fichier. Voir aussi : handler.

</dd> <dt>

**Répertoire**
</dt> <dd>

Consultez la définition de : Container.

</dd> <dt>

**PIDL complet**
</dt> <dd>

PIDL qui décrit de façon unique un objet par rapport au dossier Desktop.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**gestionnaire**
</dt> <dd>

Objet COM qui fournit les fonctionnalités d’un élément de Shell. La plupart des sources de données Shell offrent un système extensible pour lier les gestionnaires aux éléments. Par exemple, le dossier de système de fichiers utilise le système d’association pour rechercher les gestionnaires pour un type de fichier particulier. Voir aussi : Association de fichier, type de fichier, personnalisation de type de fichier.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**gestionnaire d’icône**
</dt> <dd>

Gestionnaire qui fournit les informations nécessaires pour générer et mettre en cache une icône pour un élément. Le magasin de données du système de fichiers prend en charge le chargement d’un gestionnaire d’icône pour un élément en fonction du type de fichier, ce qui permet à ce gestionnaire de fournir une icône qui est utilisée pour toutes les instances de ce type de fichier.

</dd> <dt>

**gestionnaire d’info-bulle**
</dt> <dd>

Gestionnaire qui fournit le texte contextuel lorsque l’utilisateur place le pointeur de la souris sur un objet d’interface utilisateur.

</dd> <dt>

**item**
</dt> <dd>

Consultez la définition de : élément de Shell.

</dd> <dt>

**Item (classe)**
</dt> <dd>

Consultez la définition de : type de fichier.

</dd> <dt>

**liste d’identificateurs d’éléments**
</dt> <dd>

Séquence d’une ou plusieurs structures SHITEMID qui définissent de façon unique un objet par rapport à un objet racine.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Type**
</dt> <dd>

Propriété qui fournit un nom de genre convivial et qui peut être associée à une liste de propriétés et un modèle de disposition. le genre a été introduit dans Windows Vista pour exprimer une notion plus conviviale de type de fichier par l’utilisateur final et il a été défini comme étant une propriété de chaîne à valeurs multiples (valeurs de chaîne canoniques). vous pouvez donc avoir une valeur de type « audio, vidéo » ou « liaison ; document ». Certains noms de genres conviviaux sont déjà associés à des propriétés et des modèles de disposition. Par exemple, les éléments associés au type. Picture et aux éléments associés à Kind.Document affichent des propriétés différentes, même s’ils se trouvent dans la même vue. Chaque genre d’élément peut être associé à l’un des quatre modèles de disposition uniques qui définissent le nombre de propriétés affichées pour chaque élément et leur disposition. Voir aussi : Association de genres, vue de contenu, modèle de disposition.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**modèle de disposition**
</dt> <dd>

L’un des nombreux mécanismes d’affichage des propriétés. dans Windows 7 et versions ultérieures, lorsque vous inscrivez un nouveau type de fichier, vous pouvez utiliser l’affichage de contenu pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier. Vous pouvez choisir parmi quatre modèles de disposition différents : alpha (pour les résultats de recherche de documents qui contiennent des extraits de code), la version bêta (pour les résultats de recherche par courrier électronique avec extraits de code), gamma (semblable à alpha mais avec une disposition sur deux lignes au lieu de quatre) et Delta Voir aussi : vue de contenu, genre, Association de genres.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Gestionnaire de métadonnées**
</dt> <dd>

Ce terme est parfois utilisé pour signifier le gestionnaire de propriétés. Consultez la définition de : gestionnaire de propriétés.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**extension de l’espace de noms**
</dt> <dd>

Consultez la définition de : source de données Shell.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Base de données de liaison et d’incorporation d’objets (OLE DB)**
</dt> <dd>

Ensemble standard d’interfaces qui fournit un accès hétérogène à des sources disparates d’informations situées n’importe où, comme les systèmes de fichiers, les dossiers de messagerie et les bases de données.

</dd> <dt>

**OLE DB**
</dt> <dd>

Consultez la définition de : liaison objet et incorporation d’une base de données.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**PerceivedType**
</dt> <dd>

Catégorie étendue de types de format de fichier. PerceivedType a été introduit dans Windows XP et prend en charge un ensemble limité de types de fichiers connus (par exemple, les types de fichier Image, texte, Audio et fichiers compressés). Les types de fichiers, généralement les types de fichiers publics, peuvent également avoir un type perçu. Par exemple, les types de fichiers image .bmp, .png, .jpg et .gif sont également du type perçu, image. Au niveau de la couche de programmation, PerceivedType est exprimé sous la forme d’un entier. Étant donné que du code utilise Kind et PerceivedType, les propriétaires de format de fichier doivent inscrire les deux. Par exemple, « lire tout » dépend de PerceivedType. Voir aussi : type de fichier.

</dd> <dt>

**gestionnaire d’aperçus**
</dt> <dd>

gestionnaire qui produit rapidement une vue simplifiée en lecture seule de l’élément de Shell à afficher dans le volet de visualisation de l’explorateur de Windows.

</dd> <dt>

**Gestionnaire de propriétés**
</dt> <dd>

gestionnaire qui traduit les données stockées dans un fichier dans un schéma structuré qui est reconnu par et qui est accessible par Windows Explorer, Windows Search et d’autres applications. Ces systèmes peuvent ensuite interagir avec le gestionnaire de propriétés pour écrire et lire les propriétés vers et à partir du fichier. Les données traduites comprennent la vue détails, info-bulles, le volet Détails, les pages de propriétés, etc. Chaque gestionnaire de propriétés est associé à un type de fichier particulier, identifié par l’extension de nom de fichier. Voir aussi : système de propriétés.

</dd> <dt>

**Gestionnaire de feuille de propriétés**
</dt> <dd>

Gestionnaire utilisé pour créer des feuilles de propriétés personnalisées avec des images et des contrôles d’interface utilisateur qui autorisent une interaction personnalisée avec un type de fichier.

</dd> <dt>

**système de propriétés**
</dt> <dd>

Système extensible de lecture/écriture de définitions de données qui utilise des propriétés implémentées en tant que paires nom-valeur. Voir aussi : gestionnaire de propriétés, élément de Shell.

</dd> <dt>

**valeur de la propriété**
</dt> <dd>

Valeur associée à un nom de propriété pour un élément de Shell. Par exemple, « auteur », « taille » et « date de prise » sont des propriétés. Les valeurs de propriété sont exprimées sous la forme d’une structure PROPVARIANT.

</dd> <dt>

**Gestionnaire de protocole**
</dt> <dd>

Gestionnaire qui accède aux sources de contenu et fournit un objet IUrlAccessor pour un protocole et une URL spécifiés. les gestionnaires de protocole étendent Windows fonctionnalité de recherche et peuvent fournir des notifications de modifications aux indexeurs. Différents gestionnaires de protocole sont requis pour indexer des types spécifiques de magasins de données. Pour fournir une expérience utilisateur raisonnable, vous devez également fournir une source de données Shell pour le magasin de données en plus de l’implémentation de votre gestionnaire de protocole. Le gestionnaire de protocole expose les éléments de la Banque de données à l’indexeur, tandis que la source de données Shell expose les éléments de la Banque de données au shell.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**PIDL relatif**
</dt> <dd>

PIDL relatif à un objet racine de l’espace de noms Shell autre que le dossier Desktop. Il s’agit généralement du dossier parent de l’élément.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Source de données Shell**
</dt> <dd>

Composant utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données. Dans le passé, la source de données Shell était appelée extension d’espace de noms Shell. Voir aussi : conteneur, gestionnaire, élément de Shell.

</dd> <dt>

**Extension de l’interpréteur de commandes**
</dt> <dd>

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

</dd> <dt>

**Gestionnaire d’extensions de Shell**
</dt> <dd>

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

</dd> <dt>

**Gestionnaire de Shell**
</dt> <dd>

Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier. Consultez la définition de : gestionnaire de type de fichier.

</dd> <dt>

**Élément de Shell**
</dt> <dd>

Une seule partie du contenu. Certains éléments de l’interpréteur de commandes sont des sources de contenu, et d’autres non. Un dossier est une source de contenu, par exemple, mais un fichier .jpg ne l’est pas. Les gestionnaires de types de fichiers exposent les éléments de Shell. Dans certains contextes, l’élément est utilisé pour distinguer les conteneurs des non-conteneurs. Voir aussi : conteneur, source de contenu, gestionnaire de type de fichier.

</dd> <dt>

**Extension de l’espace de noms Shell**
</dt> <dd>

Ce terme est parfois utilisé pour signifier la source de données Shell. Consultez la définition de : source de données Shell.

</dd> <dt>

**menu contextuel**
</dt> <dd>

Interface utilisateur utilisée pour présenter une collection de verbes associés à un élément d’interface utilisateur, tel qu’un fichier ou un dossier.

</dd> <dt>

**Gestionnaire de menu contextuel**
</dt> <dd>

Gestionnaire qui ajoute des verbes pour un élément ou des éléments. Ces verbes sont généralement affichés dans un menu contextuel. Voir aussi : menu contextuel.

</dd> <dt>

**PIDL simple**
</dt> <dd>

PIDL analysé sans vérification du disque.

</dd> <dt>

**verbe statique**
</dt> <dd>

Verbe qui s’applique à un élément de Shell sans avoir à inspecter l’état actuel d’un élément ou d’un système. Un verbe statique est basé sur une inscription statique des éléments associés d’un élément et ne change pas.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Gestionnaire de miniatures**
</dt> <dd>

Gestionnaire qui fournit une image statique pour représenter un élément de Shell.

</dd> <dt>

**fournisseur de miniatures**
</dt> <dd>

Ce terme est parfois utilisé pour signifier un gestionnaire de miniatures. Consultez la définition de : gestionnaire de miniatures.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**nom du type convivial de l’utilisateur**
</dt> <dd>

Consultez la définition de : Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**verbe**
</dt> <dd>

Action individuelle qui peut être appelée par un élément de Shell. Exemples : ouvrir et imprimer. Les verbes sont parfois appelés commandes ou tâches. Voir aussi : verbe dynamique, gestionnaire de menu contextuel, verbe statique.

</dd> <dt>

**Gestionnaire de verbes**
</dt> <dd>

Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel. Consultez la définition de : gestionnaire de menu contextuel.

</dd> </dl>

 

 



