---
description: La table de polices contient les informations relatives à l’inscription des fichiers de polices dans le système.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tableau des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021718"
---
# <a name="font-table"></a>Tableau des polices

La table de polices contient les informations relatives à l’inscription des fichiers de polices dans le système.

La table de polices contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| fichier\_    | [Identificateur](identifier.md) | O   | N        |
| FontTitle | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé externe dans l’entrée de [table de fichiers](file-table.md) pour le fichier de police. Il est recommandé que le composant contenant le fichier de police ait le FontsFolder spécifié dans la \_ colonne répertoire de la [table des composants](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nom de la police. Il est recommandé de conserver cette colonne null pour les polices TrueType et les collections TrueType, car le programme d’installation peut inscrire la police après avoir lu le titre de police correct à partir du fichier de police. Si le nom de la police est entré, il doit être identique au titre de police du fichier de police. Vous devez spécifier un titre pour les polices qui n’ont pas de noms incorporés, tels que les fichiers. fon.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est référencée lorsque l' [action RegisterFonts](registerfonts-action.md) ou l' [action UnregisterFonts](unregisterfonts-action.md) est exécutée.

Si le champ FontTitle est laissé null, le nom de la police est lu directement à partir du fichier de police spécifié. Si le nom de police enregistré dans le champ FontTitle diffère du nom de police interne enregistré dans le fichier de police, la police est inscrite deux fois par l' [action RegisterFonts](registerfonts-action.md).

Les fichiers de polices ne doivent pas être créés avec un ID de langue, car les polices n’ont pas de ressource d’ID de langue incorporée. Par conséquent, la colonne Language de la [table file](file-table.md) doit être laissée null pour les fichiers de police.

Étant donné que le programme d’installation ne prend pas en compte les fichiers de polices par défaut, les fichiers de polices préexistants peuvent être supprimés avec leur composant lors de la désinstallation d’une application. Pour vous assurer qu’un fichier de polices n’est pas supprimé, les auteurs peuvent définir les indicateurs de bits **msidbComponentAttributesSharedDllRefCount** ou **msidbComponentAttributesPermanent** dans la colonne attributs de la table des composants MSI de la table des composants \_ \_ \_ pour le composant contenant le fichier de police.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



