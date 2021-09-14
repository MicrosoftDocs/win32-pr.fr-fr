---
description: La table de registre contient les informations de registre que l’application doit définir dans le registre système.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Table du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009682"
---
# <a name="registry-table"></a>Table du Registre

La table de registre contient les informations de registre que l’application doit définir dans le registre système.

La table du registre contient les colonnes suivantes.



| Colonne      | Type                         | Clé : | Nullable |
|-------------|------------------------------|-----|----------|
| Registre    | [Identificateur](identifier.md) | O   | N        |
| Root        | [Integer](integer.md)       | N   | N        |
| Clé :         | [RegPath](regpath.md)       | N   | N        |
| Name        | [Correct](formatted.md)   | N   | O        |
| Valeur       | [Correct](formatted.md)   | N   | O        |
| Composant\_ | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Du
</dt> <dd>

Clé primaire utilisée pour identifier un enregistrement de registre.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes
</dt> <dd>

Clé racine prédéfinie pour la valeur de registre. Entrez la valeur-1 dans ce champ pour que la clé racine dépende du type d’installation. Entrez l’une des autres valeurs du tableau suivant pour forcer l’écriture de la valeur de Registre sous une clé racine particulière.



| Constante                          | Valeur hexadécimale | Decimal | Clé racine                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (aucun)                            | \- 0x001    | -1      | S’il s’agit d’une installation par utilisateur, la valeur de Registre est écrite sous **HKEY \_ Current \_ User**. S’il s’agit d’une installation par ordinateur, la valeur de Registre est écrite sous **HKEY \_ local \_ machine**. Notez qu’une installation par ordinateur est spécifiée en affectant à la propriété [**ALLUSERS**](allusers.md) la valeur 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ racine** le programme d’installation écrit ou supprime la valeur de la ruche des **\\ \\ classes logicielles HKCU** lors de l’installation dans le [contexte d’installation](installation-context.md)par utilisateur.<br/> Le programme d’installation écrit ou supprime la valeur de la ruche des **\\ \\ classes logicielles HKLM** lors des installations par ordinateur.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ local \_ machine**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **HKEY, \_ utilisateurs**                                                                                                                                                                                                                                                                                                                              |



 

Notez qu’il est recommandé que les entrées de Registre écrites dans la ruche **HKCU** fassent référence à un composant dont le bit RegistryKeyPath est défini dans la colonne attributs de la [table des composants](component-table.md). Cela permet de s’assurer que le programme d’installation écrit les entrées de Registre nécessaires lorsqu’il y a plusieurs utilisateurs sur le même ordinateur.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Clé localisable pour la valeur de registre.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne contient le nom de la valeur de Registre (localisable). Si la valeur est null, les données entrées dans la colonne valeur sont écrites dans la clé de Registre par défaut.

Si la colonne value est null, les chaînes affichées dans le tableau suivant de la colonne Name ont une signification spéciale.



| String | Signification                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | La clé doit être créée, si elle est absente, lorsque le composant est installé.                                                                                                                            |
| \-     | La clé doit être supprimée, le cas échéant, avec toutes ses valeurs et ses sous-clés, lorsque le composant est désinstallé.                                                                                     |
| \*     | La clé doit être créée, si elle est absente, lorsque le composant est installé. En outre, la clé doit être supprimée, le cas échéant, avec toutes ses valeurs et sous-clés, lorsque le composant est désinstallé. |



 

Notez que la [table RemoveRegistry](removeregistry-table.md) doit être utilisée si une clé de Registre installée doit être supprimée, avec ses valeurs et ses sous-clés, lors de l’installation du composant.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Cette colonne est la valeur de Registre localisable. Le champ est [mis en forme](formatted.md). Si la valeur est attachée à l’un des préfixes suivants (par exemple \# % , *valeur*), la valeur est interprétée comme décrit dans le tableau. Notez que chaque préfixe commence par un signe dièse ( \# ). Si la valeur commence par au moins deux signes dièse consécutifs ( \# ), la première \# est ignorée et la valeur est interprétée et stockée en tant que chaîne.



| Préfixe | Signification                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#x    | La valeur est interprétée et stockée sous la forme d’une valeur hexadécimale (REG \_ Binary).      |
| \#%    | La valeur est interprétée et stockée sous la forme d’une chaîne extensible (REG \_ expand \_ SZ). |
| \#     | La valeur est interprétée et stockée sous la forme d’un entier (REG \_ DWORD).                |



 

-   Si la valeur contient le tilde \[ ~ \] de séquence, la valeur est interprétée comme une liste de chaînes délimitée par des valeurs null (reg \_ \_ multisz). Par exemple, pour spécifier une liste contenant les trois chaînes a, b et c, utilisez « a \[ ~ \] b \[ ~ \] c ».
-   La séquence \[ ~ \] dans la valeur sépare les chaînes individuelles et est interprétée et stockée en tant que caractère null.
-   Si a \[ ~ \] précède la liste de chaînes, les chaînes doivent être ajoutées à toutes les chaînes de valeurs de Registre existantes. Si une chaîne d’ajout figure déjà dans la valeur de Registre, l’occurrence d’origine de la chaîne est supprimée.
-   Si un \[ ~ \] suit la fin de la liste de chaînes, les chaînes doivent être ajoutées à toute chaîne de valeur de Registre existante. Si une chaîne de préattente se trouve déjà dans la valeur de Registre, l’occurrence d’origine de la chaîne est supprimée.
-   Si un \[ ~ \] est à la fois au début et à la fin ou au début ou à la fin de la liste de chaînes, les chaînes remplacent les chaînes de valeur de Registre existantes.
-   Dans le cas contraire, la valeur est interprétée et stockée sous la forme d’une chaîne (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle l’installation de la valeur de registre.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les actions [WriteRegistryValues](writeregistryvalues-action.md) et [RemoveRegistryValues](removeregistryvalues-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

Les informations de Registre sont écrites dans le registre système lorsque le composant correspondant a été sélectionné pour être installé localement ou exécuté à partir de la source.

Notez que le programme d’installation supprime une clé de registre après avoir supprimé la dernière valeur ou sous-clé sous la clé. Pour empêcher une clé de Registre vide d’être supprimée lors de la désinstallation de, écrivez une valeur factice sous la clé que vous devez conserver et entrez + dans la colonne nom. Si \* se trouve dans la colonne nom, la clé est supprimée, avec toutes ses valeurs et ses sous-clés, lorsque le composant est supprimé.

Une action personnalisée peut être utilisée pour ajouter des lignes à la table du Registre pendant une transaction d’installation, de désinstallation ou de réparation. Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours. L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires. L’action personnalisée doit précéder les actions [RemoveRegistryValues](removeregistryvalues-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) dans la séquence d’action.

Pour plus d’informations sur la sécurisation d’une clé de Registre, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) et la [table LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




