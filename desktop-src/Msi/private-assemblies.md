---
description: Un assembly Win32 peut être installé en tant qu’assembly privé et être disponible exclusivement pour une utilisation par une seule application. Les assemblys privés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assemblys privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203194"
---
# <a name="private-assemblies"></a><span data-ttu-id="c32ff-104">Assemblys privés</span><span class="sxs-lookup"><span data-stu-id="c32ff-104">Private Assemblies</span></span>

<span data-ttu-id="c32ff-105">Un assembly Win32 peut être installé en tant qu’assembly privé et être disponible exclusivement pour une utilisation par une seule application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="c32ff-106">Les assemblys privés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="c32ff-107">Sur Windows XP, les assemblys privés sont installés en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c32ff-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="c32ff-108">Le Windows Installer installe des assemblys côte à côte privés dans un dossier privé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="c32ff-109">Généralement le dossier qui contient le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="c32ff-110">La dépendance de l’application sur l’assembly privé est spécifiée dans un fichier manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="c32ff-111">Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c32ff-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="c32ff-112">Sur les systèmes d’exploitation antérieurs à Windows XP, une copie de l’assembly privé et d’un fichier. local est installée dans un dossier privé pour l’utilisation exclusive de l’application.</span><span class="sxs-lookup"><span data-stu-id="c32ff-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="c32ff-113">Une version de l’assembly est également inscrite globalement sur le système et disponible pour toutes les applications qui y sont liées.</span><span class="sxs-lookup"><span data-stu-id="c32ff-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="c32ff-114">La version globale de l’assembly peut être la version installée avec l’application ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="c32ff-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="c32ff-115">La version globale est déterminée par les mêmes règles que celles utilisées par les [composants isolés](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="c32ff-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="c32ff-116">Notez que le Windows Installer ne peut pas installer un assembly privé dans un emplacement dont le chemin d’accès contient plus de 234 caractères, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c32ff-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
