---
description: L’action MoveFiles localise les fichiers existants sur l’ordinateur de l’utilisateur et déplace ou copie ces fichiers vers un nouvel emplacement.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Action MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868865"
---
# <a name="movefiles-action"></a>Action MoveFiles

L’action MoveFiles localise les fichiers existants sur l’ordinateur de l’utilisateur et déplace ou copie ces fichiers vers un nouvel emplacement. L’action MoveFiles interroge la [table MoveFile](movefile-table.md) et déplace les fichiers spécifiés ici si le composant lié aux entrées est spécifié pour être installé localement ou s’il est en cours d’exécution à partir de la source.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action MoveFiles doit venir après l’action [InstallValidate](installvalidate-action.md) et avant l’action [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                  |
|-------|---------------------------------------------|
| \[1\] | Identificateur du fichier déplacé.                   |
| \[6\] | Taille du fichier installé en octets.            |
| \[9\] | Identificateur du répertoire contenant le fichier déplacé. |



 

## <a name="remarks"></a>Notes

La table MoveFiles contient une colonne nommée « options » qui spécifie les fichiers sources à déplacer ou à copier. Un fichier source déplacé est supprimé une fois qu’il a été copié vers un nouvel emplacement. Pour connaître la syntaxe exacte, consultez la [table MoveFile](movefile-table.md).

Les colonnes SourceFolder et DestFolder de la table MoveFile sont des noms de propriétés dont les valeurs sont censées être résolues en chemins d’accès complets. Ces propriétés peuvent correspondre à l’une des entrées d’annuaire de la table de [répertoire](directory-table.md) , à toute propriété de dossier prédéfinie ([**FavoritesFolder**](favoritesfolder.md), par exemple) ou à une propriété définie par une entrée de la table [AppSearch](appsearch-table.md) . Ces propriétés peuvent contenir un chemin d’accès complet contenant le nom de fichier d’un fichier spécifique. Par exemple, la table AppSearch peut être créée pour rechercher un fichier particulier et définir une propriété sur le chemin d’accès complet à ce fichier. Dans cet exemple, la colonne SourceName de la table MoveFile peut être laissée vide pour indiquer que la valeur de la propriété SourceFolder contient un chemin d’accès complet au fichier. Le point-virgule est le délimiteur de liste pour les transformations, les sources et les correctifs, et ne doit pas être utilisé dans les chemins d’accès ou les noms de fichiers.

L’action MoveFiles n’agit pas sur les entrées de la table MoveFile dans lesquelles la propriété SourceFolder ou DestFolder ne correspond pas à un chemin d’accès complet.

L’action MoveFiles tente de déplacer ou de copier tous les fichiers du répertoire source qui correspondent au nom donné dans la colonne SourceName de la table MoveFiles. Le nom dans la colonne SourceName peut inclure \* ou ? caractères génériques qui permettent de déplacer ou de copier un groupe de fichiers. Par exemple, la colonne SourceName peut contenir une entrée de « \* . xls » et l’action MoveFiles déplace ou copie chaque classeur Microsoft Excel du répertoire source vers la destination.

Le nom à attribuer au fichier de destination peut être spécifié dans la colonne DestName de la table MoveFile. Le nom du fichier de destination conserve le nom du fichier source si cette colonne est laissée vide.

Si un \* caractère générique «» est entré dans la colonne SourceName de la [table MoveFile](movefile-table.md) et qu’un nom de fichier de destination est spécifié dans la colonne DestName, tous les fichiers déplacés ou copiés conservent les noms dans les sources.

Les fichiers qui sont déplacés ou copiés par l’action MoveFiles ne sont pas supprimés lorsque le produit est désinstallé.

 

 



