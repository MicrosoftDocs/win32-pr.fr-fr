---
description: La table de correctifs spécifie le fichier qui doit recevoir un correctif particulier et l’emplacement physique des fichiers de correctifs sur les images de support.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Table des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123622"
---
# <a name="patch-table"></a>Table des correctifs

La table de correctifs spécifie le fichier qui doit recevoir un correctif particulier et l’emplacement physique des fichiers de correctifs sur les images de support.

La table des correctifs contient les colonnes suivantes.



| Colonne      | Type                               | Clé | Nullable |
|-------------|------------------------------------|-----|----------|
| fichier\_      | [Identificateur](identifier.md)       | O   | N        |
| Séquence    | [Integer](integer.md)             | O   | N        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | N   | N        |
| Attributs  | [Integer](integer.md)             | N   | N        |
| En-tête      | [Binaire](binary.md)               | N   | O        |
| StreamRef\_ | [Identificateur](identifier.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Le correctif est appliqué au fichier spécifié par l’identificateur dans cette colonne. Il s’agit d’une clé primaire pour la table et il s’agit d’une clé étrangère de la [table de fichiers](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Il s’agit de la position du fichier correctif dans l’ordre séquentiel des fichiers sur les images de média. L’ordre des séquences doit correspondre à l’ordre des fichiers dans le fichier CAB du package correctif. Il s’agit d’une clé primaire pour cette table. la limite maximale est de 32767 fichiers. pour créer un package de Windows Installer avec d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

Cette colonne indique la taille du correctif en octets écrits sous la forme d’un entier long.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Entier contenant des indicateurs binaires représentant des attributs de correctif. Insérez la valeur 1 dans cette colonne pour indiquer que l’échec de l’application de ce correctif logiciel n’est pas une erreur irrécupérable.



| Constante                         | Valeur hexadécimale | Decimal | Description                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (aucun)                           | 0x000       | 0       | L’échec de l’application de ce correctif est une erreur irrécupérable.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Indique que l’échec de l’application de ce correctif n’est pas une erreur irrécupérable. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre
</dt> <dd>

Cette colonne est l’en-tête de correctif de flux binaire utilisé pour la validation des correctifs. Cette colonne doit avoir la valeur null si la \_ colonne StreamRef n’a pas la valeur null. Dans ce cas, le flux d’en-tête de correctif est stocké dans la [table MsiPatchHeaders](msipatchheaders-table.md) pour surmonter la limitation de nom de flux décrite dans [restrictions OLE sur flux](ole-limitations-on-streams.md).

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Clé externe dans la table MsiPatchHeaders spécifiant la ligne qui contient le flux d’en-tête de correctif.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est traitée par l' [action PatchFiles](patchfiles-action.md). Il est généralement ajouté au package d’installation par une transformation à partir d’un package de correctifs. En général, il n’est pas directement créé dans un package d’installation.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



