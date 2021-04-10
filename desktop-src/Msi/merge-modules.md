---
description: Les modules de fusion offrent une méthode standard par laquelle les développeurs fournissent des composants de Windows Installer partagés et une logique de configuration à leurs applications.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210592"
---
# <a name="merge-modules"></a><span data-ttu-id="a1efc-103">Modules de fusion</span><span class="sxs-lookup"><span data-stu-id="a1efc-103">Merge Modules</span></span>

<span data-ttu-id="a1efc-104">Les modules de fusion offrent une méthode standard par laquelle les développeurs fournissent des [*composants*](c-gly.md) de Windows Installer partagés et une logique de configuration à leurs applications.</span><span class="sxs-lookup"><span data-stu-id="a1efc-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="a1efc-105">Les modules de fusion sont utilisés pour distribuer du code partagé, des fichiers, des ressources, des entrées de Registre et une logique de configuration aux applications sous la forme d’un fichier composé unique.</span><span class="sxs-lookup"><span data-stu-id="a1efc-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="a1efc-106">Les développeurs qui créent de nouveaux modules de fusion ou qui utilisent des modules de fusion existants doivent suivre la norme décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="a1efc-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="a1efc-107">Un module de fusion est de structure similaire à un [*fichier Windows Installer. msi*](m-gly.md)simplifié.</span><span class="sxs-lookup"><span data-stu-id="a1efc-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="a1efc-108">Toutefois, un module de fusion ne peut pas être installé seul, il doit être fusionné dans un package d’installation à l’aide d’un outil de fusion.</span><span class="sxs-lookup"><span data-stu-id="a1efc-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="a1efc-109">Les développeurs souhaitant utiliser des modules de fusion doivent obtenir l’un des outils de fusion distribués librement, tels que Mergemod.dll, ou acheter un outil de fusion auprès d’un éditeur de logiciels indépendant.</span><span class="sxs-lookup"><span data-stu-id="a1efc-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="a1efc-110">Les développeurs peuvent créer des modules de fusion à l’aide de nombreux outils logiciels utilisés pour créer un package d’installation Windows Installer, tel que l’éditeur de table de base de données Orca fourni avec le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a1efc-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="a1efc-111">Lorsqu’un module de fusion est fusionné dans le fichier. msi d’une application, toutes les informations et ressources nécessaires à l’installation des composants fournis par le module de fusion sont incorporées dans le fichier. msi de l’application.</span><span class="sxs-lookup"><span data-stu-id="a1efc-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="a1efc-112">Le module de fusion n’est alors plus nécessaire pour installer ces composants et le module de fusion n’a pas besoin d’être accessible à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a1efc-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="a1efc-113">Étant donné que toutes les informations nécessaires pour installer les composants sont fournies sous la forme d’un fichier unique, l’utilisation de modules de fusion peut éliminer de nombreuses instances de conflits de version, des entrées de Registre manquantes et des fichiers installés de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a1efc-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="a1efc-114">Pour plus d’informations sur les modules de fusion, consultez :</span><span class="sxs-lookup"><span data-stu-id="a1efc-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="a1efc-115">À propos des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="a1efc-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="a1efc-116">Utilisation de modules de fusion</span><span class="sxs-lookup"><span data-stu-id="a1efc-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="a1efc-117">Référence de module de fusion</span><span class="sxs-lookup"><span data-stu-id="a1efc-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 



