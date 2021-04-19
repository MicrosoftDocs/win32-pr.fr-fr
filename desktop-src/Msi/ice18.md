---
description: ICE18 valide que tous les répertoires vides utilisés comme chemin de clé pour un composant sont répertoriés dans la table CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524487"
---
# <a name="ice18"></a>ICE18

ICE18 valide que tous les répertoires vides utilisés comme chemin de clé pour un composant sont répertoriés dans la [table CreateFolder](createfolder-table.md).

Si la colonne keyPath de la [table Component](component-table.md) est null, cela signifie que le répertoire figurant dans la \_ colonne Directory est le chemin d’accès de clé de ce composant. Étant donné que les dossiers créés par le programme d’installation sont supprimés lorsqu’ils sont vides, ce dossier doit être répertorié dans la [table CreateFolder](createfolder-table.md) pour empêcher le programme d’installation de tenter de s’installer à chaque fois.

Ne faites pas du répertoire SystemFolder le chemin d’accès de clé d’un composant. Étant donné que ce dossier est présent sur chaque système d’exploitation, le programme d’installation détecte toujours le chemin d’accès de la clé, que le composant soit présent ou non. Dans ce cas, le chemin d’accès de la clé doit être un fichier, une entrée de registre ou une source de données ODBC.

Lorsque vous effectuez une validation, ICE18 vérifie d’abord si les conditions suivantes sont vraies :

-   La colonne keyPath de la [table Component](component-table.md) contient une valeur null.
-   Aucun fichier n’est répertorié pour le composant dans la [table file](file-table.md).
-   Il n’existe aucun fichier pour le composant répertorié dans la [table RemoveFile](removefile-table.md) et que la valeur de DirProperty est identique à celle \_ de la colonne Directory de la [table Component](component-table.md).
-   Il n’existe aucun fichier pour le composant répertorié dans la [table DuplicateFile](duplicatefile-table.md) et que la valeur de DestFolder est identique à celle \_ de la colonne Directory de la [table Component](component-table.md).
-   Il n’y a pas de fichiers pour le composant répertorié dans la [table MoveFile](movefile-table.md) et que la valeur de DestFolder est identique à celle \_ de la colonne Directory de la [table des composants](component-table.md).

Si la valeur est true, ICE18 valide les éléments suivants :

-   Que la \_ colonne Component de la [table CreateFolder](createfolder-table.md) a la même valeur que la colonne Component de la [table Component](component-table.md).
-   Que la \_ colonne Directory de la table CreateFolder a la même valeur que la \_ colonne Directory de la [table Component](component-table.md).

## <a name="result"></a>Résultats

ICE18 publie un message d’erreur si le package d’installation spécifie un répertoire comme chemin de clé pour le composant qui n’est pas listé dans la [table CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



