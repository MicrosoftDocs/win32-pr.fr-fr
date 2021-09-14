---
description: installez les assemblys Win32 en les faisant un composant de Microsoft Windows Installer package qui installe ou met à jour votre application.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installation d’assemblys Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121730"
---
# <a name="installation-of-win32-assemblies"></a>Installation d’assemblys Win32

installez les assemblys Win32 en les faisant un composant de Microsoft Windows Installer package qui installe ou met à jour votre application. Lorsque vous créez la table [MsiAssembly](msiassembly-table.md) et la [table MsiAssemblyName](msiassemblyname-table.md), cela identifie le composant dans la \_ colonne composant en tant qu’assembly. Le programme d’installation va définir la propriété [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) sur la version de fichier de Sxs.dll sur les systèmes d’exploitation qui peuvent prendre en charge les assemblys Win32 et ne pas définir cette propriété dans le cas contraire.

dans Windows Vista et Windows XP, Windows Installer n’écrit pas les informations d’assembly dans le registre. En outre, les assemblys partagés, les assemblys privés et les assemblys côte à côte peuvent être utilisés. Pour plus d’informations, consultez [assemblys partagés](shared-assemblies.md), [assemblys privés](private-assemblies.md)et [assemblys côte à côte](side-by-side-assemblies.md).

les sections suivantes décrivent comment créer un package Windows Installer pour installer des assemblys Win32 partagés, privés ou côte à côte sur différents systèmes d’exploitation Windows.

-   [installation d’assemblys Win32 pour le partage côte à côte sur Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [installation d’assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



