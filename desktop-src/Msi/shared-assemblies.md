---
description: Un assembly Win32 peut être installé en tant qu’assembly partagé et être disponible pour une utilisation par plusieurs applications sur l’ordinateur. Les assemblys partagés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757810"
---
# <a name="shared-assemblies"></a><span data-ttu-id="ba42c-104">Assemblys partagés</span><span class="sxs-lookup"><span data-stu-id="ba42c-104">Shared Assemblies</span></span>

<span data-ttu-id="ba42c-105">Un assembly Win32 peut être installé en tant qu’assembly partagé et être disponible pour une utilisation par plusieurs applications sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba42c-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="ba42c-106">Les assemblys partagés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.</span><span class="sxs-lookup"><span data-stu-id="ba42c-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="ba42c-107">Les assemblys partagés sont installés en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="ba42c-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="ba42c-108">Le Windows Installer installe les assemblys côte à côte partagés dans le dossier WinSxS.</span><span class="sxs-lookup"><span data-stu-id="ba42c-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="ba42c-109">Les assemblys ne sont pas inscrits globalement sur le système, mais ils sont disponibles à l’échelle mondiale pour toute application qui spécifie une dépendance sur l’assembly dans un fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="ba42c-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="ba42c-110">Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ba42c-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="ba42c-111">Sur les systèmes d’exploitation antérieurs à Windows XP, les assemblys partagés sont généralement installés dans le dossier système Windows et enregistrés globalement.</span><span class="sxs-lookup"><span data-stu-id="ba42c-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="ba42c-112">La dernière version installée est disponible pour toutes les applications qui y sont liées.</span><span class="sxs-lookup"><span data-stu-id="ba42c-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="ba42c-113">Pour plus d’informations sur la création d’un package Windows Installer pour installer un assembly partagé, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba42c-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="ba42c-114">Installation d’assemblys Win32 pour le partage côte à côte sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba42c-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="ba42c-115">Installation d’assemblys Win32 pour l’utilisation privée d’une application sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba42c-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
