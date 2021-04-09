---
description: Contient un objet pour chaque application COM+ installée sur l’ordinateur local. Les propriétés exposées par ces objets conservent tous les paramètres effectués au niveau de l’application.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Collection d’applications
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111055"
---
# <a name="applications-collection"></a><span data-ttu-id="fed15-104">Collection d’applications</span><span class="sxs-lookup"><span data-stu-id="fed15-104">Applications collection</span></span>

<span data-ttu-id="fed15-105">Contient un objet pour chaque application COM+ installée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fed15-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="fed15-106">Les propriétés exposées par ces objets conservent tous les paramètres effectués au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="fed15-107">Vous définissez les propriétés des composants dans une application à l’aide de la collection de [**composants**](components.md) associés.</span><span class="sxs-lookup"><span data-stu-id="fed15-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="fed15-108">Vous attribuez des rôles à une application à l’aide de la collection de [**rôles**](roles.md) associée.</span><span class="sxs-lookup"><span data-stu-id="fed15-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="fed15-109">Pour installer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="fed15-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="fed15-110">Pour installer une application à partir d’un fichier ou pour arrêter ou exporter une application, utilisez également des méthodes sur l’objet **COMAdminCatalog** .</span><span class="sxs-lookup"><span data-stu-id="fed15-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="fed15-111">Sinon, pour créer une nouvelle application, vous pouvez ajouter un objet à la collection d' **applications** .</span><span class="sxs-lookup"><span data-stu-id="fed15-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="fed15-112">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fed15-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fed15-113">Membres</span><span class="sxs-lookup"><span data-stu-id="fed15-113">Members</span></span>

<span data-ttu-id="fed15-114">La collection d' **applications** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fed15-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fed15-115">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="fed15-115">Related Collections</span></span>

<span data-ttu-id="fed15-116">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="fed15-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fed15-117">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="fed15-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="fed15-118">**Composants**</span><span class="sxs-lookup"><span data-stu-id="fed15-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="fed15-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fed15-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fed15-120">**LegacyComponents**</span><span class="sxs-lookup"><span data-stu-id="fed15-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="fed15-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fed15-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fed15-122">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="fed15-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="fed15-123">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="fed15-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="fed15-124">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="fed15-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fed15-125">**Partitions**</span><span class="sxs-lookup"><span data-stu-id="fed15-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="fed15-126">**Causes**</span><span class="sxs-lookup"><span data-stu-id="fed15-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="fed15-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fed15-127">Properties</span></span>

<span data-ttu-id="fed15-128">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="fed15-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fed15-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="fed15-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="fed15-131">Activation</span><span class="sxs-lookup"><span data-stu-id="fed15-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="fed15-132">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="fed15-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="fed15-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="fed15-134">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="fed15-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="fed15-135">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="fed15-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="fed15-136">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="fed15-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="fed15-137">Authentification</span><span class="sxs-lookup"><span data-stu-id="fed15-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="fed15-138">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="fed15-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="fed15-139">Modifiables</span><span class="sxs-lookup"><span data-stu-id="fed15-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="fed15-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="fed15-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="fed15-141">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="fed15-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="fed15-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="fed15-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="fed15-143">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="fed15-144">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="fed15-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="fed15-145">Supprimé</span><span class="sxs-lookup"><span data-stu-id="fed15-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="fed15-146">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-146">Description</span></span>](#description)
-   [<span data-ttu-id="fed15-147">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="fed15-148">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="fed15-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="fed15-149">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="fed15-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="fed15-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="fed15-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="fed15-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="fed15-152">Identifiant</span><span class="sxs-lookup"><span data-stu-id="fed15-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="fed15-153">Identité</span><span class="sxs-lookup"><span data-stu-id="fed15-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="fed15-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="fed15-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="fed15-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="fed15-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="fed15-157">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="fed15-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="fed15-158">Nom</span><span class="sxs-lookup"><span data-stu-id="fed15-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="fed15-159">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="fed15-159">Password</span></span>](#password)
-   [<span data-ttu-id="fed15-160">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="fed15-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="fed15-161">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="fed15-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="fed15-162">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="fed15-163">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="fed15-164">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="fed15-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="fed15-166">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="fed15-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="fed15-167">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="fed15-168">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="fed15-169">Replicable</span><span class="sxs-lookup"><span data-stu-id="fed15-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="fed15-170">RunForever</span><span class="sxs-lookup"><span data-stu-id="fed15-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="fed15-171">FormName</span><span class="sxs-lookup"><span data-stu-id="fed15-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="fed15-172">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="fed15-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="fed15-173">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="fed15-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="fed15-174">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="fed15-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="fed15-175">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="fed15-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="fed15-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="fed15-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="fed15-177">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="fed15-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="fed15-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="fed15-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-180">Entry</span></span> | <span data-ttu-id="fed15-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-182">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-182">Description</span></span>    | <span data-ttu-id="fed15-183">Indique si l’application peut utiliser 3 Go de mémoire dans son processus.</span><span class="sxs-lookup"><span data-stu-id="fed15-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="fed15-184">Si cette option n’est pas activée, l’application ne peut utiliser que 2 Go de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fed15-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="fed15-185">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-185">Access</span></span>         | <span data-ttu-id="fed15-186">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="fed15-187">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-187">Type</span></span>           | <span data-ttu-id="fed15-188">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="fed15-189">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-189">Default</span></span>        | <span data-ttu-id="fed15-190">False</span><span class="sxs-lookup"><span data-stu-id="fed15-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="fed15-191">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-191">Minimum system</span></span> | <span data-ttu-id="fed15-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="fed15-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-193">AccessChecksLevel</span></span>



| <span data-ttu-id="fed15-194">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-194">Entry</span></span> | <span data-ttu-id="fed15-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-196">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-196">Description</span></span>    | <span data-ttu-id="fed15-197">Indique si les contrôles d’accès sont effectués uniquement au niveau du processus ou au niveau du processus et du composant.</span><span class="sxs-lookup"><span data-stu-id="fed15-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="fed15-198">Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="fed15-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="fed15-199">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-199">Access</span></span>         | <span data-ttu-id="fed15-200">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="fed15-201">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-201">Type</span></span>           | <span data-ttu-id="fed15-202">Longues valeurs possibles : COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="fed15-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="fed15-203">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-203">Default</span></span>        | <span data-ttu-id="fed15-204">COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="fed15-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="fed15-205">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-205">Minimum system</span></span> | <span data-ttu-id="fed15-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="fed15-207">Activation</span><span class="sxs-lookup"><span data-stu-id="fed15-207">Activation</span></span>



| <span data-ttu-id="fed15-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-208">Entry</span></span> | <span data-ttu-id="fed15-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-210">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-210">Description</span></span>    | <span data-ttu-id="fed15-211">L’activation locale indique que les objets de l’application s’exécutent dans un processus serveur local dédié (application serveur).</span><span class="sxs-lookup"><span data-stu-id="fed15-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="fed15-212">L’activation en cours indique que les objets s’exécutent dans le processus de leur créateur (application de bibliothèque).</span><span class="sxs-lookup"><span data-stu-id="fed15-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="fed15-213">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-213">Access</span></span>         | <span data-ttu-id="fed15-214">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="fed15-215">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-215">Type</span></span>           | <span data-ttu-id="fed15-216">Longues valeurs possibles : COMAdminActivationInproc (0) COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="fed15-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="fed15-217">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-217">Default</span></span>        | <span data-ttu-id="fed15-218">COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="fed15-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="fed15-219">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-219">Minimum system</span></span> | <span data-ttu-id="fed15-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="fed15-221">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="fed15-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-222">Entry</span></span> | <span data-ttu-id="fed15-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-224">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-224">Description</span></span>    | <span data-ttu-id="fed15-225">Indique si les contrôles d’accès sont effectués pour l’application lorsque les clients y effectuent des appels.</span><span class="sxs-lookup"><span data-stu-id="fed15-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="fed15-226">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-226">Access</span></span>         | <span data-ttu-id="fed15-227">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="fed15-228">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-228">Type</span></span>           | <span data-ttu-id="fed15-229">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="fed15-230">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-230">Default</span></span>        | <span data-ttu-id="fed15-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-231">True</span></span>                                                                                               |
| <span data-ttu-id="fed15-232">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-232">Minimum system</span></span> | <span data-ttu-id="fed15-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="fed15-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="fed15-234">ApplicationDirectory</span></span>



| <span data-ttu-id="fed15-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-235">Entry</span></span> | <span data-ttu-id="fed15-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-237">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-237">Description</span></span>    | <span data-ttu-id="fed15-238">Chemin d’accès complet à l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-238">The full path to the application.</span></span> <span data-ttu-id="fed15-239">Ces informations sont nécessaires lorsque vous configurez des assemblys côte à côte (SxS).</span><span class="sxs-lookup"><span data-stu-id="fed15-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="fed15-240">Les assemblys côte à côte (SxS) permettent aux applications ASP de spécifier la version d’une DLL système prise en charge par SxS à utiliser, telle que MSVCRT, MSXML, COMCTL, GDIPLUS, etc.</span><span class="sxs-lookup"><span data-stu-id="fed15-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="fed15-241">Par exemple, si votre application ASP repose sur la version 2,0 de MSVCRT, vous pouvez vous assurer que votre application utilise toujours la version 2,0 de MSVCRT même après l’application des service packs au serveur.</span><span class="sxs-lookup"><span data-stu-id="fed15-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="fed15-242">Toute nouvelle version de MSVCRT est toujours installée sur l’ordinateur, mais la version 2,0 reste et est utilisée par votre application.</span><span class="sxs-lookup"><span data-stu-id="fed15-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="fed15-243">Les dll prises en charge par SxS sont stockées dans% WINDIR% \\ WinSxS.</span><span class="sxs-lookup"><span data-stu-id="fed15-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="fed15-244">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-244">Access</span></span>         | <span data-ttu-id="fed15-245">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fed15-246">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-246">Type</span></span>           | <span data-ttu-id="fed15-247">String</span><span class="sxs-lookup"><span data-stu-id="fed15-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="fed15-248">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-248">Default</span></span>        | <span data-ttu-id="fed15-249">""</span><span class="sxs-lookup"><span data-stu-id="fed15-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fed15-250">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-250">Minimum system</span></span> | <span data-ttu-id="fed15-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="fed15-252">Une seule version d’une DLL système peut être utilisée dans n’importe quel pool d’applications, même si cette fonctionnalité est configurable au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="fed15-253">Par exemple, si l’application App1 utilise MSVCRT, version 2,5 et que l’application App2 utilise MSVCRT, version 2,4, App1 et App2 ne doivent pas figurer dans le même pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="fed15-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="fed15-254">Si c’est le cas, l’application qui est chargée en premier a sa version de MSVCRT chargée, et l’autre application est obligée de l’utiliser jusqu’à ce que les applications soient déchargées.</span><span class="sxs-lookup"><span data-stu-id="fed15-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="fed15-255">Pour plus d’informations, consultez « assemblys côte à côte » dans [modifications dans les services com+ dans IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="fed15-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="fed15-256">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="fed15-256">ApplicationProxy</span></span>



| <span data-ttu-id="fed15-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-257">Entry</span></span> | <span data-ttu-id="fed15-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="fed15-259">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-259">Description</span></span>    | <span data-ttu-id="fed15-260">Indique si l’application est un proxy d’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="fed15-261">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-261">Access</span></span>         | <span data-ttu-id="fed15-262">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fed15-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="fed15-263">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-263">Type</span></span>           | <span data-ttu-id="fed15-264">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-264">Bool</span></span>                                                       |
| <span data-ttu-id="fed15-265">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-265">Default</span></span>        | <span data-ttu-id="fed15-266">False</span><span class="sxs-lookup"><span data-stu-id="fed15-266">False</span></span>                                                      |
| <span data-ttu-id="fed15-267">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-267">Minimum system</span></span> | <span data-ttu-id="fed15-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="fed15-269">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="fed15-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="fed15-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-270">Entry</span></span> | <span data-ttu-id="fed15-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-272">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-272">Description</span></span>    | <span data-ttu-id="fed15-273">Nom de serveur distant utilisé lors de l’exportation du proxy d’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="fed15-274">Il s’agit du nom du serveur vers lequel pointe le proxy d’application lorsqu’il est installé sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="fed15-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="fed15-275">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-275">Access</span></span>         | <span data-ttu-id="fed15-276">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="fed15-277">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-277">Type</span></span>           | <span data-ttu-id="fed15-278">String</span><span class="sxs-lookup"><span data-stu-id="fed15-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="fed15-279">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-279">Default</span></span>        | <span data-ttu-id="fed15-280">""</span><span class="sxs-lookup"><span data-stu-id="fed15-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="fed15-281">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-281">Minimum system</span></span> | <span data-ttu-id="fed15-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="fed15-283">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="fed15-283">AppPartitionID</span></span>



| <span data-ttu-id="fed15-284">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-284">Entry</span></span> | <span data-ttu-id="fed15-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="fed15-286">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-286">Description</span></span>    | <span data-ttu-id="fed15-287">GUID représentant l’ID de la partition d’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="fed15-288">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-288">Access</span></span>         | <span data-ttu-id="fed15-289">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fed15-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="fed15-290">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-290">Type</span></span>           | <span data-ttu-id="fed15-291">String</span><span class="sxs-lookup"><span data-stu-id="fed15-291">String</span></span>                                            |
| <span data-ttu-id="fed15-292">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="fed15-293">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-293">Minimum system</span></span> | <span data-ttu-id="fed15-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed15-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="fed15-295">Authentification</span><span class="sxs-lookup"><span data-stu-id="fed15-295">Authentication</span></span>



| <span data-ttu-id="fed15-296">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-296">Entry</span></span> | <span data-ttu-id="fed15-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-298">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-298">Description</span></span>    | <span data-ttu-id="fed15-299">Définit le niveau d’authentification pour les appels, avec les valeurs correspondant aux paramètres d’authentification de l’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="fed15-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="fed15-300">Lorsque COMAdminAuthenticationDefault est choisi, le paramètre dans la propriété DefaultAuthenticationLevel de la collection [**LocalComputer**](localcomputer.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fed15-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="fed15-301">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-301">Access</span></span>         | <span data-ttu-id="fed15-302">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fed15-303">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-303">Type</span></span>           | <span data-ttu-id="fed15-304">Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="fed15-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="fed15-305">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-305">Default</span></span>        | <span data-ttu-id="fed15-306">COMAdminAuthenticationPacket (4)</span><span class="sxs-lookup"><span data-stu-id="fed15-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fed15-307">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-307">Minimum system</span></span> | <span data-ttu-id="fed15-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="fed15-309">Pour les applications de bibliothèque (in-process), les seuls paramètres valides sont COMAdminAuthenticationDefault et COMAdminAuthenticationNone.</span><span class="sxs-lookup"><span data-stu-id="fed15-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="fed15-310">Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="fed15-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="fed15-311">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="fed15-311">AuthenticationCapability</span></span>



| <span data-ttu-id="fed15-312">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-312">Entry</span></span> | <span data-ttu-id="fed15-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-314">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-314">Description</span></span>    | <span data-ttu-id="fed15-315">Détermine l’identité qui est présentée lorsque les appels sont empruntés.</span><span class="sxs-lookup"><span data-stu-id="fed15-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="fed15-316">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-316">Access</span></span>         | <span data-ttu-id="fed15-317">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="fed15-318">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-318">Type</span></span>           | <span data-ttu-id="fed15-319">Valeurs possibles longues : COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0X2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="fed15-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="fed15-320">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-320">Default</span></span>        | <span data-ttu-id="fed15-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="fed15-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="fed15-322">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-322">Minimum system</span></span> | <span data-ttu-id="fed15-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="fed15-324">Modifiables</span><span class="sxs-lookup"><span data-stu-id="fed15-324">Changeable</span></span>



| <span data-ttu-id="fed15-325">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-325">Entry</span></span> | <span data-ttu-id="fed15-326">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-327">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-327">Description</span></span>    | <span data-ttu-id="fed15-328">Détermine si les modifications apportées aux paramètres d’application ou à ceux de ses composants sont autorisées, par programmation ou par le biais de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="fed15-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="fed15-329">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-329">Access</span></span>         | <span data-ttu-id="fed15-330">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="fed15-331">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-331">Type</span></span>           | <span data-ttu-id="fed15-332">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="fed15-333">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-333">Default</span></span>        | <span data-ttu-id="fed15-334">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="fed15-335">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-335">Minimum system</span></span> | <span data-ttu-id="fed15-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="fed15-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="fed15-337">CommandLine</span></span>



| <span data-ttu-id="fed15-338">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-338">Entry</span></span> | <span data-ttu-id="fed15-339">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-340">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-340">Description</span></span>    | <span data-ttu-id="fed15-341">Chaîne de ligne de commande à utiliser lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="fed15-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="fed15-342">L’application peut être lancée dans un débogueur avec la ligne de commande spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fed15-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="fed15-343">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-343">Access</span></span>         | <span data-ttu-id="fed15-344">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="fed15-345">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-345">Type</span></span>           | <span data-ttu-id="fed15-346">String</span><span class="sxs-lookup"><span data-stu-id="fed15-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="fed15-347">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-347">Default</span></span>        | <span data-ttu-id="fed15-348">""</span><span class="sxs-lookup"><span data-stu-id="fed15-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="fed15-349">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-349">Minimum system</span></span> | <span data-ttu-id="fed15-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="fed15-351">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="fed15-351">ConcurrentApps</span></span>



| <span data-ttu-id="fed15-352">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-352">Entry</span></span> | <span data-ttu-id="fed15-353">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-354">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-354">Description</span></span>    | <span data-ttu-id="fed15-355">Spécifie le nombre maximal d’applications regroupables pouvant s’exécuter simultanément.</span><span class="sxs-lookup"><span data-stu-id="fed15-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="fed15-356">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-356">Access</span></span>         | <span data-ttu-id="fed15-357">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="fed15-358">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-358">Type</span></span>           | <span data-ttu-id="fed15-359">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="fed15-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="fed15-360">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-360">Default</span></span>        | <span data-ttu-id="fed15-361">1</span><span class="sxs-lookup"><span data-stu-id="fed15-361">1</span></span>                                                                                |
| <span data-ttu-id="fed15-362">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-362">Minimum system</span></span> | <span data-ttu-id="fed15-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="fed15-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="fed15-364">CreatedBy</span></span>



| <span data-ttu-id="fed15-365">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-365">Entry</span></span> | <span data-ttu-id="fed15-366">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="fed15-367">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-367">Description</span></span>    | <span data-ttu-id="fed15-368">Chaîne informatif pour décrire qui a créé l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="fed15-369">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-369">Access</span></span>         | <span data-ttu-id="fed15-370">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="fed15-371">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-371">Type</span></span>           | <span data-ttu-id="fed15-372">String</span><span class="sxs-lookup"><span data-stu-id="fed15-372">String</span></span>                                                        |
| <span data-ttu-id="fed15-373">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-373">Default</span></span>        | <span data-ttu-id="fed15-374">""</span><span class="sxs-lookup"><span data-stu-id="fed15-374">""</span></span>                                                            |
| <span data-ttu-id="fed15-375">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-375">Minimum system</span></span> | <span data-ttu-id="fed15-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="fed15-377">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-377">CRMEnabled</span></span>



| <span data-ttu-id="fed15-378">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-378">Entry</span></span> | <span data-ttu-id="fed15-379">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="fed15-380">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-380">Description</span></span>    | <span data-ttu-id="fed15-381">Détermine si le Gestionnaire des ressources de compensation est activé.</span><span class="sxs-lookup"><span data-stu-id="fed15-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="fed15-382">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-382">Access</span></span>         | <span data-ttu-id="fed15-383">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="fed15-384">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-384">Type</span></span>           | <span data-ttu-id="fed15-385">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-385">Bool</span></span>                                                             |
| <span data-ttu-id="fed15-386">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-386">Default</span></span>        | <span data-ttu-id="fed15-387">False</span><span class="sxs-lookup"><span data-stu-id="fed15-387">False</span></span>                                                            |
| <span data-ttu-id="fed15-388">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-388">Minimum system</span></span> | <span data-ttu-id="fed15-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="fed15-390">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="fed15-390">CRMLogFile</span></span>



| <span data-ttu-id="fed15-391">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-391">Entry</span></span> | <span data-ttu-id="fed15-392">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-393">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-393">Description</span></span>    | <span data-ttu-id="fed15-394">Nom et chemin d’accès du fichier pour conserver le journal pour le CRM (Compensating Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="fed15-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="fed15-395">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-395">Access</span></span>         | <span data-ttu-id="fed15-396">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="fed15-397">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-397">Type</span></span>           | <span data-ttu-id="fed15-398">String</span><span class="sxs-lookup"><span data-stu-id="fed15-398">String</span></span>                                                                                 |
| <span data-ttu-id="fed15-399">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-399">Default</span></span>        | <span data-ttu-id="fed15-400">""</span><span class="sxs-lookup"><span data-stu-id="fed15-400">""</span></span>                                                                                     |
| <span data-ttu-id="fed15-401">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-401">Minimum system</span></span> | <span data-ttu-id="fed15-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="fed15-403">Supprimé</span><span class="sxs-lookup"><span data-stu-id="fed15-403">Deleteable</span></span>



| <span data-ttu-id="fed15-404">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-404">Entry</span></span> | <span data-ttu-id="fed15-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-406">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-406">Description</span></span>    | <span data-ttu-id="fed15-407">Définit si l’application peut être supprimée, soit par programme, soit par le biais de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="fed15-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="fed15-408">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-408">Access</span></span>         | <span data-ttu-id="fed15-409">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="fed15-410">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-410">Type</span></span>           | <span data-ttu-id="fed15-411">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="fed15-412">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-412">Default</span></span>        | <span data-ttu-id="fed15-413">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="fed15-414">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-414">Minimum system</span></span> | <span data-ttu-id="fed15-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="fed15-416">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-416">Description</span></span>



| <span data-ttu-id="fed15-417">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-417">Entry</span></span> | <span data-ttu-id="fed15-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="fed15-419">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-419">Description</span></span>    | <span data-ttu-id="fed15-420">Décrit l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-420">Describes the application.</span></span> |
| <span data-ttu-id="fed15-421">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-421">Access</span></span>         | <span data-ttu-id="fed15-422">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-422">ReadWrite</span></span>                  |
| <span data-ttu-id="fed15-423">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-423">Type</span></span>           | <span data-ttu-id="fed15-424">String</span><span class="sxs-lookup"><span data-stu-id="fed15-424">String</span></span>                     |
| <span data-ttu-id="fed15-425">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-425">Default</span></span>        | <span data-ttu-id="fed15-426">""</span><span class="sxs-lookup"><span data-stu-id="fed15-426">""</span></span>                         |
| <span data-ttu-id="fed15-427">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-427">Minimum system</span></span> | <span data-ttu-id="fed15-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="fed15-429">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-429">DumpEnabled</span></span>



| <span data-ttu-id="fed15-430">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-430">Entry</span></span> | <span data-ttu-id="fed15-431">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-432">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-432">Description</span></span>    | <span data-ttu-id="fed15-433">Active le vidage de l’état d’une application COM+ au moment de l’échec dans un répertoire désigné.</span><span class="sxs-lookup"><span data-stu-id="fed15-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="fed15-434">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-434">Access</span></span>         | <span data-ttu-id="fed15-435">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="fed15-436">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-436">Type</span></span>           | <span data-ttu-id="fed15-437">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="fed15-438">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-438">Default</span></span>        | <span data-ttu-id="fed15-439">False</span><span class="sxs-lookup"><span data-stu-id="fed15-439">False</span></span>                                                                                                 |
| <span data-ttu-id="fed15-440">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-440">Minimum system</span></span> | <span data-ttu-id="fed15-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="fed15-442">À partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux fichiers de vidage COM+.</span><span class="sxs-lookup"><span data-stu-id="fed15-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="fed15-443">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="fed15-443">DumpOnException</span></span>



| <span data-ttu-id="fed15-444">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-444">Entry</span></span> | <span data-ttu-id="fed15-445">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-446">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-446">Description</span></span>    | <span data-ttu-id="fed15-447">Active le vidage de l’état d’une application COM+ lorsque l’application provoque une exception non gérée et se termine par le runtime COM+.</span><span class="sxs-lookup"><span data-stu-id="fed15-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="fed15-448">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-448">Access</span></span>         | <span data-ttu-id="fed15-449">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="fed15-450">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-450">Type</span></span>           | <span data-ttu-id="fed15-451">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="fed15-452">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-452">Default</span></span>        | <span data-ttu-id="fed15-453">False</span><span class="sxs-lookup"><span data-stu-id="fed15-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="fed15-454">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-454">Minimum system</span></span> | <span data-ttu-id="fed15-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="fed15-456">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="fed15-456">DumpOnFailfast</span></span>



| <span data-ttu-id="fed15-457">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-457">Entry</span></span> | <span data-ttu-id="fed15-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-459">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-459">Description</span></span>    | <span data-ttu-id="fed15-460">Active le vidage de l’état d’une application COM+ en cas d’échec de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="fed15-461">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-461">Access</span></span>         | <span data-ttu-id="fed15-462">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="fed15-463">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-463">Type</span></span>           | <span data-ttu-id="fed15-464">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-464">Bool</span></span>                                                                            |
| <span data-ttu-id="fed15-465">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-465">Default</span></span>        | <span data-ttu-id="fed15-466">False</span><span class="sxs-lookup"><span data-stu-id="fed15-466">False</span></span>                                                                           |
| <span data-ttu-id="fed15-467">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-467">Minimum system</span></span> | <span data-ttu-id="fed15-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="fed15-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="fed15-469">DumpPath</span></span>



| <span data-ttu-id="fed15-470">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-470">Entry</span></span> | <span data-ttu-id="fed15-471">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="fed15-472">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-472">Description</span></span>    | <span data-ttu-id="fed15-473">Chemin d’accès du répertoire dans lequel les fichiers de vidage sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fed15-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="fed15-474">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-474">Access</span></span>         | <span data-ttu-id="fed15-475">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="fed15-476">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-476">Type</span></span>           | <span data-ttu-id="fed15-477">String</span><span class="sxs-lookup"><span data-stu-id="fed15-477">String</span></span>                                                       |
| <span data-ttu-id="fed15-478">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-478">Default</span></span>        | <span data-ttu-id="fed15-479">« % systemroot% \\ system32 \\ com \\ DMP »</span><span class="sxs-lookup"><span data-stu-id="fed15-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="fed15-480">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-480">Minimum system</span></span> | <span data-ttu-id="fed15-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="fed15-482">À partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux fichiers de vidage COM+.</span><span class="sxs-lookup"><span data-stu-id="fed15-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="fed15-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-483">EventsEnabled</span></span>



| <span data-ttu-id="fed15-484">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-484">Entry</span></span> | <span data-ttu-id="fed15-485">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="fed15-486">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-486">Description</span></span>    | <span data-ttu-id="fed15-487">Indique si les événements sont activés pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="fed15-488">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-488">Access</span></span>         | <span data-ttu-id="fed15-489">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="fed15-490">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-490">Type</span></span>           | <span data-ttu-id="fed15-491">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-491">Bool</span></span>                                                      |
| <span data-ttu-id="fed15-492">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-492">Default</span></span>        | <span data-ttu-id="fed15-493">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-493">True</span></span>                                                      |
| <span data-ttu-id="fed15-494">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-494">Minimum system</span></span> | <span data-ttu-id="fed15-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="fed15-496">id</span><span class="sxs-lookup"><span data-stu-id="fed15-496">ID</span></span>



| <span data-ttu-id="fed15-497">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-497">Entry</span></span> | <span data-ttu-id="fed15-498">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-499">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-499">Description</span></span>    | <span data-ttu-id="fed15-500">GUID représentant l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-500">A GUID representing the application.</span></span> <span data-ttu-id="fed15-501">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="fed15-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fed15-502">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-502">Access</span></span>         | <span data-ttu-id="fed15-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fed15-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="fed15-504">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-504">Type</span></span>           | <span data-ttu-id="fed15-505">String</span><span class="sxs-lookup"><span data-stu-id="fed15-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="fed15-506">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="fed15-507">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-507">Minimum system</span></span> | <span data-ttu-id="fed15-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="fed15-509">Identité</span><span class="sxs-lookup"><span data-stu-id="fed15-509">Identity</span></span>



| <span data-ttu-id="fed15-510">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-510">Entry</span></span> | <span data-ttu-id="fed15-511">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-512">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-512">Description</span></span>    | <span data-ttu-id="fed15-513">Définit l’identité du processus serveur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="fed15-514">Spécifiez un compte d’utilisateur valide ou un « utilisateur interactif » pour que l’application assume l’identité de l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="fed15-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="fed15-515">Vous pouvez également spécifier les chaînes « NT Authority \\ LocalService », « NT Authority \\ NetworkService » et « NT Authority \\ System ».</span><span class="sxs-lookup"><span data-stu-id="fed15-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="fed15-516">Le mot de passe par défaut de ces trois comptes est «» (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="fed15-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="fed15-517">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-518">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-519">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-520">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-520">Minimum system</span></span> | <span data-ttu-id="fed15-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="fed15-522">La propriété Identity n’est pas activée pour les applications de bibliothèque, qui s’exécutent dans le processus client.</span><span class="sxs-lookup"><span data-stu-id="fed15-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="fed15-523">La propriété de mot de passe doit être définie en même temps que l’identité, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fed15-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="fed15-524">Si le mot de passe et l’identité ne sont pas synchronisés, l’application ne peut pas être lancée tant qu’elle n’est pas réinitialisée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="fed15-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="fed15-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-525">ImpersonationLevel</span></span>



| <span data-ttu-id="fed15-526">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-526">Entry</span></span> | <span data-ttu-id="fed15-527">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-528">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-528">Description</span></span>    | <span data-ttu-id="fed15-529">Définit le niveau d’emprunt d’identité utilisé pour les appels effectués à d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="fed15-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="fed15-530">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-530">Access</span></span>         | <span data-ttu-id="fed15-531">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="fed15-532">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-532">Type</span></span>           | <span data-ttu-id="fed15-533">Valeurs possibles longues : COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="fed15-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="fed15-534">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-534">Default</span></span>        | <span data-ttu-id="fed15-535">COMAdminImpersonationImpersonate (3)</span><span class="sxs-lookup"><span data-stu-id="fed15-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="fed15-536">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-536">Minimum system</span></span> | <span data-ttu-id="fed15-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="fed15-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-538">IsEnabled</span></span>



| <span data-ttu-id="fed15-539">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-539">Entry</span></span> | <span data-ttu-id="fed15-540">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-541">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-541">Description</span></span>    | <span data-ttu-id="fed15-542">Si l’application ou le composant COM+ est désactivé, IsEnabled a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="fed15-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="fed15-543">Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fed15-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="fed15-544">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-544">Access</span></span>         | <span data-ttu-id="fed15-545">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="fed15-546">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-546">Type</span></span>           | <span data-ttu-id="fed15-547">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="fed15-548">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-548">Default</span></span>        | <span data-ttu-id="fed15-549">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="fed15-550">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-550">Minimum system</span></span> | <span data-ttu-id="fed15-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="fed15-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="fed15-552">IsSystem</span></span>



| <span data-ttu-id="fed15-553">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-553">Entry</span></span> | <span data-ttu-id="fed15-554">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="fed15-555">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-555">Description</span></span>    | <span data-ttu-id="fed15-556">Identifie les applications système COM+.</span><span class="sxs-lookup"><span data-stu-id="fed15-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="fed15-557">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-557">Access</span></span>         | <span data-ttu-id="fed15-558">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fed15-558">ReadOnly</span></span>                             |
| <span data-ttu-id="fed15-559">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-559">Type</span></span>           | <span data-ttu-id="fed15-560">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-560">Bool</span></span>                                 |
| <span data-ttu-id="fed15-561">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-561">Default</span></span>        | <span data-ttu-id="fed15-562">False</span><span class="sxs-lookup"><span data-stu-id="fed15-562">False</span></span>                                |
| <span data-ttu-id="fed15-563">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-563">Minimum system</span></span> | <span data-ttu-id="fed15-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="fed15-565">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="fed15-565">MaxDumpCount</span></span>



| <span data-ttu-id="fed15-566">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-566">Entry</span></span> | <span data-ttu-id="fed15-567">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-568">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-568">Description</span></span>    | <span data-ttu-id="fed15-569">Indique le nombre maximal de fichiers à générer avant le remplacement.</span><span class="sxs-lookup"><span data-stu-id="fed15-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="fed15-570">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-570">Access</span></span>         | <span data-ttu-id="fed15-571">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="fed15-572">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-572">Type</span></span>           | <span data-ttu-id="fed15-573">Long (1-200)</span><span class="sxs-lookup"><span data-stu-id="fed15-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="fed15-574">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-574">Default</span></span>        | <span data-ttu-id="fed15-575">5</span><span class="sxs-lookup"><span data-stu-id="fed15-575">5</span></span>                                                                                |
| <span data-ttu-id="fed15-576">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-576">Minimum system</span></span> | <span data-ttu-id="fed15-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="fed15-578">Nom</span><span class="sxs-lookup"><span data-stu-id="fed15-578">Name</span></span>



| <span data-ttu-id="fed15-579">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-579">Entry</span></span> | <span data-ttu-id="fed15-580">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-581">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-581">Description</span></span>    | <span data-ttu-id="fed15-582">Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-582">The name of the application.</span></span> <span data-ttu-id="fed15-583">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="fed15-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fed15-584">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-584">Access</span></span>         | <span data-ttu-id="fed15-585">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="fed15-586">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-586">Type</span></span>           | <span data-ttu-id="fed15-587">String</span><span class="sxs-lookup"><span data-stu-id="fed15-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="fed15-588">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-588">Default</span></span>        | <span data-ttu-id="fed15-589">« Nouvelle application »</span><span class="sxs-lookup"><span data-stu-id="fed15-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-590">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-590">Minimum system</span></span> | <span data-ttu-id="fed15-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="fed15-592">Vous devez choisir des noms uniques pour les applications.</span><span class="sxs-lookup"><span data-stu-id="fed15-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="fed15-593">Si plusieurs applications sont créées avec le même nom, elle peut interférer avec le référencement des applications par nom, ce qui entraîne un comportement imprévisible.</span><span class="sxs-lookup"><span data-stu-id="fed15-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="fed15-594">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="fed15-594">Password</span></span>



| <span data-ttu-id="fed15-595">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-595">Entry</span></span> | <span data-ttu-id="fed15-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fed15-597">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-597">Description</span></span>    | <span data-ttu-id="fed15-598">Définit le mot de passe utilisé par le processus serveur pour se connecter sous l’identité.</span><span class="sxs-lookup"><span data-stu-id="fed15-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="fed15-599">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-599">Access</span></span>         | <span data-ttu-id="fed15-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="fed15-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="fed15-601">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-601">Type</span></span>           | <span data-ttu-id="fed15-602">String</span><span class="sxs-lookup"><span data-stu-id="fed15-602">String</span></span>                                                                     |
| <span data-ttu-id="fed15-603">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-603">Default</span></span>        | <span data-ttu-id="fed15-604">""</span><span class="sxs-lookup"><span data-stu-id="fed15-604">""</span></span>                                                                         |
| <span data-ttu-id="fed15-605">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-605">Minimum system</span></span> | <span data-ttu-id="fed15-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="fed15-607">Le mot de passe doit être défini en même temps que l’identité, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fed15-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="fed15-608">Si le mot de passe et l’identité ne sont pas synchronisés, l’application ne peut pas être lancée tant qu’elle n’est pas réinitialisée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="fed15-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="fed15-609">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="fed15-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="fed15-610">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-610">Entry</span></span> | <span data-ttu-id="fed15-611">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-612">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-612">Description</span></span>    | <span data-ttu-id="fed15-613">Indique dans quelles circonstances les demandes mises en file d’attente vers une application sont authentifiées.</span><span class="sxs-lookup"><span data-stu-id="fed15-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="fed15-614">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-614">Access</span></span>         | <span data-ttu-id="fed15-615">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="fed15-616">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-616">Type</span></span>           | <span data-ttu-id="fed15-617">Longues valeurs possibles : COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2)</span><span class="sxs-lookup"><span data-stu-id="fed15-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="fed15-618">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-618">Default</span></span>        | <span data-ttu-id="fed15-619">COMAdminQCMessageAuthenticateSecureApps (0)</span><span class="sxs-lookup"><span data-stu-id="fed15-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="fed15-620">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-620">Minimum system</span></span> | <span data-ttu-id="fed15-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="fed15-622">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="fed15-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="fed15-623">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-623">Entry</span></span> | <span data-ttu-id="fed15-624">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-625">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-625">Description</span></span>    | <span data-ttu-id="fed15-626">Indique le nombre maximal de threads d’écoute simultanés.</span><span class="sxs-lookup"><span data-stu-id="fed15-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="fed15-627">La plage valide pour cette propriété est comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="fed15-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="fed15-628">Pour une application nouvellement créée, le paramètre est dérivé de l’algorithme actuellement utilisé pour déterminer le nombre par défaut de threads de l’écouteur : 16 fois le nombre de processeurs dans le serveur.</span><span class="sxs-lookup"><span data-stu-id="fed15-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="fed15-629">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-629">Access</span></span>         | <span data-ttu-id="fed15-630">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fed15-631">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-631">Type</span></span>           | <span data-ttu-id="fed15-632">Long (0-1000)</span><span class="sxs-lookup"><span data-stu-id="fed15-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fed15-633">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-633">Default</span></span>        | <span data-ttu-id="fed15-634">0</span><span class="sxs-lookup"><span data-stu-id="fed15-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fed15-635">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-635">Minimum system</span></span> | <span data-ttu-id="fed15-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="fed15-637">Cette propriété est également disponible avec la fonctionnalité de lecture/écriture à partir de l’onglet mise en **file d’attente** de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="fed15-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="fed15-638">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="fed15-639">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-639">Entry</span></span> | <span data-ttu-id="fed15-640">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-641">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-641">Description</span></span>    | <span data-ttu-id="fed15-642">Indique si l’écouteur de composants en file d’attente est activé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="fed15-643">S’il est activé, l’écouteur est lancé au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="fed15-644">Cette propriété prend effet uniquement si QueuingEnabled a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fed15-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="fed15-645">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-645">Access</span></span>         | <span data-ttu-id="fed15-646">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="fed15-647">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-647">Type</span></span>           | <span data-ttu-id="fed15-648">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="fed15-649">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-649">Default</span></span>        | <span data-ttu-id="fed15-650">False</span><span class="sxs-lookup"><span data-stu-id="fed15-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="fed15-651">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-651">Minimum system</span></span> | <span data-ttu-id="fed15-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="fed15-653">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-653">QueuingEnabled</span></span>



| <span data-ttu-id="fed15-654">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-654">Entry</span></span> | <span data-ttu-id="fed15-655">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-656">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-656">Description</span></span>    | <span data-ttu-id="fed15-657">Indique si le service de composants en file d’attente COM+ est activé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="fed15-658">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-658">Access</span></span>         | <span data-ttu-id="fed15-659">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="fed15-660">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-660">Type</span></span>           | <span data-ttu-id="fed15-661">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="fed15-662">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-662">Default</span></span>        | <span data-ttu-id="fed15-663">False</span><span class="sxs-lookup"><span data-stu-id="fed15-663">False</span></span>                                                                                |
| <span data-ttu-id="fed15-664">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-664">Minimum system</span></span> | <span data-ttu-id="fed15-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="fed15-666">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="fed15-667">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-667">Entry</span></span> | <span data-ttu-id="fed15-668">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-669">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-669">Description</span></span>    | <span data-ttu-id="fed15-670">Indique le nombre maximal d’activations d’objets configurés dans l’application à accepter avant de recycler le processus.</span><span class="sxs-lookup"><span data-stu-id="fed15-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="fed15-671">Le nombre d’activations par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="fed15-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="fed15-672">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-672">Access</span></span>         | <span data-ttu-id="fed15-673">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="fed15-674">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-674">Type</span></span>           | <span data-ttu-id="fed15-675">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="fed15-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="fed15-676">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-676">Default</span></span>        | <span data-ttu-id="fed15-677">0</span><span class="sxs-lookup"><span data-stu-id="fed15-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="fed15-678">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-678">Minimum system</span></span> | <span data-ttu-id="fed15-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="fed15-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-680">RecycleCallLimit</span></span>



| <span data-ttu-id="fed15-681">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-681">Entry</span></span> | <span data-ttu-id="fed15-682">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-683">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-683">Description</span></span>    | <span data-ttu-id="fed15-684">Indique le nombre maximal d’appels pour autoriser les objets configurés dans l’application à accepter avant de recycler le processus.</span><span class="sxs-lookup"><span data-stu-id="fed15-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="fed15-685">Le nombre d’appels par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="fed15-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="fed15-686">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-686">Access</span></span>         | <span data-ttu-id="fed15-687">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="fed15-688">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-688">Type</span></span>           | <span data-ttu-id="fed15-689">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="fed15-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="fed15-690">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-690">Default</span></span>        | <span data-ttu-id="fed15-691">0</span><span class="sxs-lookup"><span data-stu-id="fed15-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="fed15-692">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-692">Minimum system</span></span> | <span data-ttu-id="fed15-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="fed15-694">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="fed15-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="fed15-695">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-695">Entry</span></span> | <span data-ttu-id="fed15-696">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-697">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-697">Description</span></span>    | <span data-ttu-id="fed15-698">Indique la durée (en minutes) nécessaire à l’exécution d’un processus recyclé avant son arrêt.</span><span class="sxs-lookup"><span data-stu-id="fed15-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="fed15-699">Le compte à rebours commence immédiatement après le recyclage du processus.</span><span class="sxs-lookup"><span data-stu-id="fed15-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="fed15-700">Le délai d’expiration maximal est de 1440 minutes (24 heures) et la valeur par défaut est 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="fed15-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="fed15-701">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-701">Access</span></span>         | <span data-ttu-id="fed15-702">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="fed15-703">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-703">Type</span></span>           | <span data-ttu-id="fed15-704">Long (1-1440)</span><span class="sxs-lookup"><span data-stu-id="fed15-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-705">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-705">Default</span></span>        | <span data-ttu-id="fed15-706">15</span><span class="sxs-lookup"><span data-stu-id="fed15-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fed15-707">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-707">Minimum system</span></span> | <span data-ttu-id="fed15-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="fed15-709">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="fed15-710">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-710">Entry</span></span> | <span data-ttu-id="fed15-711">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-712">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-712">Description</span></span>    | <span data-ttu-id="fed15-713">Indique le nombre maximal de minutes pendant lesquelles un processus doit être exécuté avant de le recycler.</span><span class="sxs-lookup"><span data-stu-id="fed15-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="fed15-714">La limite de durée de vie maximale est de 30240 minutes (21 jours) et la valeur par défaut est 0 minute.</span><span class="sxs-lookup"><span data-stu-id="fed15-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="fed15-715">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-715">Access</span></span>         | <span data-ttu-id="fed15-716">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="fed15-717">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-717">Type</span></span>           | <span data-ttu-id="fed15-718">Long (0-30240)</span><span class="sxs-lookup"><span data-stu-id="fed15-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="fed15-719">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-719">Default</span></span>        | <span data-ttu-id="fed15-720">0</span><span class="sxs-lookup"><span data-stu-id="fed15-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="fed15-721">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-721">Minimum system</span></span> | <span data-ttu-id="fed15-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="fed15-723">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="fed15-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="fed15-724">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-724">Entry</span></span> | <span data-ttu-id="fed15-725">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-726">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-726">Description</span></span>    | <span data-ttu-id="fed15-727">Indique la quantité maximale d’utilisation de la mémoire (en kilo-octets) autorisée pour un processus avant son recyclage.</span><span class="sxs-lookup"><span data-stu-id="fed15-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="fed15-728">Si l’utilisation de la mémoire de processus dépasse le nombre spécifié pendant une période supérieure à une minute, le processus est recyclé.</span><span class="sxs-lookup"><span data-stu-id="fed15-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="fed15-729">La quantité d’utilisation de la mémoire par défaut est de 0 Ko.</span><span class="sxs-lookup"><span data-stu-id="fed15-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="fed15-730">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-730">Access</span></span>         | <span data-ttu-id="fed15-731">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fed15-732">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-732">Type</span></span>           | <span data-ttu-id="fed15-733">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="fed15-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fed15-734">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-734">Default</span></span>        | <span data-ttu-id="fed15-735">0</span><span class="sxs-lookup"><span data-stu-id="fed15-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fed15-736">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-736">Minimum system</span></span> | <span data-ttu-id="fed15-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="fed15-738">Replicable</span><span class="sxs-lookup"><span data-stu-id="fed15-738">Replicable</span></span>



| <span data-ttu-id="fed15-739">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-739">Entry</span></span> | <span data-ttu-id="fed15-740">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="fed15-741">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-741">Description</span></span>    | <span data-ttu-id="fed15-742">Indique si l’application peut être répliquée.</span><span class="sxs-lookup"><span data-stu-id="fed15-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="fed15-743">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-743">Access</span></span>         | <span data-ttu-id="fed15-744">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="fed15-745">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-745">Type</span></span>           | <span data-ttu-id="fed15-746">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-746">Bool</span></span>                                                 |
| <span data-ttu-id="fed15-747">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-747">Default</span></span>        | <span data-ttu-id="fed15-748">Vrai</span><span class="sxs-lookup"><span data-stu-id="fed15-748">True</span></span>                                                 |
| <span data-ttu-id="fed15-749">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-749">Minimum system</span></span> | <span data-ttu-id="fed15-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="fed15-751">RunForever</span><span class="sxs-lookup"><span data-stu-id="fed15-751">RunForever</span></span>



| <span data-ttu-id="fed15-752">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-752">Entry</span></span> | <span data-ttu-id="fed15-753">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-754">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-754">Description</span></span>    | <span data-ttu-id="fed15-755">Permet à un processus serveur de continuer si une application est inactive.</span><span class="sxs-lookup"><span data-stu-id="fed15-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="fed15-756">Si la valeur est true, le processus serveur ne s’arrête pas quand il est resté inactif.</span><span class="sxs-lookup"><span data-stu-id="fed15-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="fed15-757">Si la valeur est false, le processus s’arrête en fonction de la valeur définie par la propriété ShutdownAfter.</span><span class="sxs-lookup"><span data-stu-id="fed15-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="fed15-758">RunForever n’est pas activé pour les applications de bibliothèque (in-process).</span><span class="sxs-lookup"><span data-stu-id="fed15-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="fed15-759">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-759">Access</span></span>         | <span data-ttu-id="fed15-760">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="fed15-761">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-761">Type</span></span>           | <span data-ttu-id="fed15-762">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="fed15-763">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-763">Default</span></span>        | <span data-ttu-id="fed15-764">False</span><span class="sxs-lookup"><span data-stu-id="fed15-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-765">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-765">Minimum system</span></span> | <span data-ttu-id="fed15-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="fed15-767">NomService</span><span class="sxs-lookup"><span data-stu-id="fed15-767">ServiceName</span></span>



| <span data-ttu-id="fed15-768">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-768">Entry</span></span> | <span data-ttu-id="fed15-769">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-770">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-770">Description</span></span>    | <span data-ttu-id="fed15-771">Nom du service correspondant à l’application configurée pour s’exécuter en tant qu’application de service.</span><span class="sxs-lookup"><span data-stu-id="fed15-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="fed15-772">Si cette valeur est **null**, l’application n’est pas configurée pour s’exécuter en tant que service.</span><span class="sxs-lookup"><span data-stu-id="fed15-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="fed15-773">Dans le cas contraire, les informations de configuration du service sont disponibles à l’aide du nom du service.</span><span class="sxs-lookup"><span data-stu-id="fed15-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="fed15-774">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-774">Access</span></span>         | <span data-ttu-id="fed15-775">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fed15-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fed15-776">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-776">Type</span></span>           | <span data-ttu-id="fed15-777">String</span><span class="sxs-lookup"><span data-stu-id="fed15-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fed15-778">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-778">Default</span></span>        | <span data-ttu-id="fed15-779">""</span><span class="sxs-lookup"><span data-stu-id="fed15-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fed15-780">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-780">Minimum system</span></span> | <span data-ttu-id="fed15-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="fed15-782">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="fed15-782">ShutdownAfter</span></span>



| <span data-ttu-id="fed15-783">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-783">Entry</span></span> | <span data-ttu-id="fed15-784">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-785">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-785">Description</span></span>    | <span data-ttu-id="fed15-786">Définit le délai avant l’arrêt d’un processus serveur lorsqu’il devient inactif.</span><span class="sxs-lookup"><span data-stu-id="fed15-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="fed15-787">La latence d’arrêt est comprise entre 0 et 1440 minutes (24 heures).</span><span class="sxs-lookup"><span data-stu-id="fed15-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="fed15-788">Si RunForever a la valeur true, cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="fed15-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="fed15-789">ShutdownAfter n’est pas activé pour les applications de bibliothèque (in-process).</span><span class="sxs-lookup"><span data-stu-id="fed15-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="fed15-790">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-790">Access</span></span>         | <span data-ttu-id="fed15-791">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fed15-792">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-792">Type</span></span>           | <span data-ttu-id="fed15-793">Long (0-1440)</span><span class="sxs-lookup"><span data-stu-id="fed15-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fed15-794">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-794">Default</span></span>        | <span data-ttu-id="fed15-795">3</span><span class="sxs-lookup"><span data-stu-id="fed15-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fed15-796">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-796">Minimum system</span></span> | <span data-ttu-id="fed15-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fed15-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="fed15-798">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="fed15-798">SoapActivated</span></span>



| <span data-ttu-id="fed15-799">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-799">Entry</span></span> | <span data-ttu-id="fed15-800">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-801">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-801">Description</span></span>    | <span data-ttu-id="fed15-802">Indique si cette application est exposée pour être consommée via le protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="fed15-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="fed15-803">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-803">Access</span></span>         | <span data-ttu-id="fed15-804">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="fed15-805">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-805">Type</span></span>           | <span data-ttu-id="fed15-806">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="fed15-807">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-807">Default</span></span>        | <span data-ttu-id="fed15-808">False</span><span class="sxs-lookup"><span data-stu-id="fed15-808">False</span></span>                                                                                |
| <span data-ttu-id="fed15-809">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-809">Minimum system</span></span> | <span data-ttu-id="fed15-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed15-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="fed15-811">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="fed15-811">SoapBaseUrl</span></span>



| <span data-ttu-id="fed15-812">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-812">Entry</span></span> | <span data-ttu-id="fed15-813">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-814">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-814">Description</span></span>    | <span data-ttu-id="fed15-815">Point de terminaison d’URL auquel cette application est exposée via le protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="fed15-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="fed15-816">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-816">Access</span></span>         | <span data-ttu-id="fed15-817">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="fed15-818">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-818">Type</span></span>           | <span data-ttu-id="fed15-819">String</span><span class="sxs-lookup"><span data-stu-id="fed15-819">String</span></span>                                                                       |
| <span data-ttu-id="fed15-820">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-820">Default</span></span>        | <span data-ttu-id="fed15-821">""</span><span class="sxs-lookup"><span data-stu-id="fed15-821">""</span></span>                                                                           |
| <span data-ttu-id="fed15-822">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-822">Minimum system</span></span> | <span data-ttu-id="fed15-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed15-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="fed15-824">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="fed15-824">SoapMailTo</span></span>



| <span data-ttu-id="fed15-825">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-825">Entry</span></span> | <span data-ttu-id="fed15-826">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-827">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-827">Description</span></span>    | <span data-ttu-id="fed15-828">Adresse de messagerie à laquelle cette application est exposée par le biais du protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="fed15-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="fed15-829">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-829">Access</span></span>         | <span data-ttu-id="fed15-830">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="fed15-831">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-831">Type</span></span>           | <span data-ttu-id="fed15-832">String</span><span class="sxs-lookup"><span data-stu-id="fed15-832">String</span></span>                                                                        |
| <span data-ttu-id="fed15-833">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-833">Default</span></span>        | <span data-ttu-id="fed15-834">""</span><span class="sxs-lookup"><span data-stu-id="fed15-834">""</span></span>                                                                            |
| <span data-ttu-id="fed15-835">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-835">Minimum system</span></span> | <span data-ttu-id="fed15-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed15-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="fed15-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="fed15-837">SoapVRoot</span></span>



| <span data-ttu-id="fed15-838">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-838">Entry</span></span> | <span data-ttu-id="fed15-839">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-840">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-840">Description</span></span>    | <span data-ttu-id="fed15-841">Répertoire racine virtuel IIS dans lequel les scripts d’accès qui exposent l’application via le protocole SOAP résident.</span><span class="sxs-lookup"><span data-stu-id="fed15-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="fed15-842">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-842">Access</span></span>         | <span data-ttu-id="fed15-843">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="fed15-844">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-844">Type</span></span>           | <span data-ttu-id="fed15-845">String</span><span class="sxs-lookup"><span data-stu-id="fed15-845">String</span></span>                                                                                                               |
| <span data-ttu-id="fed15-846">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fed15-846">Default</span></span>        | <span data-ttu-id="fed15-847">""</span><span class="sxs-lookup"><span data-stu-id="fed15-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="fed15-848">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-848">Minimum system</span></span> | <span data-ttu-id="fed15-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fed15-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="fed15-850">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="fed15-850">SRPEnabled</span></span>



| <span data-ttu-id="fed15-851">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-851">Entry</span></span> | <span data-ttu-id="fed15-852">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-853">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-853">Description</span></span>    | <span data-ttu-id="fed15-854">Détermine la stratégie de restriction logicielle (SRP) pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="fed15-855">Si la valeur est true, la propriété SRPTrustLevel de l’application est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fed15-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="fed15-856">Si la valeur est false, les stratégies de restriction logicielle des paramètres de sécurité locaux sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="fed15-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="fed15-857">Les paramètres de sécurité locaux sont contrôlés par le biais du composant logiciel enfichable Stratégie de sécurité locale de la console MMC (Microsoft Management Console).</span><span class="sxs-lookup"><span data-stu-id="fed15-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="fed15-858">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-858">Access</span></span>         | <span data-ttu-id="fed15-859">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fed15-860">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-860">Type</span></span>           | <span data-ttu-id="fed15-861">Bool</span><span class="sxs-lookup"><span data-stu-id="fed15-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fed15-862">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-862">Default</span></span>        | <span data-ttu-id="fed15-863">False</span><span class="sxs-lookup"><span data-stu-id="fed15-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fed15-864">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-864">Minimum system</span></span> | <span data-ttu-id="fed15-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="fed15-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="fed15-866">SRPTrustLevel</span></span>



| <span data-ttu-id="fed15-867">Entrée</span><span class="sxs-lookup"><span data-stu-id="fed15-867">Entry</span></span> | <span data-ttu-id="fed15-868">Valeur</span><span class="sxs-lookup"><span data-stu-id="fed15-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed15-869">Description</span><span class="sxs-lookup"><span data-stu-id="fed15-869">Description</span></span>    | <span data-ttu-id="fed15-870">Indique le niveau de confiance de la stratégie de restriction logicielle (SRP) de l’application.</span><span class="sxs-lookup"><span data-stu-id="fed15-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="fed15-871">Cette propriété est utilisée uniquement si la propriété SRPEnabled a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fed15-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="fed15-872">Le niveau de confiance du SRP fait référence au niveau de confiance que vous êtes prêt à accorder à une application.</span><span class="sxs-lookup"><span data-stu-id="fed15-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="fed15-873">Un niveau de confiance SRP non restreint correspond à la \_ valeur enum LEVELID FULLYTRUSTED plus sécurisée \_ , tandis qu’un niveau de confiance SRP non autorisé correspond à la \_ valeur enum non autorisée LEVELID plus sûre \_ .</span><span class="sxs-lookup"><span data-stu-id="fed15-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="fed15-874">L’énumération pour les niveaux de confiance est définie dans Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="fed15-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="fed15-875">Accès</span><span class="sxs-lookup"><span data-stu-id="fed15-875">Access</span></span>         | <span data-ttu-id="fed15-876">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fed15-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fed15-877">Type</span><span class="sxs-lookup"><span data-stu-id="fed15-877">Type</span></span>           | <span data-ttu-id="fed15-878">Valeurs possibles longues : LEVELID sécurisé \_ non \_ autorisé (0x0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="fed15-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fed15-879">Default</span><span class="sxs-lookup"><span data-stu-id="fed15-879">Default</span></span>        | <span data-ttu-id="fed15-880">SÉCURITÉ \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="fed15-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fed15-881">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fed15-881">Minimum system</span></span> | <span data-ttu-id="fed15-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fed15-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="fed15-883">Une application que vous êtes disposé à approuver avec un accès non restreint doit avoir la sécurité la plus stricte qui lui est attachée.</span><span class="sxs-lookup"><span data-stu-id="fed15-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="fed15-884">Les applications non restreintes ne peuvent charger que des composants non restreints, tandis que les applications non autorisées ne sont pas autorisées à s’exécuter et ne peuvent donc pas charger de composants.</span><span class="sxs-lookup"><span data-stu-id="fed15-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="fed15-885">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fed15-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed15-886">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="fed15-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
