---
description: La table RemoveRegistry contient les informations de registre que l’application doit supprimer du Registre système.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Table RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314879"
---
# <a name="removeregistry-table"></a>Table RemoveRegistry

La table RemoveRegistry contient les informations de registre que l’application doit supprimer du Registre système.

La table RemoveRegistry contient les colonnes suivantes.



| Colonne         | Type                         | Clé | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificateur](identifier.md) | O   | N        |
| Root           | [Integer](integer.md)       | N   | N        |
| Clé            | [RegPath](regpath.md)       | N   | N        |
| Nom           | [Correct](formatted.md)   | N   | O        |
| Composant\_    | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

Clé de cette table.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes
</dt> <dd>

Clé racine prédéfinie pour la valeur de registre.



| Constante                          | Valeur hexadécimale | Decimal | Clé racine                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (aucun)                            | \- 0x001    | -1      | **HKEY \_ Le \_** programme d’installation de l’utilisateur actuel définit cette clé lors de l’installation par utilisateur.<br/>                                                                                                                    |
| (aucun)                            | -0x001      | -1      | **HKEY \_ Le \_** programme d’installation de l’ordinateur local définit cette clé lors de l’installation de tous les utilisateurs avec [**ALLUSERS**](allusers.md) défini sur 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ racine** le programme d’installation supprime la valeur de la ruche des **\\ \\ classes logicielles HKCU** lors des installations dans le contexte d' [installation](installation-context.md)par utilisateur et par ordinateur.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ local \_ machine**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **HKEY, \_ utilisateurs**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Clé localisable pour la valeur de registre.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de la valeur de Registre localisable.

La chaîne suivante dans la colonne Name a une signification spéciale.



| String | Signification                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | La clé doit être supprimée, le cas échéant, avec toutes ses valeurs et ses sous-clés, lorsque le composant est installé. |



 

Notez que la [table de Registre](registry-table.md) doit être utilisée pour créer ou supprimer une clé de registre lors de la suppression du composant.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle la suppression de la valeur de registre.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les informations de Registre sont supprimées du Registre système lorsque le composant correspondant a été sélectionné pour être installé localement ou exécuté à partir de la source.

Cette table est référencée lorsque l' [action RemoveRegistryValues](removeregistryvalues-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




