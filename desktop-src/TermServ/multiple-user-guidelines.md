---
title: Instructions pour plusieurs utilisateurs
description: Instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544145"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="4c073-103">Instructions pour plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4c073-103">Multiple-user guidelines</span></span>

<span data-ttu-id="4c073-104">Les sections suivantes fournissent des instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4c073-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c073-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4c073-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4c073-106">Configuration des applications</span><span class="sxs-lookup"><span data-stu-id="4c073-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="4c073-107">L’installation d’une application pour un seul utilisateur peut créer des problèmes dans un environnement multi-utilisateur Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4c073-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="4c073-108">Stockage des informations spécifiques à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c073-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="4c073-109">Les applications doivent stocker les informations spécifiques à l’utilisateur dans des emplacements spécifiques à l’utilisateur, séparément des informations globales qui s’appliquent à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4c073-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="4c073-110">Espaces de noms d’objets de noyau</span><span class="sxs-lookup"><span data-stu-id="4c073-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="4c073-111">Services Bureau à distance utilise plusieurs espaces de noms pour les objets de noyau ; un espace de noms global est principalement utilisé par les services dans les applications client/serveur.</span><span class="sxs-lookup"><span data-stu-id="4c073-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="4c073-112">Adresses IP et noms d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="4c073-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="4c073-113">Il est déconseillé de supposer que le nom d’ordinateur ou l’ adresse IP affectée à l’ordinateur sont associés à un seul utilisateur, étant donné que plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de Session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4c073-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="4c073-114">Comme toujours, verrouillez les fichiers et les bases de données tout en apportant des modifications pour empêcher toute perte accidentelle de données.</span><span class="sxs-lookup"><span data-stu-id="4c073-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="4c073-115">Votre application ne doit pas verrouiller les fichiers d’application d’exécution qui ne sont pas des fichiers par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c073-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="4c073-116">Les fichiers d’exécution verrouillés peuvent empêcher l’exécution de plusieurs instances de l’application, ou des processus sous l’application, tels que les assistants.</span><span class="sxs-lookup"><span data-stu-id="4c073-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="4c073-117">Un bon moyen de tester les fichiers qui sont des fichiers d’application au moment de l’exécution consiste à effectuer le suivi des fichiers qui sont installés par le programme d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="4c073-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="4c073-118">Les fichiers par utilisateur sont rarement installés par le programme d’installation de. par conséquent, la plupart des fichiers installés par le programme d’installation sont des fichiers d’application au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4c073-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




