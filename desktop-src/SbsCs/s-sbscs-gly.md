---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759040"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="bc719-103">S (applications isolées et assemblys côte à côte)</span><span class="sxs-lookup"><span data-stu-id="bc719-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="bc719-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="bc719-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bc719-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly partagé côte à côte**</span><span class="sxs-lookup"><span data-stu-id="bc719-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="bc719-106">Un assembly partagé côte à côte est disponible pour une utilisation par plusieurs applications sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc719-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="bc719-107">Il est installé dans le dossier WinSxS du répertoire Windows.</span><span class="sxs-lookup"><span data-stu-id="bc719-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="bc719-108">Les applications et les administrateurs peuvent gérer la version d’un assembly partagé à utiliser en spécifiant la configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="bc719-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="bc719-109">Les assemblys côte à côte sont toujours accompagnés de fichiers manifestes qui fournissent des informations sur l’assembly au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bc719-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bc719-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly côte à côte**</span><span class="sxs-lookup"><span data-stu-id="bc719-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="bc719-111">Un assembly côte à côte est un assembly Win32 accompagné de manifestes.</span><span class="sxs-lookup"><span data-stu-id="bc719-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="bc719-112">Un assembly côte à côte contient une collection de ressources (un groupe de dll, de classes Windows, de serveurs COM, de bibliothèques de types ou d’interfaces) qui sont toujours fournies aux applications ensemble.</span><span class="sxs-lookup"><span data-stu-id="bc719-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="bc719-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**partage d’assembly côte à côte**</span><span class="sxs-lookup"><span data-stu-id="bc719-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="bc719-114">Utilisation d’assemblys côte à côte pour partager en toute sécurité des assemblys entre plusieurs applications et pour compenser les effets négatifs du partage, tels que les conflits de DLL.</span><span class="sxs-lookup"><span data-stu-id="bc719-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="bc719-115">Au lieu d’avoir une seule version d’un assembly qui suppose la compatibilité descendante avec toutes les applications, le partage d’assembly côte à côte permet à plusieurs versions d’un assembly Win32 de s’exécuter simultanément sur le système.</span><span class="sxs-lookup"><span data-stu-id="bc719-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="bc719-116">Les assemblys côte à côte sont toujours accompagnés des fichiers manifestes de l’assembly qui fournissent des informations sur l’assembly au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bc719-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="bc719-117">Les applications et les administrateurs peuvent gérer le partage d’assemblys côte à côte après le déploiement en mettant à jour la configuration de l’application au niveau global ou par application.</span><span class="sxs-lookup"><span data-stu-id="bc719-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



