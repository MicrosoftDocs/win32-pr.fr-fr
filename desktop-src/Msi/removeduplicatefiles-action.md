---
description: L’action RemoveDuplicateFiles supprime les fichiers installés par l’action DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Action RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7527e7bd4dc66fe4d57f8c23654f1138e781a33064fc0a4a2694987c7ccdb66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074619"
---
# <a name="removeduplicatefiles-action"></a>Action RemoveDuplicateFiles

L’action RemoveDuplicateFiles supprime les fichiers installés par l’action [DuplicateFiles](duplicatefiles-action.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RemoveDuplicateFiles doit se produire après l’action [InstallValidate](installvalidate-action.md) et avant l’action [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                    |
|-------|-----------------------------------------------|
| \[1\] | Identificateur du fichier supprimé.                   |
| \[9\] | Identificateur du répertoire contenant le fichier supprimé. |



 

## <a name="remarks"></a>Remarques

Pour supprimer un fichier dupliqué avec l' [action DuplicateFiles](duplicatefiles-action.md) à l’aide de l’action RemoveDuplicateFiles, vous devez sélectionner le composant associé à l’entrée du fichier dans la table DuplicateFile pour la suppression.

Utilisez la colonne DestFolder de la [table DuplicateFile](duplicatefile-table.md) pour spécifier le nom de la propriété dont la valeur identifie le dossier de destination.

 

 



