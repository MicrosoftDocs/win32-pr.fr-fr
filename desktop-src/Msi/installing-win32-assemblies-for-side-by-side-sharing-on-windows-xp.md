---
description: La rubrique suivante décrit comment créer un package Windows Installer pour installer un assembly Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Installation d’assemblys Win32 pour le partage côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532155"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Installation d’assemblys Win32 pour le partage côte à côte

La rubrique suivante décrit comment créer un package Windows Installer pour installer un assembly Win32. Le package installe un assembly côte à côte dans le dossier WinSxS pour l’utilisation partagée de l’application. Après l’installation du package, l’assembly partagé est accessible globalement à toute application qui spécifie une dépendance sur l’assembly dans un fichier manifeste d’assembly. Le programme d’installation n’enregistre pas globalement l’assembly côte à côte sur le système.

Notez que vous pouvez installer des assemblys côte à côte partagés à l’aide de [modules de fusion](merge-modules.md).

Avant de continuer, vous devez comprendre comment créer un package Windows Installer sans assemblys. Pour obtenir un exemple de création d’une installation simple, consultez [un exemple d’installation](an-installation-example.md).

**Pour installer un assembly partagé côte à côte**

1.  Définissez un composant Windows Installer qui comprend l’assembly Win32. Ce composant peut contenir d’autres ressources qui doivent toujours être installées ou supprimées avec l’assembly. Tous les autres composants de l’application peuvent être créés de la même manière que pour une installation sans assemblys. Ajoutez une ligne à la [table des composants](component-table.md) pour le composant contenant l’assembly Win32. Entrez un [GUID](guid.md) de Windows Installer valide pour ce code de composant. N’utilisez pas le fichier manifeste comme chemin d’accès de clé pour ce composant.
2.  Ajoutez une ligne à la [table FeatureComponents](featurecomponents-table.md) en liant le composant à une fonctionnalité de Windows Installer. Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md). Une fonctionnalité de Windows Installer doit être une partie des fonctionnalités de l’application qui est reconnaissable à un utilisateur. L’assembly est activé lorsque cette fonctionnalité est sélectionnée par un utilisateur ou a généré une erreur par une application. Si l’assembly définit une fonctionnalité supplémentaire, ajoutez une ligne supplémentaire à la [table des fonctionnalités](feature-table.md) pour les attributs de la fonctionnalité. Cette étape n’est pas nécessaire lors de la création d’un module de fusion.
3.  Pour les assemblys côte à côte, les informations de liaison et d’activation, telles que les classes COM, les interfaces et les bibliothèques de types, sont stockées dans des fichiers manifestes plutôt que dans le registre. Les assemblys partagés stockent ces informations dans un manifeste d’assembly. Sur les systèmes qui prennent en charge les assemblys côte à côte, le programme d’installation ignore le traitement des informations relatives au composant entré dans la [table d’extension](extension-table.md), la [table de verbes](verb-table.md), la [table Typelib](typelib-table.md), la [table MIME](mime-table.md), la table de [classes](class-table.md), la [table ProgID](progid-table.md)et la [table AppID](appid-table.md). Les informations de liaison et d’activation peuvent être entrées dans ces tables pour être utilisées par les systèmes qui ne prennent pas en charge le partage d’assembly côte à côte.
4.  L’installation côte à côte n’inscrit pas l’assembly globalement, le programme d’installation ignore l’inscription automatique du composant si des informations d’auto-inscription ont été entrées dans la [table Selfreg](selfreg-table.md). Les informations d’auto-inscription peuvent être entrées dans la table SelfReg pour l’inscription automatique du composant sur les systèmes qui ne prennent pas en charge le partage d’assembly côte à côte.
5.  Ajoutez toutes les autres informations du Registre, en excluant la liaison et l’activation ou l’inscription automatique du composant, à la table [du Registre](registry-table.md), à la [table RemoveRegistry](removeregistry-table.md)et à la [table d’environnement](environment-table.md).
6.  Comme il s’agit d’un assembly partagé, ne générez pas de fichier. local. N’incluez pas d’informations pour ce composant dans la [table IsolatedComponent](isolatedcomponent-table.md). Le programme d’installation ignore la table IsolatedComponent pour ce composant sur les systèmes d’exploitation qui prennent en charge le partage côte à côte. Ajoutez des informations à la table IsolatedComponent si vous souhaitez que l’assembly soit privé sur les systèmes qui prennent en charge les fichiers. local.
7.  Pour activer le partage côte à côte, l’assembly Win32 doit être installé dans le dossier WinSxS. Pour ce faire, vous devez laisser la \_ colonne application de fichier de la [table MsiAssembly](msiassembly-table.md) null pour l’assembly. Cela indique au programme d’installation d’installer l’assembly dans le dossier WinSxS, plutôt que dans le dossier du composant. Ajoutez une ligne à la [table MsiAssembly](msiassembly-table.md) pour le composant qui contient l’assembly Win32. Entrez la valeur 1 dans le champ attributs de la table MsiAssembly pour spécifier qu’il s’agit d’un assembly Win32. Pour un assembly partagé, laissez le champ de l’application de fichier \_ vide. Ajoutez l' [action MsiPublishAssemblies](msipublishassemblies-action.md) à la table [InstallExecuteSequence](installexecutesequence-table.md) ou à la [table AdvtExecuteSequence](advtexecutesequence-table.md). Ajoutez l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md) à la table InstallExecuteSequence.
8.  Ajoutez des lignes à la [table MsiAssemblyName](msiassemblyname-table.md) pour le composant. Ajoutez une ligne pour chaque paire nom/valeur spécifiée dans la section assemblyIdentity du manifeste. Pour obtenir un exemple, consultez la [table MsiAssemblyName](msiassemblyname-table.md).

 

 



