---
description: La table BindImage contient des informations sur chaque fichier exécutable ou DLL qui doit être lié aux dll importées par celui-ci.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Table BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951750"
---
# <a name="bindimage-table"></a>Table BindImage

La table BindImage contient des informations sur chaque fichier exécutable ou DLL qui doit être lié aux dll importées par celui-ci.

La table BindImage contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| fichier\_ | [Identificateur](identifier.md) | O   | N        |
| Chemin d’accès   | [Chemins d’accès](paths.md)           | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé externe de la colonne de l’une des [tables de fichiers](file-table.md). Il doit s’agir d’un fichier exécutable ou d’un fichier DLL.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>D
</dt> <dd>

Liste de chemins d’accès, séparés par des points-virgules, qui représentent les chemins d’accès dans lesquels rechercher les dll importées. La liste est généralement une liste de propriétés, chaque propriété étant placée entre crochets ( \[ \] ).

</dd> </dl>

## <a name="remarks"></a>Notes

Le programme d’installation calcule l’adresse virtuelle de chaque fonction importée à partir de toutes les dll, et l’adresse virtuelle calculée est ensuite enregistrée dans la table d’adresses d’importation (IAT) de l’image d’importation.

Cette table est référencée lorsque l' [action BindImage](bindimage-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



