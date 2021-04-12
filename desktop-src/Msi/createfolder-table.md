---
description: La table CreateFolder contient des références à des dossiers qui doivent être créés explicitement pour un composant particulier.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Table CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204015"
---
# <a name="createfolder-table"></a>Table CreateFolder

La table CreateFolder contient des références à des dossiers qui doivent être créés explicitement pour un composant particulier.

La table CreateFolder contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Répertoire\_ | [Identificateur](identifier.md) | O   | N        |
| -\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Clé externe dans la première colonne de la [table de répertoires](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table des composants](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les dossiers de ce tableau sont créés lors de l’installation du composant. Une tentative est effectuée pour supprimer ces dossiers uniquement lorsque le composant est désinstallé ou déplacé vers l’exécution à partir de la source. Aucune suppression automatique n’est déclenchée si les dossiers sont vides. En revanche, les dossiers créés par le programme d’installation mais non répertoriés dans ce tableau sont supprimés lorsqu’ils sont vides.

Étant donné que les dossiers créés par le programme d’installation sont supprimés lorsqu’ils sont vides, vous devez créer une entrée dans la table CreateFolder pour installer un composant qui se compose d’un dossier vide.

Cette table est référencée lorsque l’action [CreateFolders](createfolders-action.md) ou l’action [RemoveFolders](removefolders-action.md) est appelée.

Pour plus d’informations sur la sécurisation d’un dossier, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) et la [table LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



