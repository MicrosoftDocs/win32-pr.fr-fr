---
description: La table DuplicateFile contient une liste des fichiers qui doivent être dupliqués, soit vers un répertoire différent de celui du fichier d’origine, soit vers le même répertoire, mais avec un nom différent. Le fichier d’origine doit être un fichier installé par l’action InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Table DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034645"
---
# <a name="duplicatefile-table"></a>Table DuplicateFile

La table DuplicateFile contient une liste des fichiers qui doivent être dupliqués, soit vers un répertoire différent de celui du fichier d’origine, soit vers le même répertoire, mais avec un nom différent. Le fichier d’origine doit être un fichier installé par l' [action InstallFiles](installfiles-action.md).

La table DuplicateFile contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| FileKey     | [Identificateur](identifier.md) | O   | N        |
| -\_ | [Identificateur](identifier.md) | N   | N        |
| fichier\_      | [Identificateur](identifier.md) | N   | N        |
| DestName    | [Nom du fichier](filename.md)     | N   | O        |
| DestFolder  | [Identificateur](identifier.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Une clé primaire, un jeton non localisé, identifiant un enregistrement DuplicateFile unique.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe de la première colonne de la [table de composants](component-table.md). Si le composant identifié par la clé n’est pas sélectionné pour l’installation ou la suppression, aucune action n’est effectuée sur cet enregistrement DuplicateFile.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé étrangère dans la [table de fichiers](file-table.md) qui représente le fichier d’origine à dupliquer.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Nom localisable à attribuer au fichier dupliqué. Si ce champ est vide, le fichier de destination se voit attribuer le même nom que le fichier d’origine.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nom d’une propriété qui est le chemin d’accès complet à l’emplacement où le fichier dupliqué doit être copié. Si ce répertoire est le même que le répertoire contenant le fichier d’origine et que le nom du fichier dupliqué proposé est identique à l’original, aucune action n’a lieu.

</dd> </dl>

## <a name="remarks"></a>Notes

La table est traitée par l' [action DuplicateFiles](duplicatefiles-action.md) et l' [action RemoveDuplicateFiles](removeduplicatefiles-action.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 



