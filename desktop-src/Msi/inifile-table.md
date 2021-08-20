---
description: La table IniFile contient les informations .ini que l’application doit définir dans un fichier .ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Table IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd12c02fa0123ac9e1a763b4e725681e6c6b1d51a331a1efea9916b5ac4cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946566"
---
# <a name="inifile-table"></a>Table IniFile

La table IniFile contient les informations .ini que l’application doit définir dans un fichier .ini.

La table IniFile contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificateur](identifier.md) | O   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [Identificateur](identifier.md) | N   | O        |
| Section     | [Correct](formatted.md)   | N   | N        |
| Clé         | [Correct](formatted.md)   | N   | N        |
| Valeur       | [Correct](formatted.md)   | N   | N        |
| Action      | [Integer](integer.md)       | N   | N        |
| Composant\_ | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

Clé de cette table.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom localisable du fichier .ini dans lequel les informations doivent être écrites.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nom d’une propriété ayant une valeur qui correspond au chemin d’accès complet du dossier contenant le fichier .ini. La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet. Si ce champ est laissé vide, le fichier .ini est créé dans le dossier avec le chemin d’accès complet spécifié par la propriété [**WindowsFolder**](windowsfolder.md) .

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

Section du fichier de .ini localisable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Clé de fichier .ini localisable dans la section.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur localisable à écrire.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Type de modification à effectuer.



| Constante                         | Valeur hexadécimale | Decimal | Modification                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Crée ou met à jour une entrée de .ini.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Crée une entrée de .ini uniquement si l’entrée n’existe pas déjà.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Crée une entrée ou ajoute une nouvelle valeur séparée par des virgules à une entrée existante. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle l’installation de la valeur de .ini.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les informations du fichier de .ini sont écrites lorsque le composant correspondant a été sélectionné pour être installé en local ou exécuté à partir de la source.

Cette table est référencée lorsque l' [action WriteIniValues](writeinivalues-action.md) ou l' [action RemoveIniValues](removeinivalues-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



