---
description: Windows Installer pouvez installer, supprimer et mettre à jour les assemblys et assemblys Win32 utilisés par le common language runtime de l’infrastructure Microsoft .NET.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531907"
---
# <a name="assemblies"></a>Assemblys

Windows Installer pouvez installer, supprimer et mettre à jour les assemblys et assemblys Win32 utilisés par le common language runtime de l’infrastructure Microsoft .NET. Un assembly est géré par le Windows Installer en tant que composant d’installation unique. Tous les fichiers qui constituent un assembly doivent être contenus par un composant d’installation unique qui est listé dans la table des [composants](component-table.md) .

Les Windows Installer s’exécutant sur Windows Vista et Windows XP peuvent installer des assemblys côte à côte. Les assemblys côte à côte peuvent partager en toute sécurité des assemblys entre plusieurs applications et peuvent décaler les effets négatifs du partage d’assembly, tels que les conflits de DLL. Au lieu d’une seule version d’un assembly qui suppose la compatibilité descendante avec toutes les applications, le partage d’assembly côte à côte permet à plusieurs versions d’un assembly COM ou Win32 de s’exécuter simultanément sur le système. Cette fonctionnalité améliorée pour isoler les applications est une partie importante de l’infrastructure Microsoft .NET. Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Les sections suivantes décrivent l’utilisation des assemblys avec l’Windows Installer.

-   [Ajout d’assemblys à un package](adding-assemblies-to-a-package.md)
-   [Installation et suppression d’assemblys](installing-and-removing-assemblies.md)
-   [Mise à jour des assemblys](updating-assemblies.md)
-   [Modes de réinstallation des assemblys du Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Clés de registre de l’assembly écrites par Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)

Pour plus d’informations sur l’installation des applications COM et COM+ 1,0, consultez [installation d’une application com+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md), [installation d’un composant COM dans un emplacement privé](installing-a-com-component-to-a-private-location.md)et [création d’un composant COM dans un package existant privé](make-a-com-component-in-an-existing-package-private.md).

 

 
