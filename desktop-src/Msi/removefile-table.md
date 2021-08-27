---
description: La table RemoveFile contient une liste de fichiers à supprimer par l’action RemoveFiles. L’affectation de la valeur null à la colonne FileName de cette table prend en charge la suppression des dossiers vides.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Table RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082599"
---
# <a name="removefile-table"></a>Table RemoveFile

La table RemoveFile contient une liste de fichiers à supprimer par l' [action RemoveFiles](removefiles-action.md). L’affectation de la valeur null à la colonne FileName de cette table prend en charge la suppression des dossiers vides.

La table RemoveFile contient les colonnes suivantes.



| Colonne      | Type                                     | Clé | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identificateur](identifier.md)             | O   | N        |
| Composant\_ | [Identificateur](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | O        |
| DirProperty | [Identificateur](identifier.md)             | N   | N        |
| InstallMode | [Integer](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Clé primaire utilisée pour identifier cette entrée de table particulière.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe première colonne de la [table des composants](component-table.md). Ce champ fait référence au composant qui contrôle le fichier à supprimer.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Cette colonne contient le nom localisable du fichier à supprimer. Si cette colonne est null, le dossier spécifié est supprimé s’il est vide. Tous les fichiers qui correspondent au caractère générique seront supprimés du répertoire spécifié.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nom d’une propriété dont la valeur est supposée correspondre au chemin d’accès complet au dossier du fichier à supprimer. La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Il doit s’agir de l’une des valeurs suivantes.



| Constante                                | Valeur hexadécimale | Decimal | Description                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Supprimer uniquement lorsque le composant associé est en cours d’installation (msiInstallStateLocal ou msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Supprimer uniquement lorsque le composant associé est en cours de suppression (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Supprimez dans l’un des cas ci-dessus.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Les références de fichier de cette table sont traitées par l' [action RemoveFiles](removefiles-action.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



