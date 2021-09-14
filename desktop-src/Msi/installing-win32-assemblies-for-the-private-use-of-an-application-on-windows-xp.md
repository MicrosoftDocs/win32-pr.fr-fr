---
description: la procédure de cette rubrique indique comment créer un package Windows Installer pour installer un assembly Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: installation d’assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012037"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>installation d’assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP

la procédure de cette rubrique indique comment créer un package Windows Installer pour installer un assembly Win32. Le package installe l’assembly et un fichier manifeste d’application dans un dossier créé que l’application utilise. Le manifeste d’application spécifie la dépendance de l’application sur l’assembly privé. Une fois le package installé, l’assembly privé est disponible pour l’utilisation exclusive de l’application. La dépendance d’assembly spécifiée dans le manifeste de l’application remplace (pour cette application) toutes les autres dépendances d’assembly globales spécifiées dans les fichiers manifeste de l’assembly.

avant de continuer, il est judicieux de comprendre comment créer un package Windows Installer sans assemblys. Pour plus d’informations, consultez [un exemple d’installation](an-installation-example.md).

**pour installer un assembly privé sur Windows XP**

1.  définissez un composant Windows Installer qui comprend l’assembly Win32 et le fichier manifeste de l’application. Ce composant peut contenir d’autres ressources qui doivent toujours être installées ou supprimées avec l’assembly. Les étapes restantes de cette procédure décrivent comment créer la base de données d’installation pour installer ce composant.
2.  Ajoutez une ligne à la [table des composants](component-table.md) pour le composant qui contient l’assembly Win32 et le fichier manifeste de l’application. entrez un [GUID](guid.md) de Windows Installer valide pour ce code de composant. Pour plus d’informations, consultez [modification du code du composant](changing-the-component-code.md) et [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md)
3.  Le programme d’installation copie le fichier manifeste de l’assembly dans le dossier qui contient le fichier spécifié dans le \_ champ application de fichier de la [table MsiAssembly](msiassembly-table.md).
4.  ajoutez une ligne à la [table FeatureComponents](featurecomponents-table.md) en liant le composant à une fonctionnalité de Windows Installer. Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md). une fonctionnalité de Windows Installer doit être une partie des fonctionnalités d’application qu’un utilisateur peut reconnaître. L’assembly est activé lorsque cette fonctionnalité est sélectionnée par un utilisateur ou a généré une erreur par une application. Si l’assembly définit une fonctionnalité supplémentaire, ajoutez une ligne supplémentaire à la [table des fonctionnalités](feature-table.md) pour les attributs de fonctionnalité. Cette étape n’est pas requise en cas de création d’un module de fusion.
5.  Pour les assemblys côte à côte, les informations de liaison et d’activation, par exemple, les classes COM, les interfaces et les bibliothèques de types, sont stockées dans des fichiers manifeste plutôt que dans le registre. Les assemblys privés stockent ces informations dans un manifeste d’assembly. Sur les systèmes qui prennent en charge les assemblys côte à côte, le programme d’installation ignore le traitement des informations relatives au composant qui est entré dans la [table d’extension](extension-table.md), la [table de verbes](verb-table.md), la [table Typelib](typelib-table.md), la [table MIME](mime-table.md), la table de [classes](class-table.md), la [table ProgID](progid-table.md)et la [table AppID](appid-table.md). Les informations de liaison et d’activation peuvent être entrées dans les tables pour être utilisées par les systèmes qui ne prennent pas en charge le partage d’assembly côte à côte.
6.  L’installation côte à côte n’inscrit pas l’assembly globalement. Le programme d’installation ignore l’inscription automatique du composant si des informations d’auto-inscription sont entrées dans la [table Selfreg](selfreg-table.md). Les informations d’auto-inscription peuvent être entrées dans la table SelfReg pour l’inscription automatique du composant sur les systèmes qui ne prennent pas en charge le partage d’assembly côte à côte.
7.  Ajoutez toutes les autres informations du Registre, en excluant la liaison et l’activation ou l’inscription automatique du composant, à la table [du Registre](registry-table.md), à la [table RemoveRegistry](removeregistry-table.md)et à la [table d’environnement](environment-table.md).
8.  Le programme d’installation ignore la [table IsolatedComponent](isolatedcomponent-table.md) pour ce composant sur les systèmes d’exploitation qui prennent en charge le partage côte à côte. Entrez les informations dans cette table si vous souhaitez que l’assembly soit privé sur les systèmes qui prennent en charge des fichiers locaux.
9.  Ajoutez une ligne à la [table MsiAssembly](msiassembly-table.md) pour le composant qui contient l’assembly Win32. Entrez la valeur 1 dans le champ attributs de la table MsiAssembly pour spécifier qu’il s’agit d’un assembly Win32. Entrez la clé de fichier de l’assembly privé dans le \_ champ application de fichier de la [table MsiAssembly](msiassembly-table.md). Ajoutez l' [action MsiPublishAssemblies](msipublishassemblies-action.md) à la table [InstallExecuteSequence](installexecutesequence-table.md) ou à la [table AdvtExecuteSequence](advtexecutesequence-table.md). Ajoutez l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md) à la table InstallExecuteSequence. Créez un dossier pour l’assembly et le fichier manifeste dans la [table de répertoires](directory-table.md). Ce dossier doit se trouver dans le répertoire racine de l’application et contenir le fichier spécifié dans le \_ champ application de fichier de la [table MsiAssembly](msiassembly-table.md). Pendant l’installation de l’application, le programme d’installation résout la [table de répertoire](directory-table.md) pour le chemin d’accès à ce dossier. Pour plus d’informations, consultez [utilisation de la table des répertoires](using-the-directory-table.md).
10. Ajoutez des lignes à la [table MsiAssemblyName](msiassemblyname-table.md) pour le composant. Ajoutez une ligne pour chaque paire nom/valeur spécifiée dans la section assemblyIdentity du manifeste. Pour plus d’informations, consultez la [table MsiAssemblyName](msiassemblyname-table.md).

 

 



