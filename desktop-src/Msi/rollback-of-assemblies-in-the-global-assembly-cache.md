---
description: Un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys. Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Restauration d’assemblys dans le global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751117"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="4b99b-104">Restauration d’assemblys dans le global assembly cache</span><span class="sxs-lookup"><span data-stu-id="4b99b-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="4b99b-105">Un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys.</span><span class="sxs-lookup"><span data-stu-id="4b99b-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="4b99b-106">Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="4b99b-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="4b99b-107">Au cours de la première étape, l’Windows Installer utilise l’infrastructure Microsoft .NET pour créer une interface pour chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="4b99b-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="4b99b-108">Le Windows Installer utilise autant d’interfaces qu’il y a d’assemblys en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="4b99b-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="4b99b-109">La validation d’un assembly à l’aide de l’une de ces interfaces signifie uniquement que l’assembly est prêt à remplacer un assembly existant portant le même nom, il ne le remplace pas encore.</span><span class="sxs-lookup"><span data-stu-id="4b99b-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="4b99b-110">Si l’utilisateur annule l’installation, ou s’il y a une erreur d’installation irrécupérable, le Windows Installer peut toujours restaurer l’assembly à son état précédent en libérant ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="4b99b-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="4b99b-111">Une fois l’Windows Installer terminée l’installation de tous les assemblys et Windows Installer composants, le programme d’installation peut lancer la deuxième étape de l’installation.</span><span class="sxs-lookup"><span data-stu-id="4b99b-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="4b99b-112">La deuxième étape utilise une fonction distincte pour effectuer la validation finale de tous les nouveaux assemblys de common language runtime.</span><span class="sxs-lookup"><span data-stu-id="4b99b-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="4b99b-113">Cela remplace tous les assemblys existants portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="4b99b-113">This replaces any existing assemblies with the same name.</span></span>

 

 



