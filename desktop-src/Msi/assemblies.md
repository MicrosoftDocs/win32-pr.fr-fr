---
description: Windows Le programme d’installation peut installer, supprimer et mettre à jour les assemblys et assemblys Win32 utilisés par le common language runtime du .NET Framework Microsoft.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092557"
---
# <a name="assemblies"></a>Assemblys

Windows Le programme d’installation peut installer, supprimer et mettre à jour les assemblys et assemblys Win32 utilisés par le common language runtime du .NET Framework Microsoft. un assembly est géré par le Windows Installer en tant que composant d’installation unique. Tous les fichiers qui constituent un assembly doivent être contenus par un composant d’installation unique qui est listé dans la table des [composants](component-table.md) .

Windows le programme d’installation s’exécutant sur Windows Vista et Windows XP peut installer des assemblys côte à côte. Les assemblys côte à côte peuvent partager en toute sécurité des assemblys entre plusieurs applications et peuvent décaler les effets négatifs du partage d’assembly, tels que les conflits de DLL. Au lieu d’une seule version d’un assembly qui suppose la compatibilité descendante avec toutes les applications, le partage d’assembly côte à côte permet à plusieurs versions d’un assembly COM ou Win32 de s’exécuter simultanément sur le système. Cette fonctionnalité améliorée pour isoler les applications est une partie importante de l' .NET Framework Microsoft. Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

les sections suivantes décrivent l’utilisation des assemblys avec l’Windows Installer.

-   [Ajout d’assemblys à un package](adding-assemblies-to-a-package.md)
-   [Installation et suppression d’assemblys](installing-and-removing-assemblies.md)
-   [Mise à jour des assemblys](updating-assemblies.md)
-   [Modes de réinstallation des assemblys du Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [clés de registre de l’assembly écrites par Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)

pour plus d’informations sur l’installation des applications COM et com+ 1,0, consultez [installation d’une Application com+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md), [installation d’un composant com dans un emplacement privé](installing-a-com-component-to-a-private-location.md)et [création d’un composant com dans un Package existant privé](make-a-com-component-in-an-existing-package-private.md).

 

 
