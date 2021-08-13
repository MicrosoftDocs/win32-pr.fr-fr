---
description: L’action DuplicateFiles duplique les fichiers installés par l’action InstallFiles. Les fichiers dupliqués peuvent être copiés dans le même répertoire avec un nom différent ou dans un répertoire différent avec le nom d’origine.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Action DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637711"
---
# <a name="duplicatefiles-action"></a>Action DuplicateFiles

L’action DuplicateFiles duplique les fichiers installés par l’action [InstallFiles](installfiles-action.md) . Les fichiers dupliqués peuvent être copiés dans le même répertoire avec un nom différent ou dans un répertoire différent avec le nom d’origine.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action DuplicateFiles doit venir après l' [action InstallFiles](installfiles-action.md). L’action DuplicateFiles doit également être postérieure à l' [action PatchFiles](patchfiles-action.md) pour empêcher la duplication de la version non corrigée du fichier.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                       |
|-------|--------------------------------------------------|
| \[1\] | Identificateur du fichier dupliqué.                   |
| \[6\] | Taille du fichier dupliqué.                         |
| \[9\] | Identificateur du répertoire contenant le fichier dupliqué. |



 

## <a name="remarks"></a>Remarques

L’action DuplicateFiles traite une entrée de [table DuplicateFile](duplicatefile-table.md) uniquement si le composant lié à cette entrée est installé localement. Pour plus d’informations, consultez [table des composants](component-table.md).

La chaîne dans le champ DestFolder est un nom de propriété dont la valeur est supposée être résolue en chemin d’accès qualifié complet. Cette propriété peut être l’une des entrées d’annuaire de la table de [répertoire](directory-table.md) , toute propriété de dossier prédéfinie ([**CommonFilesFolder**](commonfilesfolder.md), par exemple) ou une propriété définie par une entrée de la table [AppSearch](appsearch-table.md) . Si la propriété **DestFolder** ne correspond pas à un chemin d’accès valide, l’action DuplicateFiles ne fait rien pour cette entrée.

Si le nom du fichier de destination dans la colonne DestName de la table DuplicateFile est vide, le nom du fichier de destination sera le même que le nom du fichier d’origine.

Les fichiers installés par l’action DuplicateFiles sont supprimés par l’action [RemoveDuplicateFiles](removeduplicatefiles-action.md) le cas échéant.

 

 



