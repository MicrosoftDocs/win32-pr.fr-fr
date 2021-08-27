---
description: L’action RemoveFolders supprime tous les dossiers liés à des composants définis pour être supprimés ou exécutés à partir de la source. Ces dossiers sont supprimés uniquement s’ils sont vides. Si un dossier est supprimé, il est désinscrit avec l’identificateur de composant approprié.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Action RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b476de044ef48b50120575a8d6991d27bf063dec37a026a2f5d2ea0e604abee0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082539"
---
# <a name="removefolders-action"></a>Action RemoveFolders

L’action RemoveFolders supprime tous les dossiers liés à des composants définis pour être supprimés ou exécutés à partir de la source. Ces dossiers sont supprimés uniquement s’ils sont vides. Si un dossier est supprimé, il est désinscrit avec l’identificateur de composant approprié.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RemoveFolders doit venir après l’action [RemoveFiles](removefiles-action.md) ou toute action qui peut supprimer des fichiers de dossiers.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action    |
|-------|-------------------------------|
| \[1\] | Identificateur du dossier supprimé. |



 

## <a name="remarks"></a>Remarques

Le programme d’installation ne supprime pas automatiquement les dossiers créés par l' [action CreateFolders](createfolders-action.md) pendant la désinstallation de l’application. Le programme d’installation doit être invité à supprimer ces dossiers en créant l’action RemoveFolders dans la séquence d’action.

Pour spécifier le nom et l’emplacement du dossier, utilisez la \_ colonne Directory de la [table CreateFolder](createfolder-table.md). Chaque nom de dossier dans la table CreateFolder est supposé être une propriété qui définit l’emplacement du dossier.

Pour spécifier le composant propriétaire du dossier, utilisez la colonne ComponentId de la [table des composants](component-table.md).

 

 



