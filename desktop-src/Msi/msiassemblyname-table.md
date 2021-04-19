---
description: La table MsiAssembly et la table MsiAssemblyName spécifient Windows Installer paramètres pour les assemblys common language runtime et les assemblys Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Table MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531752"
---
# <a name="msiassemblyname-table"></a>Table MsiAssemblyName

La [table MsiAssembly](msiassembly-table.md) et la table MsiAssemblyName spécifient Windows Installer paramètres pour les assemblys Common Language Runtime et les assemblys Win32. Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).

La table MsiAssemblyName spécifie le schéma pour les éléments d’un nom de cache d’assembly fort pour un assembly .NET Framework ou Win32. Le nom est construit en ajoutant tous les éléments avec la même clé de composant \_ . Consultez l’exemple qui suit.

Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). Pour plus d’informations, consultez l' [API d’assembly côte à côte](../sbscs/side-by-side-assembly-api.md).

La table MsiAssemblyName contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| -\_ | [Identificateur](identifier.md) | O   | N        |
| Nom        | [Text](text.md)             | O   | N        |
| Valeur       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé dans la [table de composants](component-table.md) qui spécifie le composant Windows Installer qui contient cet assembly.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de l’attribut associé à la valeur spécifiée dans la colonne valeur.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur associée au nom spécifié dans la colonne nom.

</dd> </dl>

## <a name="remarks"></a>Notes

Les informations créées dans la table MsiAssemblyName doivent correspondre aux informations contenues dans le fichier manifeste de l’assembly. Si les informations contenues dans le manifeste et la table MsiAssemblyName ne correspondent pas, la suppression de l’application peut permettre de conserver l’assembly sur l’ordinateur.

Pour les assemblys Win32, il doit y avoir une ligne dans la table MsiAssemblyName pour chacune des entrées suivantes dans le champ Name : type, Name, version, language, publicKeyToken et processorArchitecture. La valeur correspondante pour chaque nom peut être entrée dans le champ valeur. Les paires nom-valeur dans la table MsiAssemblyName doivent correspondre aux attributs type, Name, version, language, publicKeyToken et processorArchitecture dans le manifeste de l’assembly.

Pour les assemblys common language runtime privés (.NET FrameworkVersions 1,0 et 1,1), la table MsiAssemblyName doit inclure une ligne pour chacune des entrées suivantes dans le champ Nom : nom, version et culture. La valeur correspondante pour chaque nom peut être entrée dans le champ valeur.

Pour les assemblys common language runtime globaux (.NET Framework versions 1,0 et 1,1), la table MsiAssemblyName doit inclure une ligne pour chacune des entrées suivantes dans le champ Nom : nom, version, culture et PublicKeyToken. La valeur correspondante pour chaque nom peut être entrée dans le champ valeur.

Le .NET Framework version 1,1 est la version minimale qui peut être utilisée pour effectuer une mise à jour sur place d’un assembly de common language runtime global. Vous pouvez vérifier la version de la propriété [**MsiNetAssemblySupport**](msinetassemblysupport.md) . La table MsiAssemblyName doit également avoir un champ FileVersion, car ce type de mise à jour d’assembly modifie uniquement la FileVersion. Pour plus d’informations, consultez [mise à jour des assemblys](updating-assemblies.md).

Par exemple, le manifeste de l’assembly pour le composant a peut avoir une section assemblyIdentity comme suit pour un assembly Win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

Dans ce cas, remplissez la table MsiAssemblyName comme suit.



| Composant  | Nom                  | Valeur             |
|------------|-----------------------|-------------------|
| Composant | type                  | 32             |
| Composant | name                  | MS-sxstest-simple |
| Composant | version               | 1.0.0.0           |
| Composant | langage              | en                |
| Composant | publicKeyToken        | 1111111111222222  |
| Composant | processorArchitecture | x86               |



 

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
