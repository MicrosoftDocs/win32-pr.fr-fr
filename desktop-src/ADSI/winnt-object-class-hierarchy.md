---
title: Hiérarchie de classes d’objets Winnt
description: La hiérarchie de classes d’objets Winnt démarre à partir de l’objet Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI du fournisseur de services WinNT, hiérarchie des classes d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507023"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="28cc3-104">Hiérarchie de classes d’objets Winnt</span><span class="sxs-lookup"><span data-stu-id="28cc3-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="28cc3-105">La hiérarchie de classes d’objets Winnt démarre à partir de l’objet Namespace.</span><span class="sxs-lookup"><span data-stu-id="28cc3-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="28cc3-106">classe d'objet,</span><span class="sxs-lookup"><span data-stu-id="28cc3-106">Object class</span></span>                   | <span data-ttu-id="28cc3-107">Description</span><span class="sxs-lookup"><span data-stu-id="28cc3-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="28cc3-108">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="28cc3-108">Namespace</span></span><br/>           | <span data-ttu-id="28cc3-109">Conteneur d’objets de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="28cc3-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="28cc3-110">Domain</span><span class="sxs-lookup"><span data-stu-id="28cc3-110">Domain</span></span><br/>              | <span data-ttu-id="28cc3-111">Domaine Windows NT.</span><span class="sxs-lookup"><span data-stu-id="28cc3-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="28cc3-112">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="28cc3-112">User</span></span><br/>                | <span data-ttu-id="28cc3-113">Compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28cc3-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="28cc3-114">Group</span><span class="sxs-lookup"><span data-stu-id="28cc3-114">Group</span></span><br/>               | <span data-ttu-id="28cc3-115">Compte de groupe pour la gestion des droits d’accès.</span><span class="sxs-lookup"><span data-stu-id="28cc3-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="28cc3-116">UserGroupCollection</span><span class="sxs-lookup"><span data-stu-id="28cc3-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="28cc3-117">Ensemble de groupes d’utilisateurs qui implémentent [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="28cc3-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="28cc3-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="28cc3-118">GroupCollection</span></span><br/>     | <span data-ttu-id="28cc3-119">Ensemble d’autres groupes qui implémentent [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="28cc3-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="28cc3-120">Computer</span><span class="sxs-lookup"><span data-stu-id="28cc3-120">Computer</span></span><br/>            | <span data-ttu-id="28cc3-121">Serveur ou station de travail Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="28cc3-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="28cc3-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="28cc3-122">PrintJob</span></span><br/>            | <span data-ttu-id="28cc3-123">Travail d’impression dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="28cc3-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="28cc3-124">PrintJobsCollection</span><span class="sxs-lookup"><span data-stu-id="28cc3-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="28cc3-125">Ensemble de travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="28cc3-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="28cc3-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="28cc3-126">PrintQueue</span></span><br/>          | <span data-ttu-id="28cc3-127">File d’attente à l’impression sur un spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="28cc3-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="28cc3-128">Service</span><span class="sxs-lookup"><span data-stu-id="28cc3-128">Service</span></span><br/>             | <span data-ttu-id="28cc3-129">Application s’exécutant en tant que service.</span><span class="sxs-lookup"><span data-stu-id="28cc3-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="28cc3-130">FileService</span><span class="sxs-lookup"><span data-stu-id="28cc3-130">FileService</span></span><br/>         | <span data-ttu-id="28cc3-131">Services accédant au système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="28cc3-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="28cc3-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="28cc3-132">FileShare</span></span><br/>           | <span data-ttu-id="28cc3-133">Point de partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="28cc3-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="28cc3-134">Ressource</span><span class="sxs-lookup"><span data-stu-id="28cc3-134">Resource</span></span><br/>            | <span data-ttu-id="28cc3-135">Ressource dans le service.</span><span class="sxs-lookup"><span data-stu-id="28cc3-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="28cc3-136">session</span><span class="sxs-lookup"><span data-stu-id="28cc3-136">Session</span></span><br/>             | <span data-ttu-id="28cc3-137">Connexion au service de fichiers active.</span><span class="sxs-lookup"><span data-stu-id="28cc3-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="28cc3-138">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="28cc3-138">User</span></span><br/>                | <span data-ttu-id="28cc3-139">Compte d’utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="28cc3-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="28cc3-140">Group</span><span class="sxs-lookup"><span data-stu-id="28cc3-140">Group</span></span><br/>               | <span data-ttu-id="28cc3-141">Groupe local.</span><span class="sxs-lookup"><span data-stu-id="28cc3-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="28cc3-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="28cc3-142">UserCollection</span></span><br/>      | <span data-ttu-id="28cc3-143">Collection d’utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="28cc3-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="28cc3-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="28cc3-144">GroupCollection</span></span><br/>     | <span data-ttu-id="28cc3-145">Collection de groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="28cc3-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="28cc3-146">schéma</span><span class="sxs-lookup"><span data-stu-id="28cc3-146">Schema</span></span><br/>              | <span data-ttu-id="28cc3-147">Conteneur du schéma Winnt.</span><span class="sxs-lookup"><span data-stu-id="28cc3-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="28cc3-148">Classe</span><span class="sxs-lookup"><span data-stu-id="28cc3-148">Class</span></span><br/>               | <span data-ttu-id="28cc3-149">Définition de classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="28cc3-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="28cc3-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="28cc3-150">Property</span></span><br/>            | <span data-ttu-id="28cc3-151">Définition d’attribut de schéma.</span><span class="sxs-lookup"><span data-stu-id="28cc3-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="28cc3-152">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28cc3-152">Syntax</span></span><br/>              | <span data-ttu-id="28cc3-153">Syntaxe d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="28cc3-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





