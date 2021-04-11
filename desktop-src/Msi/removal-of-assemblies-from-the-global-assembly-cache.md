---
description: L’Windows Installer détermine s’il faut autoriser la suppression d’un assembly common language runtime basé sur une liste de clients qu’il conserve indépendamment de l’assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Suppression d’assemblys du global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202871"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="2fd78-103">Suppression d’assemblys du global assembly cache</span><span class="sxs-lookup"><span data-stu-id="2fd78-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="2fd78-104">L’Windows Installer détermine s’il faut autoriser la suppression d’un assembly common language runtime basé sur une liste de clients qu’il conserve indépendamment de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="2fd78-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="2fd78-105">Le Windows Installer conserve un bit de code confidentiel pour représenter les clients Windows Installer de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="2fd78-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="2fd78-106">Le programme d’installation épingle l’assembly pour le premier client Windows Installer et le désépingle lorsque le dernier client Windows Installer est supprimé.</span><span class="sxs-lookup"><span data-stu-id="2fd78-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="2fd78-107">L’assembly gère un bit de code confidentiel pour chaque client d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="2fd78-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="2fd78-108">La Windows Installer n’est pas directement responsable de la suppression physique des assemblys de common language runtime de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2fd78-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="2fd78-109">Le programme d’installation désépingle l’assembly lorsque la dernière Windows Installer client est supprimée.</span><span class="sxs-lookup"><span data-stu-id="2fd78-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="2fd78-110">Si le Windows Installer est le dernier client de l’assembly, le common language runtime permet de forcer un nettoyage synchrone de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="2fd78-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="2fd78-111">Le processus de nettoyage est atomique et il n’y a aucune provision pour une « restauration » à ce stade.</span><span class="sxs-lookup"><span data-stu-id="2fd78-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="2fd78-112">Tout désépinglage de common language runtime assemblys doit se produire après que l’utilisateur a eu la possibilité d’annuler l’installation ou la suppression.</span><span class="sxs-lookup"><span data-stu-id="2fd78-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



