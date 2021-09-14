---
description: La table RegLocator contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire à l’aide du Registre, ou à la recherche d’une entrée de Registre particulière. Cette table contient les colonnes suivantes.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Table RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009678"
---
# <a name="reglocator-table"></a>Table RegLocator

La table RegLocator contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire à l’aide du Registre, ou à la recherche d’une entrée de Registre particulière. Cette table contient les colonnes suivantes.



| Colonne      | Type                         | Clé : | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificateur](identifier.md) | O   | N        |
| Root        | [Integer](integer.md)       | N   | N        |
| Clé :         | [RegPath](regpath.md)       | N   | N        |
| Name        | [Correct](formatted.md)   | N   | O        |
| Type        | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

La valeur du champ signature \_ représente une signature unique qui est une clé externe dans la colonne une de la table de [signature](signature-table.md) . Si cette signature est présente dans la table de signatures, la recherche porte sur un fichier. Si cette signature est absente de la table de signature et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche porte sur le nom de la clé de Registre désignée par la table RegLocator. Dans le cas contraire, la recherche concerne un répertoire vers lequel pointe la table RegLocator.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes
</dt> <dd>

Clé racine prédéfinie pour la valeur de registre.



| Constante                          | Valeur hexadécimale | Decimal | Clé racine             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | \_racine des classes HKEY \_  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | HKEY \_ Current \_ User  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | HKEY \_ local \_ machine |
| **msidbRegistryRootUsers**        | 0x003       | 3       | HKEY, \_ utilisateurs          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Clé pour la valeur de registre.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de la valeur de Registre. Si cette valeur est null, la valeur de la valeur sans nom ou par défaut de la clé, le cas échéant, est récupérée.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Valeur qui détermine si la valeur de Registre est un nom de fichier, un emplacement de répertoire ou une valeur de Registre brute.

Le tableau suivant répertorie les valeurs valides. Définissez l’une des trois premières valeurs et **msidbLocatorType64bit** si nécessaire. Si l’entrée de ce champ est absente, le type est défini sur 1.



| Constante                      | Valeur hexadécimale | Decimal | Description                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Le chemin d’accès de la clé est un répertoire.                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Le chemin d’accès de la clé est un nom de fichier.                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Le chemin d’accès de la clé est une valeur de registre.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Définissez ce bit pour que le programme d’installation recherche la partie 64 bits du Registre. Ne définissez pas ce bit pour que le programme d’installation recherche la partie 32 bits du Registre. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez que si la valeur du champ de type est **msidbLocatorTypeRawValue**, le programme d’installation définit la valeur de registre de la propriété spécifiée dans le champ de propriété de la table [AppSearch](appsearch-table.md) . Le programme d’installation ajoute un préfixe à la valeur de Registre qui identifie le type de valeur de registre. Pour plus d’informations sur les types de valeurs de Registre, consultez [types de valeur de Registre](../sysinfo/registry-value-types.md).



| Type de registre   | Préfixe ajouté par le programme d’installation                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| SZ de REG \_         | Aucun, mais si le premier caractère de la valeur de Registre est \# , le programme d’installation échappe le caractère en préfixant un autre caractère \# .            |
| DWORD           | " \# " éventuellement suivi de' + 'ou'-'                                                                                                  |
| REG \_ développer \_ SZ | "\#%"                                                                                                                                   |
| REG \_ multiple \_ SZ  | Null. Le programme d’installation définit la propriété sur une valeur qui commence par null et se termine par une valeur null.                                          |
| \_fichier binaire reg     | « \# x » dans le cas de reg \_ Binary, le programme d’installation convertit et enregistre chaque chiffre hexadécimal (grignoter) sous la forme d’un caractère ASCII préfixé par « \# x ». |



 

En règle générale, les colonnes de cette table ne sont pas localisées. Si un auteur décide de rechercher des produits dans plusieurs langues, il doit y avoir une entrée distincte incluse dans le tableau pour chaque langue.

Notez qu’il n’est pas possible d’utiliser la table RegLocator pour vérifier uniquement la présence de la clé. Toutefois, vous pouvez rechercher la valeur par défaut d’une clé et récupérer sa valeur si elle n’est pas vide.

Pour plus d’informations, consultez [recherche d’applications, de fichiers, d’entrées de registre ou de .ini entrées de fichier existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
