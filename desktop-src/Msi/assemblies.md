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
# <a name="assemblies"></a><span data-ttu-id="c8f30-103">Assemblys</span><span class="sxs-lookup"><span data-stu-id="c8f30-103">Assemblies</span></span>

<span data-ttu-id="c8f30-104">Windows Installer pouvez installer, supprimer et mettre à jour les assemblys et assemblys Win32 utilisés par le common language runtime de l’infrastructure Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="c8f30-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c8f30-105">Un assembly est géré par le Windows Installer en tant que composant d’installation unique.</span><span class="sxs-lookup"><span data-stu-id="c8f30-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="c8f30-106">Tous les fichiers qui constituent un assembly doivent être contenus par un composant d’installation unique qui est listé dans la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f30-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="c8f30-107">Les Windows Installer s’exécutant sur Windows Vista et Windows XP peuvent installer des assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="c8f30-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="c8f30-108">Les assemblys côte à côte peuvent partager en toute sécurité des assemblys entre plusieurs applications et peuvent décaler les effets négatifs du partage d’assembly, tels que les conflits de DLL.</span><span class="sxs-lookup"><span data-stu-id="c8f30-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="c8f30-109">Au lieu d’une seule version d’un assembly qui suppose la compatibilité descendante avec toutes les applications, le partage d’assembly côte à côte permet à plusieurs versions d’un assembly COM ou Win32 de s’exécuter simultanément sur le système.</span><span class="sxs-lookup"><span data-stu-id="c8f30-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="c8f30-110">Cette fonctionnalité améliorée pour isoler les applications est une partie importante de l’infrastructure Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="c8f30-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c8f30-111">Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span><span class="sxs-lookup"><span data-stu-id="c8f30-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="c8f30-112">Les sections suivantes décrivent l’utilisation des assemblys avec l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c8f30-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="c8f30-113">Ajout d’assemblys à un package</span><span class="sxs-lookup"><span data-stu-id="c8f30-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="c8f30-114">Installation et suppression d’assemblys</span><span class="sxs-lookup"><span data-stu-id="c8f30-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="c8f30-115">Mise à jour des assemblys</span><span class="sxs-lookup"><span data-stu-id="c8f30-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="c8f30-116">Modes de réinstallation des assemblys du Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="c8f30-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="c8f30-117">Clés de registre de l’assembly écrites par Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c8f30-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="c8f30-118">Pour plus d’informations sur l’installation des applications COM et COM+ 1,0, consultez [installation d’une application com+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md), [installation d’un composant COM dans un emplacement privé](installing-a-com-component-to-a-private-location.md)et [création d’un composant COM dans un package existant privé](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="c8f30-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
