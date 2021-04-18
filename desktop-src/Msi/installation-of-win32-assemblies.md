---
description: Installez les assemblys Win32 en les faisant un composant de Microsoft Windows Installer Package qui installe ou met à jour votre application.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installation d’assemblys Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519786"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="a6718-103">Installation d’assemblys Win32</span><span class="sxs-lookup"><span data-stu-id="a6718-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="a6718-104">Installez les assemblys Win32 en les faisant un composant de Microsoft Windows Installer Package qui installe ou met à jour votre application.</span><span class="sxs-lookup"><span data-stu-id="a6718-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="a6718-105">Lorsque vous créez la table [MsiAssembly](msiassembly-table.md) et la [table MsiAssemblyName](msiassemblyname-table.md), cela identifie le composant dans la \_ colonne composant en tant qu’assembly.</span><span class="sxs-lookup"><span data-stu-id="a6718-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="a6718-106">Le programme d’installation va définir la propriété [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) sur la version de fichier de Sxs.dll sur les systèmes d’exploitation qui peuvent prendre en charge les assemblys Win32 et ne pas définir cette propriété dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a6718-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="a6718-107">Dans Windows Vista et Windows XP, Windows Installer n’écrit pas les informations d’assembly dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a6718-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="a6718-108">En outre, les assemblys partagés, les assemblys privés et les assemblys côte à côte peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="a6718-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="a6718-109">Pour plus d’informations, consultez [assemblys partagés](shared-assemblies.md), [assemblys privés](private-assemblies.md)et [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a6718-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="a6718-110">Les sections suivantes décrivent comment créer un package Windows Installer pour installer des assemblys Win32 partagés, privés ou côte à côte sur différents systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="a6718-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="a6718-111">Installation d’assemblys Win32 pour le partage côte à côte sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6718-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="a6718-112">Installation d’assemblys Win32 pour l’utilisation privée d’une application sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6718-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



