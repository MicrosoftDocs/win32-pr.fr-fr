---
description: La table IniLocator contient les informations nécessaires pour rechercher un fichier ou un répertoire à l’aide d’un fichier .ini ou pour rechercher une entrée de .ini particulière. le fichier .ini doit être présent dans le répertoire Microsoft Windows par défaut.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Table IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121769"
---
# <a name="inilocator-table"></a>Table IniLocator

La table IniLocator contient les informations nécessaires pour rechercher un fichier ou un répertoire à l’aide d’un fichier .ini ou pour rechercher une entrée de .ini particulière. le fichier .ini doit être présent dans le répertoire Microsoft Windows par défaut.

La table IniLocator contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificateur](identifier.md) | O   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Section     | [Text](text.md)             | N   | N        |
| Clé         | [Text](text.md)             | N   | N        |
| Champ       | [Integer](integer.md)       | N   | O        |
| Type        | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

Clé externe dans la première colonne de la [table de signatures](signature-table.md). La signature \_ représente une signature unique et est également la clé externe dans la colonne une de la table de signature. Si cette signature est présente dans la table de signatures, la recherche porte sur un fichier. Si cette clé est absente de la table de signature et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche correspond à l’entrée de .ini spécifiée par la table IniLocator. Dans le cas contraire, la recherche concerne un répertoire spécifié par la table IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom du fichier .ini.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

Nom de la section dans le fichier de .ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Valeur de clé dans la section.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Case
</dt> <dd>

Champ de la ligne de .ini. Si le champ a la valeur null ou est égal à 0, la ligne entière est lue. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Valeur qui détermine si la valeur .ini est un emplacement de fichier, un emplacement de répertoire ou une valeur de .ini brute.

Le tableau suivant répertorie les valeurs valides. Si elle est absente, le type est défini sur 1.



| Constante                      | Valeur hexadécimale | Decimal | Description           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Emplacement du répertoire. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Emplacement de fichier.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Valeur .ini brute.     |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est utilisée avec la [table AppSearch](appsearch-table.md).

Les colonnes de cette table ne sont généralement pas localisées. Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.

Le texte localisé associé à l’affichage de progression ou à la journalisation est spécifié dans la [table ActionText](actiontext-table.md).

Consultez [recherche d’applications, de fichiers, d’entrées de registre ou de .ini d’entrées de fichier existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



