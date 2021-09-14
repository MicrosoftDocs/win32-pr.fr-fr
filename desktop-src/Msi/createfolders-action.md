---
description: L’action CreateFolders crée des dossiers vides pour les composants qui sont configurés pour être installés.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Action CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091909"
---
# <a name="createfolders-action"></a>Action CreateFolders

L’action CreateFolders crée des dossiers vides pour les composants qui sont configurés pour être installés. Le programme d’installation crée des dossiers pour les composants qui s’exécutent localement et qui s’exécutent à partir de la source. Les dossiers nouvellement créés sont inscrits avec l’identificateur de composant approprié.

L’action CreateFolders interroge la [table CreateFolder](createfolder-table.md) et la [table des composants](component-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action CreateFolders doit être exécutée avant l’action [InstallFiles](installfiles-action.md) ou avant toute action qui ajoute des fichiers aux dossiers.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description de la description des données d’action |
|-------|----------------------------------------|
| \[1\] | Identificateur de répertoire du dossier.        |



 

## <a name="remarks"></a>Notes

Le programme d’installation ne supprime pas automatiquement les dossiers créés par l’action CreateFolders pendant la désinstallation de l’application. Le programme d’installation supprime uniquement les dossiers si l' [action RemoveFolders](removefolders-action.md) est incluse dans la séquence d’action.

 

 



