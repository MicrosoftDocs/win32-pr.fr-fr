---
description: Le fournisseur WMI pour Hyper-V permet aux développeurs et aux scripteurs de créer rapidement des outils personnalisés, des utilitaires et des améliorations pour la plate-forme de virtualisation. Les interfaces WMI peuvent gérer tous les aspects des services Hyper-V.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: À propos du fournisseur WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529846"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="d5825-104">À propos du fournisseur WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="d5825-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="d5825-105">Le fournisseur WMI pour Hyper-V permet aux développeurs et aux scripteurs de créer rapidement des outils personnalisés, des utilitaires et des améliorations pour la plate-forme de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="d5825-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="d5825-106">Les interfaces WMI peuvent gérer tous les aspects des services Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d5825-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="d5825-107">À propos de Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="d5825-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="d5825-108">Microsoft Windows Server 2008 R2 Hyper-V permet aux administrateurs système de consolider des serveurs matériels distincts sur un seul serveur exécutant Microsoft Windows Server 2008 R2 en tant que système d’exploitation hôte.</span><span class="sxs-lookup"><span data-stu-id="d5825-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="d5825-109">Chacun des ordinateurs virtuels hébergés s’exécute dans son propre environnement virtuel distinct et isolé.</span><span class="sxs-lookup"><span data-stu-id="d5825-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="d5825-110">Cela permet à l’administrateur de gérer, de fournir et de gérer facilement un grand nombre d’ordinateurs virtuels tout en réduisant le besoin d’exécuter plusieurs solutions matérielles pour utiliser différents produits et systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d5825-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="d5825-111">Un autre avantage de l’environnement d’ordinateur virtuel réside dans le test et le support.</span><span class="sxs-lookup"><span data-stu-id="d5825-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="d5825-112">De nouvelles configurations de serveur et de système peuvent être déployées et testées en parallèle avec le système existant sans nécessiter de temps d’arrêt coûteux pendant la phase de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d5825-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="d5825-113">Chaque machine virtuelle peut être configurée pour utiliser des configurations différentes en cours d’exécution sur une plateforme standard pour produire de meilleurs résultats de test.</span><span class="sxs-lookup"><span data-stu-id="d5825-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="d5825-114">Avec la prise en charge des systèmes d’exploitation antérieurs, il est possible de prendre en charge et de tester le matériel, les systèmes et les applications hérités.</span><span class="sxs-lookup"><span data-stu-id="d5825-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="d5825-115">La prise en charge des instantanés vous permet de prendre un instantané de l’état d’une machine virtuelle afin de pouvoir revenir à un événement antérieur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d5825-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="d5825-116">Hyper-V expose une interface riche qui permet à l’utilisateur de surveiller et de contrôler l’environnement de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5825-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="d5825-117">La plupart des Hyper-V peuvent être contrôlés à l’aide du fournisseur WMI, qui permet une personnalisation facile, mais puissante, des machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="d5825-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="d5825-118">Pour plus d’informations sur ce qui peut être contrôlé avec le fournisseur WMI, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5825-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="d5825-119">Service de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="d5825-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="d5825-120">Service de mise en réseau</span><span class="sxs-lookup"><span data-stu-id="d5825-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="d5825-121">Service de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="d5825-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="d5825-122">Nouveautés du fournisseur WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="d5825-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



