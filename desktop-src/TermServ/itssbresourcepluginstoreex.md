---
title: Interface ITsSbResourcePluginStoreEx
description: Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface ITsSbResourcePluginStoreEx
- Services Bureau à distance de l’interface ITsSbResourcePluginStoreEx, Description
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104296"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="7d0b1-105">Interface ITsSbResourcePluginStoreEx</span><span class="sxs-lookup"><span data-stu-id="7d0b1-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="7d0b1-106">Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="7d0b1-107">Ces méthodes ajoutent, suppriment et interrogent ces objets.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="7d0b1-108">Cette interface est uniquement disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="7d0b1-109">Les méthodes [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) et [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) de l’interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) sont disponibles à partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="7d0b1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7d0b1-110">Members</span></span>

<span data-ttu-id="7d0b1-111">L’interface **ITsSbResourcePluginStoreEx** hérite de [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="7d0b1-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="7d0b1-112">**ITsSbResourcePluginStoreEx** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7d0b1-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="7d0b1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7d0b1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7d0b1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7d0b1-114">Methods</span></span>

<span data-ttu-id="7d0b1-115">L’interface **ITsSbResourcePluginStoreEx** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="7d0b1-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="7d0b1-116">Method</span></span>                                                                                                            | <span data-ttu-id="7d0b1-117">Description</span><span class="sxs-lookup"><span data-stu-id="7d0b1-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d0b1-118">**AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="7d0b1-119">Verrouille une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="7d0b1-120">**AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="7d0b1-121">Ajoute un environnement au magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="7d0b1-122">**AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="7d0b1-123">Ajoute une nouvelle session au magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="7d0b1-124">**AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="7d0b1-125">Ajoute une cible au magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="7d0b1-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="7d0b1-127">Supprime une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="7d0b1-128">**EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="7d0b1-129">Retourne un tableau qui contient les environnements présents dans le magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="7d0b1-130">**EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="7d0b1-131">Énumère toutes les batteries de serveurs qui ont été ajoutées au magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="7d0b1-132">**EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="7d0b1-133">Énumère un ensemble de sessions spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="7d0b1-134">**EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="7d0b1-135">Retourne un tableau qui contient les cibles spécifiées qui sont présentes dans le magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="7d0b1-136">**GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="7d0b1-137">Récupère une propriété d’une batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="7d0b1-138">**QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="7d0b1-139">Retourne l’objet d’environnement spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="7d0b1-140">**QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="7d0b1-141">Retourne l’objet de session qui a l’ID de session spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="7d0b1-142">**QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="7d0b1-143">Retourne la cible qui a le nom cible et le nom de la batterie de serveurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="7d0b1-144">**ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="7d0b1-145">Libère un verrou sur une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="7d0b1-146">**RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="7d0b1-147">Supprime l’environnement spécifié du magasin de plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="7d0b1-148">**SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="7d0b1-149">Enregistre un environnement.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="7d0b1-150">**SaveSession**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="7d0b1-151">Enregistre une session.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="7d0b1-152">**SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="7d0b1-153">Enregistre une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="7d0b1-154">**SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="7d0b1-155">Définit une propriété sur un environnement.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="7d0b1-156">**SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="7d0b1-157">Définit une propriété sur un environnement.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="7d0b1-158">**SetSessionState**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="7d0b1-159">Définit l’état d’une session.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="7d0b1-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="7d0b1-161">Définit une propriété sur une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="7d0b1-162">**SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="7d0b1-163">Définit une propriété sur une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="7d0b1-164">**SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="7d0b1-165">Définit l’état d’une cible.</span><span class="sxs-lookup"><span data-stu-id="7d0b1-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="7d0b1-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d0b1-166">Requirements</span></span>



| <span data-ttu-id="7d0b1-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d0b1-167">Requirement</span></span> | <span data-ttu-id="7d0b1-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d0b1-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0b1-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d0b1-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7d0b1-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d0b1-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7d0b1-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d0b1-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7d0b1-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7d0b1-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="7d0b1-173">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7d0b1-173">End of server support</span></span><br/>    | <span data-ttu-id="7d0b1-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7d0b1-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="7d0b1-175">IID</span><span class="sxs-lookup"><span data-stu-id="7d0b1-175">IID</span></span><br/>                      | <span data-ttu-id="7d0b1-176">IID \_ ITsSbResourcePluginStoreEx est défini en tant que 80b83ffd-625d-11e5-BEA1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="7d0b1-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d0b1-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d0b1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0b1-178">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="7d0b1-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="7d0b1-179">Bureau à distance les interfaces de virtualisation</span><span class="sxs-lookup"><span data-stu-id="7d0b1-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





