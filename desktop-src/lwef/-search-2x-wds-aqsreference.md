---
title: Syntaxe de requête avancée
description: la syntaxe de requête avancée (AQS) est utilisée par Microsoft Windows Desktop Search (WDS) pour aider les utilisateurs et les programmeurs à mieux définir et limiter leurs recherches.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 9517041a0a240c40722e8c21da960b9fc8deef09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415889"
---
# <a name="advanced-query-syntax"></a>Syntaxe de requête avancée

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

la syntaxe de requête avancée (AQS) est utilisée par Microsoft Windows Desktop Search (WDS) pour aider les utilisateurs et les programmeurs à mieux définir et limiter leurs recherches. L’utilisation de AQS est un moyen simple de limiter les recherches et de fournir de meilleurs jeux de résultats. Les recherches peuvent être limitées par les paramètres suivants :

- Types de fichiers : dossiers, documents, présentations, images, etc.
- Magasins de fichiers : bases de données et emplacements spécifiques.
- Propriétés du fichier : taille, date, titre, etc.
- Contenu du fichier : Mots clés tels que « livrables du projet », « AQS », « chaussures de attrait bleu », etc.

En outre, les paramètres de recherche peuvent être combinés à l’aide d’opérateurs de recherche. Le reste de cette section explique la syntaxe de requête, les paramètres et les opérateurs, et comment ils peuvent être combinés pour offrir des résultats de recherche ciblés. les tables décrivent la syntaxe à utiliser avec WDS, ainsi que les propriétés qui peuvent être interrogées pour chaque type de fichier affiché dans la fenêtre des résultats de la **recherche de bureau Windows** .

## <a name="desktop-search-syntax"></a>Syntaxe de Desktop Search

Une requête de recherche peut inclure un ou plusieurs mots clés, avec des opérateurs booléens et des critères facultatifs. Ces critères facultatifs peuvent affiner une recherche basée sur les éléments suivants :

- Portée ou magasin de données dans lequel les fichiers résident
- Genres de fichiers
- Propriétés managées des fichiers

Les critères facultatifs, décrits plus en détail ci-dessous, utilisent la syntaxe suivante :

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Supposons qu’un utilisateur souhaite rechercher un document contenant l’expression « dernier trimestre » créé par John ou Joanne, et que l’utilisateur a enregistré dans le dossier MyDocuments. La requête peut se présenter comme suit :

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Étendue : emplacements et banques de données

Les utilisateurs peuvent limiter l’étendue de leurs recherches à des emplacements de dossiers ou des magasins de données spécifiques. par exemple, si vous utilisez plusieurs comptes de messagerie et que vous souhaitez limiter une requête à microsoft Outlook ou microsoft Outlook Express, vous pouvez utiliser `store:outlook` ou `store:oe` respectivement.

| Limiter la recherche par le magasin de données | Utiliser              | Exemple                                  |
|-------------------------------|------------------|------------------------------------------|
| Bureau                       | Bureau          | Store : Desktop                            |
| Fichiers                         | files            | Store : fichiers                              |
| Outlook                       | programme          | Store : Outlook                            |
| Outlook Express               | oe               | magasin : oe                                 |
| Dossier spécifique               | NomDossier ou in | NomDossier : MyDocuments ou dans : MyDocuments |

Si vous avez un gestionnaire de protocole en place pour analyser des magasins personnalisés, comme Lotus Notes, vous pouvez utiliser le nom du magasin ou du gestionnaire de protocole pour le magasin. Par exemple, si vous avez implémenté un gestionnaire de protocole pour inclure une banque de données Lotus Notes comme « notes », la syntaxe de la requête serait `store:notes` .

### <a name="common-file-kinds"></a>Genres de fichiers communs

Les utilisateurs peuvent également limiter leurs recherches à des types de fichiers spécifiques, appelés genres de fichiers. Le tableau suivant répertorie les types de fichiers et fournit des exemples de la syntaxe utilisée pour rechercher ces types de fichiers.

| Pour restreindre par type de fichier :       | Utiliser              | Exemple                        |
|---------------------------------|------------------|--------------------------------|
| Tous les types de fichiers                  | tout       | genre : tout                |
| Communications                  | communications   | genre : communications            |
| Contacts                        | contacts         | genre : contacts                  |
| Messagerie électronique                          | email            | genre : courrier électronique                     |
| Conversations par messagerie instantanée | im               | genre : im                        |
| Face                        | face         | genre : réunions                  |
| Tâches                           | tâches            | genre : tâches                     |
| Notes                           | HDInsight            | genre : Remarques                     |
| Documents                       | docs             | genre : docs                      |
| Documents texte                  | text             | genre : texte                      |
| Tableurs                    | feuilles     | genre : feuilles de calcul              |
| Présentations                   | présentations    | genre : présentations             |
| Musique                           | music            | genre : musique                     |
| Images                        | pics             | genre : pics                      |
| Vidéos                          | videos           | genre : vidéos                    |
| Dossiers                         | dossiers          | genre : dossiers                   |
| Nom de dossier                     | NomDossier ou in | NomDossier : mydocs ou in : mydocs |
| Favoris                       | favoris        | genre : favoris                 |
| Programmes                        | programmes         | genre : programmes                  |

### <a name="boolean-operators"></a>Opérateurs booléens

Les mots clés de recherche et les propriétés de fichier peuvent être combinés pour élargir ou limiter une recherche avec des opérateurs. Le tableau suivant décrit les opérateurs courants utilisés dans une requête de recherche.

| Mot clé/symbole  | Exemples | Fonction |
|---|---|----|
| NOT             | sécurité sociale non sécurisée<br/>                        | Recherche les éléments qui contiennent des *réseaux sociaux*, mais pas la *sécurité*.<br/>                                              |
|                 | sécurité sociale<br/>                           | Recherche des éléments qui contiennent des *réseaux sociaux* et de *sécurité*.<br/>                                              |
| OR              | réseaux sociaux ou sécurité<br/>                         | Recherche des éléments qui contiennent des *réseaux sociaux* ou de *sécurité*.<br/>                                                    |
| Guillemets | « sécurité sociale »<br/>                          | Recherche les éléments qui contiennent la phrase exacte *sécurité sociale*.<br/>                                        |
| Parenthèses     | (sécurité sociale)<br/>                          | Recherche des éléments qui contiennent des *réseaux sociaux* et de la *sécurité* dans n’importe quel ordre.<br/>                                      |
| >            | Date : >11/13/21<br/> taille : >500<br/>  | Recherche les éléments dont la date est postérieure à MM/JJ/AA. <br/> Recherche les éléments dont la taille est supérieure à 500 octets.<br/> |
| <            | Date : <11/13/21 <br/> taille : <500<br/> | Recherche les éléments dont la date est antérieure à MM/JJ/AA. <br/> Recherche les éléments dont la taille est inférieure à 500 octets.<br/>   |
| ..              | Date : 11/13/21.. 11/15/21<br/>                    | Recherche les éléments dont la date commence à MM/JJ/AA et se termine le MM/JJ/AA.<br/>                               |

> [!Note]
> Les opérateurs **not** et **or** doivent être en majuscules et ne peuvent pas être combinés dans une requête (par exemple, `social OR security NOT retirement` ).

### <a name="boolean-properties"></a>Propriétés booléennes

Certains types de fichiers permettent aux utilisateurs de rechercher des fichiers à l’aide des propriétés booléennes, comme décrit dans le tableau suivant.

| Propriété | Exemple | Fonction |
|---|---|---|
| est : pièce jointe  | rapport : pièce jointe      | Recherche les éléments qui ont des pièces jointes qui contiennent un *rapport*. Comme pour `isattachment:true`.                           |
| isonline:      | rapport IsOnline : true      | Recherche les éléments en ligne et qui contiennent un *rapport*.                                                         |
| IsRecurring   | rapport IsRecurring : true   | Recherche les éléments récurrents et contenant le *rapport*.                                                       |
| isflagged:     | rapport isflagged : true     | Recherche les éléments signalés (révision, suivi, par exemple) et contenant le *rapport*.                       |
| IsDeleted     | rapport IsDeleted : true     | Recherche les éléments marqués comme supprimés (Corbeille ou éléments supprimés, par exemple) et qui contiennent un *rapport*. |
| IsCompleted   | État IsCompleted : false  | Recherche les éléments qui ne sont pas marqués comme terminés et qui contiennent un *rapport*.                                        |
| HasAttachment | rapport HasAttachment : true | Recherche des éléments contenant des *rapports* et des pièces jointes                                                          |
| HasFlag       | rapport HasFlag : true       | Recherche des éléments contenant un *rapport* et ayant des indicateurs.                                                                |

### <a name="dates"></a>Dates

En plus de la recherche de dates et de plages de dates spécifiques à l’aide des opérateurs décrits précédemment, AQS autorise les valeurs de date relatives (telles que `today` , `tomorrow` ou `next week` ) et le jour (comme `Tuesday` ou `Monday..Wednesday` ) et le mois ( `February` ).

| Par rapport à :    | Exemple de syntaxe | Résultats |
|----|---|---|
| Jour | Date : aujourd’hui<br/> Date : demain<br/> Date : hier<br/> | Recherche des éléments avec la date du jour.<br/> Recherche des éléments avec la date de demain.<br/> Recherche des éléments avec la date d’hier. <br/> |
| Semaine/mois/année | Date : cette semaine<br/> Date : dernière semaine<br/> Date : mois suivant<br/> Date : mois dernier<br/> Date : année à venir <br/> | Recherche les éléments dont la date est comprise dans la semaine en cours.<br/> Recherche les éléments dont la date est comprise dans la semaine précédente.<br/> Recherche les éléments dont la date est comprise dans la semaine à venir.<br/> Recherche les éléments dont la date est comprise dans le mois précédent.<br/> Recherche les éléments dont la date est comprise dans l’année à venir. <br/> |

## <a name="properties-by-file-kind"></a>Propriétés par genre de fichier

Les utilisateurs peuvent effectuer des recherches sur des propriétés spécifiques de différents types de fichiers. Certaines propriétés (telles que la taille de fichier) sont communes à tous les fichiers, tandis que d’autres sont limitées à un type spécifique. Le nombre de diapositives, par exemple, est spécifique aux présentations. Les tableaux suivants répertorient ces propriétés par genre de fichier.

### <a name="file-kind-everything"></a>Genre de fichier : tout

Il s’agit de propriétés communes à tous les types de fichiers. Pour inclure tous les types de fichiers dans une requête, la syntaxe est la suivante :

`kind:everything <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété       | Utiliser                      | Exemple                        |
|----------------|--------------------------|--------------------------------|
| Intitulé          | titre, objet ou à propos de  | titre : « financier trimestriel »    |
| Statut         | status                   | État : terminé                |
| Date           | date                     | Date : dernière semaine                 |
| Date de modification  | DateModified ou modifié | modifié : dernière semaine             |
| Importance     | importance ou priorité   | importance : haute                |
| Taille           | taille                     | taille : > 50                   |
| Deleted        | Deleted ou IsDeleted     | IsDeleted : true                 |
| Est une pièce jointe  | isattachment             | isattachment : true              |
| À             | à ou toname             | à : Bob                         |
| Cc             | CC ou ccname             | CC : John                        |
| Company        | société                  | société : Microsoft              |
| Emplacement       | location                 | emplacement : « salle de conférence 102 » |
| Category       | catégorie                 | Catégorie : entreprise              |
| Mots clés       | mots clés                 | Mots clés : « projections de ventes »   |
| Album          | album                    | album : « passage à la nuit »           |
| Nom de fichier      | nom de fichier ou fichier         | nom de fichier : MyResume              |
| Genre          | genre                    | genre : Rock                     |
| Auteur         | auteur ou par             | Auteur : « Stephen King »          |
| Personnes         | personnes ou avec           | avec : (Sonja ou David)          |
| Dossier         | dossier, sous ou chemin d’accès    | dossier : téléchargements               |
| Extension de fichier | ext ou fileext           | ext:.txt                       |

### <a name="attachment"></a>Pièce jointe

Il s’agit de propriétés communes aux pièces jointes. Pour limiter la recherche aux pièces jointes, la syntaxe est la suivante :

`kind:attachment <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété | Utiliser            | Exemple                  |
|----------|----------------|--------------------------|
| Personnes   | personnes ou avec | personnes : John ou avec : John |

### <a name="contacts"></a>Contacts

Il s’agit des propriétés communes aux contacts. Pour limiter la recherche aux contacts uniquement, la syntaxe est la suivante :

`kind:contacts <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété              | Utiliser                 | Exemple                            |
|-----------------------|---------------------|------------------------------------|
| Fonction             | jobtitle            | JobTitle : directeur financier                       |
| Adresse de messagerie instantanée            | imadresse           | adresse : John\_doe@msn.com        |
| Téléphone de l’Assistant     | assistantsphone     | assistantsphone : 555-3323           |
| Nom de l’Assistant        | assistantname       | AssistantName : Paul                 |
| Profession            | exercice          | profession : plombier                 |
| Surnom              | nickname            | surnom : Tex                       |
| Époux                | époux              | Époux : Debbie                      |
| Ville de l’entreprise         | businesscity        | businesscity : Seattle               |
| Code postal de l’entreprise  | businesspostalcode  | businesspostalcode : 98006           |
| Page d’espace professionnel    | businesshomepage    | BusinessHomePage : www. Office. com |
| Numéro de téléphone de rappel | callbackphonenumber | callbackphonenumber : 555-555-2121   |
| Téléphone voiture             | procède            | procède : 555-555-2121              |
| Children              | enfants            | enfants : Timmy                     |
| Prénom            | firstname           | Prénom : John                     |
| Nom             | lastname            | nom : Doe                       |
| Télécopie personnelle              | homefax             | homefax : 555-555-2121               |
| Nom du responsable        | managersname        | managersname : John                  |
| Récepteur de radiomessagerie                 | pager               | radiomessagerie : 555-555-2121                 |
| Téléphone professionnel        | BusinessPhone       | BusinessPhone : 555-555-2121         |
| Téléphone personnel            | homePhone           | HomePhone : 555-555-2121             |
| Téléphone mobile          | MobilePhone         | MobilePhone : 555-555-2121           |
| Office                | Office              | Office : exemple                      |
| Ans           | ans         | anniversaire : 1/1/06                 |
| Birthday              | proche            | anniversaire : 1/1/06                    |
| Page web              | pages             | page Web : www. Microsoft. com          |

> [!Note]
> les numéros de Téléphone sont indexés comme entrés. Par exemple, si un utilisateur n’a pas inclus de code de pays ou de région lors de la saisie du numéro de téléphone, les utilisateurs ne peuvent pas localiser un contact si la recherche porte sur le pays ou l’indicatif régional dans le numéro de téléphone.

### <a name="communications"></a>Communications

Il s’agit de propriétés communes aux communications. Pour limiter la recherche aux communications uniquement, la syntaxe est la suivante :

`kind:communications <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété       | Utiliser                           | Exemple                         |
|----------------|-------------------------------|---------------------------------|
| Du           | à partir de ou de l’organisateur             | à partir de : John                       |
| Reçu       | reçu ou envoyé              | envoyé : hier                  |
| Objet        | objet ou titre              | objet : « financier trimestriel »   |
| A une pièce jointe | HasAttachments, HasAttachment | HasAttachment : true              |
| Pièces jointes    | pièces jointes ou pièces jointes     | attachment:presentation.ppt     |
| Cci            | BCC, bccname ou bccaddress    | CCI : Dave                        |
| Adresse CC     | ccaddress ou CC               | ccaddress : John\_doe@outlook.com |
| Indicateur de suivi | followupflag                  | followupflag : 2                  |
| Date d’échéance       | DueDate ou due                | échéance : dernière semaine                   |
| Lire           | lecture ou IsRead                | est : lecture                         |
| Est terminée   | IsCompleted                   | est : terminé                    |
| Incomplet     | incomplet ou isincomplete    | est : incomplet                   |
| A un indicateur       | HasFlag ou isflagged          | has : indicateur                        |
| Duration       | duration                      | Durée : > 50                |

### <a name="calendar"></a>Calendrier

Il s’agit de propriétés communes aux calendriers. Pour limiter la recherche aux calendriers uniquement, la syntaxe est la suivante :

`kind:calendar <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété  | Utiliser                      | Exemple          |
|-----------|--------------------------|------------------|
| Périodique | périodique ou IsRecurring | est : périodique     |
| Organizer | Organisateur, par ou à partir de    | Organisateur : Debbie |

### <a name="documents"></a>Documents

Il s’agit de propriétés communes aux documents. Pour limiter la recherche aux documents uniquement, la syntaxe est la suivante :

`kind:documents <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété          | Utiliser             | Exemple                       |
|-------------------|-----------------|-------------------------------|
| Commentaires          | comments        | Commentaires : « nécessite une revue finale » |
| Dernier enregistrement par     | lastsavedby     | LastSavedBy : John              |
| Gestionnaire de documents  | DocumentManager | DocumentManager : John          |
| Numéro de révision   | RevisionNumber  | RevisionNumber : 1.0.3          |
| Format du document   | DocumentFormat  | DocumentFormat : MIMETYPE       |
| Date de la dernière impression | datelastprinted | datelastprinted : dernière semaine     |

### <a name="presentation"></a>Présentation

Il s’agit de propriétés communes aux présentations. Pour limiter la recherche aux présentations uniquement, la syntaxe est la suivante :

`kind:presentation <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété    | Utiliser        | Exemple           |
|-------------|------------|-------------------|
| Nombre de diapositives | slidecount | slidecount : >20 |

### <a name="music"></a>Musique

Il s’agit de propriétés communes aux fichiers musicaux. Pour limiter la recherche uniquement à la musique, la syntaxe est la suivante :

`kind:music <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété | Utiliser                | Exemple                  |
|----------|--------------------|--------------------------|
| Vitesse de transmission | débit binaire, taux      | débit binaire : 192              |
| Peinture   | artiste, par ou à partir de | Artiste : John singe       |
| Duration | duration           | Durée : 3               |
| Album    | album              | album : « meilleurs résultats »    |
| Genre    | genre              | genre : Rock               |
| Suivre    | track              | suivi : 12                 |
| Year     | year               | année : > 1980 < 1990 |

### <a name="picture"></a>Image

Il s’agit de propriétés communes aux images. Pour limiter la recherche aux seules images, la syntaxe est la suivante :

`kind:picture <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété     | Utiliser         | Exemple               |
|--------------|-------------|-----------------------|
| Marque de l’appareil photo  | cameramake  | cameramake : exemple     |
| Modèle d’appareil photo | cameramodel | CameraModel : exemple    |
| Dimensions   | dimensions  | Dimensions : 8X10       |
| Orientation  | orientation | orientation : paysage |
| Date de prise   | datetaken   | DateTaken : hier   |
| Largeur        | width       | Largeur : 1600            |
| Hauteur       | height      | hauteur : 1200           |

### <a name="video"></a>Vidéo

Il s’agit de propriétés communes aux vidéos. Pour limiter la recherche aux vidéos uniquement, la syntaxe est la suivante :

`kind:video <property>:<value>`

où `<property>` est une propriété listée ci-dessous et `<value>` est le terme de recherche spécifié par l’utilisateur.

| Propriété | Utiliser           | Exemple                                |
|----------|---------------|----------------------------------------|
| Nom     | nom, objet | nom : « vacances familiales jusqu’au Beach 05 » |
| Extension      | ext, fileext  | ext:.avi                               |

## <a name="related-topics"></a>Rubriques connexes

**Informations de référence**

[Types perçus](-search-2x-wds-perceivedtype.md)

[SchemaTable](-search-2x-wds-schematable.md)

[Appel de WDS à partir de la ligne de commande](-search-2x-wds-fromcommandline.md)

[Appel de WDS à partir de pages Web](-search-2x-wds-browserhelpobject.md)
