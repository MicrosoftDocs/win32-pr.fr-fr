---
description: Un AppContainer est implémenté en ajoutant de nouvelles informations au jeton de processus, en modifiant SeAccessCheck () afin que tous les objets de liste de contrôle d’accès (ACL) hérités et non modifiés bloquent les demandes d’accès des processus AppContainer par défaut, et les objets de réacl qui doivent être disponibles pour AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implémentation d’un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867810"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="cbe22-103">Implémentation d’un AppContainer</span><span class="sxs-lookup"><span data-stu-id="cbe22-103">Implementing an AppContainer</span></span>

<span data-ttu-id="cbe22-104">Un AppContainer est implémenté en ajoutant de nouvelles informations au jeton de processus, en modifiant [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) afin que tous les objets de liste de contrôle d’accès (ACL) hérités et non modifiés bloquent les demandes d’accès des processus AppContainer par défaut, et les objets de réacl qui doivent être disponibles pour AppContainers.</span><span class="sxs-lookup"><span data-stu-id="cbe22-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="cbe22-105">Processus</span><span class="sxs-lookup"><span data-stu-id="cbe22-105">The process</span></span>

<span data-ttu-id="cbe22-106">Commencez par ajouter de nouvelles informations pour le jeton de processus.</span><span class="sxs-lookup"><span data-stu-id="cbe22-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="cbe22-107">Modifiez ensuite **SeAccessCheck ()** afin que toutes les listes de contrôle d’accès héritées non modifiées bloquent les demandes d’accès des processus AppContainer par défaut.</span><span class="sxs-lookup"><span data-stu-id="cbe22-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="cbe22-108">Enfin, reconfigurez les ressources de liste de contrôle d’accès qui doivent être disponibles pour AppContainers</span><span class="sxs-lookup"><span data-stu-id="cbe22-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="cbe22-109">Le SID AppContainer est un identificateur unique persistant pour l’appcontainer.</span><span class="sxs-lookup"><span data-stu-id="cbe22-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="cbe22-110">Les SID de capacité accordent l’accès à des groupes de ressources à des groupes de AppContainers.</span><span class="sxs-lookup"><span data-stu-id="cbe22-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="cbe22-111">Un AppContainerNumber est un **DWORD** temporaire utilisé pour distinguer les AppContainers.</span><span class="sxs-lookup"><span data-stu-id="cbe22-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="cbe22-112">Toutefois, il ne doit pas être utilisé en tant qu’identité pour l’AppContainer.</span><span class="sxs-lookup"><span data-stu-id="cbe22-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="cbe22-113">Pour autoriser un seul AppContainer à accéder à une ressource, ajoutez son AppContainerSID à la liste de contrôle d’accès pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="cbe22-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="cbe22-114">Pour permettre à plusieurs AppContainers spécifiques d’accéder à une ressource, ajoutez tous leurs AppContainerSIDs à la liste de contrôle d’accès pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="cbe22-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="cbe22-115">Pour gérer des groupes d’autorisations, créez un SID de capacité (un GUID) et placez ce SID de fonctionnalité sur toutes les ressources à accorder.</span><span class="sxs-lookup"><span data-stu-id="cbe22-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="cbe22-116">Ajoutez ensuite le SID de fonctionnalité à votre jeton de processus.</span><span class="sxs-lookup"><span data-stu-id="cbe22-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="cbe22-117">Pour autoriser tous les AppContainers à accéder à une ressource, ajoutez le SID **tous les packages d’application** à la liste de contrôle d’accès de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="cbe22-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="cbe22-118">Cela agit comme un caractère générique.</span><span class="sxs-lookup"><span data-stu-id="cbe22-118">This acts like a wildcard.</span></span>

<span data-ttu-id="cbe22-119">AppContainerSID et CapabilitySID prennent tous deux en charge les masques d’accès dans les entrées Access Control (ACE).</span><span class="sxs-lookup"><span data-stu-id="cbe22-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="cbe22-120">Définissez le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe22-120">Set as appropriate.</span></span>

 

 
