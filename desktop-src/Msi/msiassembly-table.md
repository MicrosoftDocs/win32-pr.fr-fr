---
description: La table MsiAssembly spécifie Windows Installer paramètres pour les assemblys Microsoft .NET Framework et les assemblys Win32. Pour plus d’informations, consultez Installation d’assemblys dans le global assembly cache et installation d’assemblys Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Table MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953083"
---
# <a name="msiassembly-table"></a>Table MsiAssembly

La table MsiAssembly spécifie Windows Installer paramètres pour les assemblys Microsoft .NET Framework et les assemblys Win32. Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).

Sur Windows XP, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). Pour plus d’informations, consultez l' [API d’assembly côte à côte](../sbscs/side-by-side-assembly-api.md).

**Windows 2000 :** Cette fonctionnalité n’est pas prise en charge.

La table MsiAssembly contient les colonnes suivantes.



| Colonne            | Type                         | Clé | Nullable |
|-------------------|------------------------------|-----|----------|
| -\_       | [Identificateur](identifier.md) | O   | N        |
| Fonctionnalité\_         | [Identificateur](identifier.md) | N   | N        |
| Manifeste de fichier \_    | [Identificateur](identifier.md) | N   | O        |
| Application de fichier \_ | [Identificateur](identifier.md) | N   | O        |
| Attributs        | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé dans la [table de composants](component-table.md) qui spécifie le composant Windows Installer qui contient cet assembly.

La valeur de ce champ ne doit pas être définie sur null. Le champ keyPath du composant dans la [table Component](component-table.md) ne doit pas avoir la valeur null.

Pour les assemblys Win32, le chemin d’accès du composant ne peut pas être le fichier manifeste spécifié dans le manifeste de fichier \_ . Le manifeste peut être le chemin d’accès du keyPath pour un .NET Framework ou un assembly de stratégie.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé dans la [table des fonctionnalités](feature-table.md).

Lorsque l’assembly doit être installé par une installation de fonctionnalité, Windows Installer installe la fonctionnalité vers laquelle pointe ce champ.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifeste de fichier \_
</dt> <dd>

Clé externe dans la [table de fichiers](file-table.md) qui spécifie le fichier qui contient le manifeste d’un assembly .NET Framework ou d’un assembly Win32.

Pour un assembly Win32, ne spécifiez pas ce fichier comme fichier de chemin d’accès de la clé du composant dans le champ keyPath de la [table des composants](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Application de fichier \_
</dt> <dd>

Pour installer l’assembly à un emplacement privé, entrez le fichier du chemin d’accès de la clé pour le composant d’assembly dans ce champ.

Il s’agit de la valeur qui apparaît dans le champ keyPath (chemin d’accès) de la [table des composants](component-table.md). Le programme d’installation peut ensuite installer l’assembly dans la structure de répertoires du composant spécifié dans la [table de répertoires](directory-table.md). Ce champ doit avoir la valeur null si l’assembly doit être installé dans le Global Assembly Cache.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Entrez la valeur 1 (un) pour un assembly Win32. Entrez la valeur 0 (zéro) pour un assembly de .NET Framework.

Si la colonne d’attributs a la valeur NULL, le programme d’installation traite l’assembly comme un .NET Framework assembly.

</dd> </dl>

## <a name="remarks"></a>Notes

S’il existe au moins une entrée dans la table MsiAssembly, la [table InstallExecuteSequence](installexecutesequence-table.md) doit contenir l' [action MsiPublishAssemblies](msipublishassemblies-action.md)et l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Étant donné que les assemblys ne peuvent pas être restaurés une fois qu’ils ont été validés, Windows Installer utilise un processus d’installation en deux étapes. Les interfaces vers les assemblys sont créées pendant les opérations d’installation qui sont générées par l' [action MsiPublishAssemblies](msipublishassemblies-action.md).

Les assemblys ne sont pas validés avant la réussite de l’exécution de l' [action InstallFinalize](installfinalize-action.md). Cela signifie que si vous créez une action ou une ressource personnalisée qui s’appuie sur l’assembly, elle doit être séquencée après l' [action InstallFinalize](installfinalize-action.md). Par exemple, si vous devez démarrer un service qui dépend d’un assembly dans le global assembly cache (GAC), vous devez planifier le démarrage de ce service après l' [action InstallFinalize](installfinalize-action.md). Cela signifie que vous ne pouvez pas utiliser la [table ServiceControl](servicecontrol-table.md) pour démarrer le service. au lieu de cela, vous devez utiliser une action personnalisée qui est séquencée après InstallFinalize.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
