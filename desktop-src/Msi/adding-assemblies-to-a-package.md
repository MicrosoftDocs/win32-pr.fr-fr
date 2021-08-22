---
description: Windows les développeurs du programme d’installation peuvent utiliser les instructions de cette rubrique pour créer des packages Windows Installer qui contiennent des assemblys.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Ajout d’assemblys à un package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a96c1b8c8d9b73fedf03fceeb82be62b8457556da02334ed7a224aefc2202a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534869"
---
# <a name="adding-assemblies-to-a-package"></a>Ajout d’assemblys à un package

Windows les développeurs du programme d’installation peuvent utiliser les instructions de cette rubrique pour créer des packages Windows Installer qui contiennent des assemblys.

les indications suivantes s’appliquent aux assemblys Win32 et aux assemblys utilisés par le common language runtime de Microsoft .NET Framework.

-   un composant Windows Installer ne doit pas contenir plus d’un assembly.
-   Tous les fichiers de l’assembly doivent se trouver dans un seul composant.
-   Chaque composant qui contient un assembly doit avoir une entrée dans la table [MsiAssembly](msiassembly-table.md) .
-   Le nom fort du cache d’assembly de chaque assembly doit être créé dans la table [MsiAssemblyName](msiassemblyname-table.md) .
-   Utilisez la table de [Registre](registry-table.md) au lieu de la table de [classe](class-table.md) lorsque vous inscrivez COM Interop pour un assembly.
-   Les assemblys qui ont le même nom fort sont le même assembly. Lorsque le même assembly est installé par différentes applications, les composants qui contiennent l’assembly doivent utiliser la même valeur pour l’ID de composant dans leurs tables de [composants](component-table.md) .

> [!Note]  
> Les publications de produit identifient les assemblys qui peuvent être installés et utilisés par différentes applications. Les publications de produit n’identifient pas les assemblys privés.

 

## <a name="adding-win32-assemblies"></a>Ajout d’assemblys Win32

Utilisez les instructions suivantes lorsque vous incluez des assemblys Win32 :

-   La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly Win32 ne doit pas être null.
-   La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly de stratégie Win32 doit être le fichier manifeste.
-   La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly Win32, qui n’est pas un assembly de stratégie, ne doit pas être le fichier manifeste ou le fichier catalogue. Il doit s’agir d’un fichier différent dans l’assembly.
-   Ajoutez une ligne à la table [MsiAssemblyName](msiassemblyname-table.md) pour chaque paire nom/valeur répertoriée dans la section **assemblyIdentity** du manifeste de l’assembly Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Ajout d’assemblys utilisés avec le .NET Framework

utilisez les instructions suivantes lorsque vous incluez des assemblys que la common language runtime de la .NET Framework utilise.

-   La valeur keyPath dans la table des [composants](component-table.md) pour un composant qui contient l’assembly ne doit pas être null.
-   Quand vous installez un assembly utilisé par le common language runtime dans le Global Assembly Cache, la valeur dans la \_ colonne application de fichier de la table MsiAssembly doit être null.
-   Ajoutez une ligne à la table [MsiAssemblyName](msiassemblyname-table.md) pour chaque attribut du nom fort de l’assembly. Tous les assemblys doivent avoir les attributs Name, version et culture qui sont spécifiés dans la table MsiAssemblyName. Un attribut publicKeyToken est requis pour un assembly global. Le tableau suivant est un exemple de la table MsiAssemblyName pour un assembly global utilisé par le common language runtime.

[Table MsiAssemblyName](msiassemblyname-table.md)



| Composant  | Name           | Valeur            |
|------------|----------------|------------------|
| Composant | Name           | simple           |
| Composant | version        | 1.0.0.0          |
| Composant | Culture        | neutre          |
| Composant | publicKeyToken | 9d1ec8380f483f5a |



 

 

 



