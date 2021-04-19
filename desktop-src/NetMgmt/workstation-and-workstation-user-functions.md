---
title: Fonctions utilisateur de station de travail et de station de travail
description: Les fonctions de station de travail de gestion de réseau effectuent des tâches d’administration sur une station de travail locale ou distante.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509873"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="cb6b7-103">Fonctions utilisateur de station de travail et de station de travail</span><span class="sxs-lookup"><span data-stu-id="cb6b7-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="cb6b7-104">Les fonctions de station de travail de gestion de réseau effectuent des tâches d’administration sur une station de travail locale ou distante.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="cb6b7-105">Seul un utilisateur ou une application ayant l’appartenance à un groupe d’administrateurs, sur un serveur local ou distant, peut effectuer des tâches d’administration sur une station de travail pour contrôler son fonctionnement, son accès utilisateur et son partage de ressources.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="cb6b7-106">Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="cb6b7-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="cb6b7-107">Les fonctions de station de travail sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="cb6b7-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="cb6b7-108">Function</span></span>                                   | <span data-ttu-id="cb6b7-109">Description</span><span class="sxs-lookup"><span data-stu-id="cb6b7-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="cb6b7-110">**NetWkstaGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="cb6b7-111">Retourne des informations sur les éléments de configuration d’une station de travail.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="cb6b7-112">**NetWkstaSetInfo**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="cb6b7-113">Configure une station de travail.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="cb6b7-114">Les fonctions de station de travail permettent d’accéder à deux types discrets d’informations sur les stations de travail :</span><span class="sxs-lookup"><span data-stu-id="cb6b7-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="cb6b7-115">Informations système</span><span class="sxs-lookup"><span data-stu-id="cb6b7-115">System information</span></span>
-   <span data-ttu-id="cb6b7-116">Informations spécifiques à la plateforme</span><span class="sxs-lookup"><span data-stu-id="cb6b7-116">Platform-specific information</span></span>

<span data-ttu-id="cb6b7-117">Dans chaque type, les données sont classées par accès de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="cb6b7-118">Les données accessibles à l’invité sont un sous-ensemble des données accessibles par l’utilisateur, qui est à son tour un sous-ensemble des données accessibles par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="cb6b7-119">Les informations de station de travail sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="cb6b7-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="cb6b7-120">**WKSTA \_ INFO \_ 100**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="cb6b7-121">**WKSTA \_ INFO \_ 101**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="cb6b7-122">**WKSTA \_ INFO \_ 102**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="cb6b7-123">Les fonctions utilisateur de la station de travail de gestion du réseau permettent d’accéder à des informations spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="cb6b7-124">Les informations spécifiques à l’utilisateur sont séparées des informations de la station de travail, car il peut y avoir plusieurs utilisateurs sur une station de travail.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="cb6b7-125">Les fonctions utilisateur de station de travail sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="cb6b7-126">Fonction</span><span class="sxs-lookup"><span data-stu-id="cb6b7-126">Function</span></span>                                           | <span data-ttu-id="cb6b7-127">Description</span><span class="sxs-lookup"><span data-stu-id="cb6b7-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb6b7-128">**NetWkstaUserEnum**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="cb6b7-129">Répertorie des informations sur tous les utilisateurs actuellement connectés à la station de travail.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="cb6b7-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="cb6b7-131">Retourne des informations sur un utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="cb6b7-132">**NetWkstaUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="cb6b7-133">Définit les informations spécifiques à l’utilisateur pour les éléments de configuration d’une station de travail.</span><span class="sxs-lookup"><span data-stu-id="cb6b7-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="cb6b7-134">Les informations utilisateur de station de travail sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="cb6b7-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="cb6b7-135">**\_Informations utilisateur \_ wksta \_ 0**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="cb6b7-136">**\_Informations utilisateur \_ wksta \_ 1**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="cb6b7-137">**\_Informations utilisateur \_ wksta \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="cb6b7-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 