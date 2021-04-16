---
description: Contient un objet pour chaque composant de l’application associée.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Collection de composants
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524215"
---
# <a name="components-collection"></a><span data-ttu-id="f1862-103">Collection de composants</span><span class="sxs-lookup"><span data-stu-id="f1862-103">Components collection</span></span>

<span data-ttu-id="f1862-104">Contient un objet pour chaque composant de l’application associée.</span><span class="sxs-lookup"><span data-stu-id="f1862-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="f1862-105">La collection de **composants** est toujours liée à un objet dans la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="f1862-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="f1862-106">Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="f1862-107">Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="f1862-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="f1862-108">Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="f1862-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f1862-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f1862-109">Members</span></span>

<span data-ttu-id="f1862-110">La collection **Components** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f1862-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f1862-111">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="f1862-111">Related Collections</span></span>

<span data-ttu-id="f1862-112">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="f1862-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f1862-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f1862-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f1862-114">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f1862-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="f1862-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f1862-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f1862-116">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f1862-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="f1862-117">**RolesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f1862-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="f1862-118">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="f1862-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="f1862-119">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="f1862-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f1862-120">**Applications**</span><span class="sxs-lookup"><span data-stu-id="f1862-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="f1862-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1862-121">Properties</span></span>

<span data-ttu-id="f1862-122">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="f1862-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f1862-123">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="f1862-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="f1862-124">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="f1862-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="f1862-125">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="f1862-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="f1862-126">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="f1862-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="f1862-127">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="f1862-128">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f1862-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="f1862-129">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="f1862-130">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f1862-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="f1862-131">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="f1862-132">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="f1862-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="f1862-133">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="f1862-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="f1862-134">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-134">Description</span></span>](#description)
-   [<span data-ttu-id="f1862-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f1862-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="f1862-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="f1862-137">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="f1862-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="f1862-138">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="f1862-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="f1862-139">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f1862-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="f1862-140">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="f1862-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="f1862-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="f1862-142">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="f1862-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="f1862-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="f1862-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="f1862-144">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f1862-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="f1862-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="f1862-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="f1862-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="f1862-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="f1862-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="f1862-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="f1862-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="f1862-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="f1862-149">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="f1862-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="f1862-150">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="f1862-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="f1862-151">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f1862-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="f1862-152">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="f1862-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="f1862-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="f1862-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="f1862-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="f1862-155">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="f1862-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="f1862-156">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="f1862-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="f1862-157">Synchronisation</span><span class="sxs-lookup"><span data-stu-id="f1862-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="f1862-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f1862-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="f1862-159">Transaction</span><span class="sxs-lookup"><span data-stu-id="f1862-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="f1862-160">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="f1862-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="f1862-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="f1862-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="f1862-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="f1862-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="f1862-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="f1862-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="f1862-164">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="f1862-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="f1862-165">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="f1862-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="f1862-166">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-166">Entry</span></span> | <span data-ttu-id="f1862-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="f1862-168">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-168">Description</span></span>    | <span data-ttu-id="f1862-169">Active les abonnés au processus si le composant est une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1862-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="f1862-170">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-170">Access</span></span>         | <span data-ttu-id="f1862-171">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="f1862-172">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-172">Type</span></span>           | <span data-ttu-id="f1862-173">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-173">Bool</span></span>                                                               |
| <span data-ttu-id="f1862-174">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-174">Default</span></span>        | <span data-ttu-id="f1862-175">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1862-175">True</span></span>                                                               |
| <span data-ttu-id="f1862-176">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-176">Minimum system</span></span> | <span data-ttu-id="f1862-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="f1862-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="f1862-178">ApplicationID</span></span>



| <span data-ttu-id="f1862-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-179">Entry</span></span> | <span data-ttu-id="f1862-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-181">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-181">Description</span></span>    | <span data-ttu-id="f1862-182">GUID de l’application contenant le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="f1862-183">Doit être un GUID d’application valide, qui est vérifié avant l’appel de [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="f1862-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="f1862-184">Si cette valeur est remplacée par un GUID pour une autre application, le composant se déplace vers cette application.</span><span class="sxs-lookup"><span data-stu-id="f1862-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="f1862-185">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-185">Access</span></span>         | <span data-ttu-id="f1862-186">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f1862-187">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-187">Type</span></span>           | <span data-ttu-id="f1862-188">String</span><span class="sxs-lookup"><span data-stu-id="f1862-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f1862-189">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-189">Default</span></span>        | <span data-ttu-id="f1862-190">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f1862-191">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-191">Minimum system</span></span> | <span data-ttu-id="f1862-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="f1862-193">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="f1862-193">Bitness</span></span>



| <span data-ttu-id="f1862-194">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-194">Entry</span></span> | <span data-ttu-id="f1862-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-196">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-196">Description</span></span>    | <span data-ttu-id="f1862-197">Représente le type de bits binaire d’un composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="f1862-198">Sur les systèmes qui utilisent Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f1862-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="f1862-199">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-199">Access</span></span>         | <span data-ttu-id="f1862-200">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="f1862-201">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-201">Type</span></span>           | <span data-ttu-id="f1862-202">Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="f1862-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="f1862-203">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-203">Default</span></span>        | <span data-ttu-id="f1862-204">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f1862-205">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-205">Minimum system</span></span> | <span data-ttu-id="f1862-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1862-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="f1862-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1862-207">CLSID</span></span>



| <span data-ttu-id="f1862-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-208">Entry</span></span> | <span data-ttu-id="f1862-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-210">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-210">Description</span></span>    | <span data-ttu-id="f1862-211">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-211">A GUID for the component.</span></span> <span data-ttu-id="f1862-212">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="f1862-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f1862-213">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-213">Access</span></span>         | <span data-ttu-id="f1862-214">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="f1862-215">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-215">Type</span></span>           | <span data-ttu-id="f1862-216">String</span><span class="sxs-lookup"><span data-stu-id="f1862-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="f1862-217">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-217">Default</span></span>        | <span data-ttu-id="f1862-218">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="f1862-219">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-219">Minimum system</span></span> | <span data-ttu-id="f1862-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="f1862-221">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="f1862-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-222">Entry</span></span> | <span data-ttu-id="f1862-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-224">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-224">Description</span></span>    | <span data-ttu-id="f1862-225">Indique si les contrôles d’accès basés sur les rôles sont effectués sur les appels au composant et fonctionnent conjointement avec les propriétés AccessChecksLevel et ApplicationAccessChecksEnabled de l’application.</span><span class="sxs-lookup"><span data-stu-id="f1862-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="f1862-226">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-226">Access</span></span>         | <span data-ttu-id="f1862-227">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="f1862-228">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-228">Type</span></span>           | <span data-ttu-id="f1862-229">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="f1862-230">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-230">Default</span></span>        | <span data-ttu-id="f1862-231">False</span><span class="sxs-lookup"><span data-stu-id="f1862-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="f1862-232">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-232">Minimum system</span></span> | <span data-ttu-id="f1862-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="f1862-234">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f1862-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="f1862-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-235">Entry</span></span> | <span data-ttu-id="f1862-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-237">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-237">Description</span></span>    | <span data-ttu-id="f1862-238">En cas d’utilisation dans une transaction, spécifie la période pendant laquelle ce composant provoque l’expiration du délai d’attente de la transaction. La valeur par défaut est 60 secondes et ne peut pas dépasser 3600 secondes (1 heure).</span><span class="sxs-lookup"><span data-stu-id="f1862-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="f1862-239">La valeur du délai d’attente peut être définie sur 0, en spécifiant un délai d’expiration de transaction infini.</span><span class="sxs-lookup"><span data-stu-id="f1862-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="f1862-240">Pour que cette propriété soit utilisée, ComponentTransactionTimeoutEnabled doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="f1862-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="f1862-241">La valeur de cette propriété remplace le délai d’expiration de la transaction globale spécifié par la propriété TransactionTimeout de la collection [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="f1862-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="f1862-242">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-242">Access</span></span>         | <span data-ttu-id="f1862-243">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f1862-244">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-244">Type</span></span>           | <span data-ttu-id="f1862-245">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="f1862-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f1862-246">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-246">Default</span></span>        | <span data-ttu-id="f1862-247">60</span><span class="sxs-lookup"><span data-stu-id="f1862-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f1862-248">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-248">Minimum system</span></span> | <span data-ttu-id="f1862-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="f1862-250">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="f1862-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-251">Entry</span></span> | <span data-ttu-id="f1862-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-253">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-253">Description</span></span>    | <span data-ttu-id="f1862-254">Spécifie si le délai d’expiration de la transaction est activé pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="f1862-255">Par défaut, la fonctionnalité de délai d’expiration de la transaction est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f1862-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="f1862-256">Lorsque cette propriété a la valeur true, le délai d’attente spécifié par ComponentTransactionTimeout est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f1862-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="f1862-257">Lorsque cette propriété a la valeur false, le délai d’attente spécifié par la propriété TransactionTimeout de la collection [**LocalComputer**](localcomputer.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f1862-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="f1862-258">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-258">Access</span></span>         | <span data-ttu-id="f1862-259">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f1862-260">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-260">Type</span></span>           | <span data-ttu-id="f1862-261">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f1862-262">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-262">Default</span></span>        | <span data-ttu-id="f1862-263">False</span><span class="sxs-lookup"><span data-stu-id="f1862-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f1862-264">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-264">Minimum system</span></span> | <span data-ttu-id="f1862-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="f1862-266">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f1862-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="f1862-267">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-267">Entry</span></span> | <span data-ttu-id="f1862-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-269">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-269">Description</span></span>    | <span data-ttu-id="f1862-270">Permet de passer des propriétés de contexte du COM Transaction Integrator (COMTI) dans le contexte de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1862-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="f1862-271">Le composant COMTI facilite l’encapsulation des transactions de macroordinateurs et de la logique métier en tant que composants COM.</span><span class="sxs-lookup"><span data-stu-id="f1862-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="f1862-272">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-272">Access</span></span>         | <span data-ttu-id="f1862-273">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="f1862-274">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-274">Type</span></span>           | <span data-ttu-id="f1862-275">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="f1862-276">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-276">Default</span></span>        | <span data-ttu-id="f1862-277">False</span><span class="sxs-lookup"><span data-stu-id="f1862-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="f1862-278">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-278">Minimum system</span></span> | <span data-ttu-id="f1862-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="f1862-280">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-280">ConstructionEnabled</span></span>



| <span data-ttu-id="f1862-281">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-281">Entry</span></span> | <span data-ttu-id="f1862-282">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-283">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-283">Description</span></span>    | <span data-ttu-id="f1862-284">Détermine si le ConstructorString est passé à l’objet lors de sa construction.</span><span class="sxs-lookup"><span data-stu-id="f1862-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="f1862-285">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-285">Access</span></span>         | <span data-ttu-id="f1862-286">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="f1862-287">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-287">Type</span></span>           | <span data-ttu-id="f1862-288">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="f1862-289">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-289">Default</span></span>        | <span data-ttu-id="f1862-290">False</span><span class="sxs-lookup"><span data-stu-id="f1862-290">False</span></span>                                                                                    |
| <span data-ttu-id="f1862-291">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-291">Minimum system</span></span> | <span data-ttu-id="f1862-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="f1862-293">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="f1862-293">ConstructorString</span></span>



| <span data-ttu-id="f1862-294">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-294">Entry</span></span> | <span data-ttu-id="f1862-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-296">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-296">Description</span></span>    | <span data-ttu-id="f1862-297">Chaîne d’initialisation pour la construction du composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-297">Initialization string for component construction.</span></span> <span data-ttu-id="f1862-298">Vous pouvez créer différents objets à partir du même composant générique en utilisant des chaînes de constructeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="f1862-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="f1862-299">Si ConstructionEnabled a la valeur false, cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f1862-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="f1862-300">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-300">Access</span></span>         | <span data-ttu-id="f1862-301">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f1862-302">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-302">Type</span></span>           | <span data-ttu-id="f1862-303">String</span><span class="sxs-lookup"><span data-stu-id="f1862-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="f1862-304">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-304">Default</span></span>        | <span data-ttu-id="f1862-305">""</span><span class="sxs-lookup"><span data-stu-id="f1862-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="f1862-306">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-306">Minimum system</span></span> | <span data-ttu-id="f1862-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="f1862-308">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="f1862-308">CreationTimeout</span></span>



| <span data-ttu-id="f1862-309">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-309">Entry</span></span> | <span data-ttu-id="f1862-310">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-311">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-311">Description</span></span>    | <span data-ttu-id="f1862-312">Lors de la création de l’objet, nombre de millisecondes avant qu’une erreur de délai d’attente soit renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f1862-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="f1862-313">Le délai d’expiration maximal est de 2147483647 millisecondes (environ 25 jours).</span><span class="sxs-lookup"><span data-stu-id="f1862-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="f1862-314">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-314">Access</span></span>         | <span data-ttu-id="f1862-315">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="f1862-316">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-316">Type</span></span>           | <span data-ttu-id="f1862-317">Long (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="f1862-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="f1862-318">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-318">Default</span></span>        | <span data-ttu-id="f1862-319">0</span><span class="sxs-lookup"><span data-stu-id="f1862-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="f1862-320">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-320">Minimum system</span></span> | <span data-ttu-id="f1862-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="f1862-322">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-322">Description</span></span>



| <span data-ttu-id="f1862-323">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-323">Entry</span></span> | <span data-ttu-id="f1862-324">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="f1862-325">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-325">Description</span></span>    | <span data-ttu-id="f1862-326">Décrit le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-326">Describes the component.</span></span> |
| <span data-ttu-id="f1862-327">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-327">Access</span></span>         | <span data-ttu-id="f1862-328">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-328">ReadWrite</span></span>                |
| <span data-ttu-id="f1862-329">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-329">Type</span></span>           | <span data-ttu-id="f1862-330">String</span><span class="sxs-lookup"><span data-stu-id="f1862-330">String</span></span>                   |
| <span data-ttu-id="f1862-331">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-331">Default</span></span>        | <span data-ttu-id="f1862-332">""</span><span class="sxs-lookup"><span data-stu-id="f1862-332">""</span></span>                       |
| <span data-ttu-id="f1862-333">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-333">Minimum system</span></span> | <span data-ttu-id="f1862-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="f1862-335">DLL</span><span class="sxs-lookup"><span data-stu-id="f1862-335">DLL</span></span>



| <span data-ttu-id="f1862-336">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-336">Entry</span></span> | <span data-ttu-id="f1862-337">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="f1862-338">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-338">Description</span></span>    | <span data-ttu-id="f1862-339">Nom et chemin d’accès du fichier contenant le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="f1862-340">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-340">Access</span></span>         | <span data-ttu-id="f1862-341">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="f1862-342">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-342">Type</span></span>           | <span data-ttu-id="f1862-343">String</span><span class="sxs-lookup"><span data-stu-id="f1862-343">String</span></span>                                                  |
| <span data-ttu-id="f1862-344">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-344">Default</span></span>        | <span data-ttu-id="f1862-345">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-345">N/A</span></span>                                                     |
| <span data-ttu-id="f1862-346">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-346">Minimum system</span></span> | <span data-ttu-id="f1862-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="f1862-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="f1862-349">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-349">Entry</span></span> | <span data-ttu-id="f1862-350">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-351">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-351">Description</span></span>    | <span data-ttu-id="f1862-352">Détermine si les événements sont suivis.</span><span class="sxs-lookup"><span data-stu-id="f1862-352">Determines whether events are tracked.</span></span> <span data-ttu-id="f1862-353">Les événements incluent des actions telles que l’arrêt de l’application ; création et publication d’objets ; références d’objet, cohérence, activation et désactivation ; appels de méthode, retours et exceptions ; démarrage de la transaction, préparation à la validation et abandon ; connexion, allocation et recyclage des distributions de ressources ; allocation et recyclage des threads.</span><span class="sxs-lookup"><span data-stu-id="f1862-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="f1862-354">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-354">Access</span></span>         | <span data-ttu-id="f1862-355">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f1862-356">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-356">Type</span></span>           | <span data-ttu-id="f1862-357">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f1862-358">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-358">Default</span></span>        | <span data-ttu-id="f1862-359">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1862-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f1862-360">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-360">Minimum system</span></span> | <span data-ttu-id="f1862-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="f1862-362">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="f1862-362">ExceptionClass</span></span>



| <span data-ttu-id="f1862-363">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-363">Entry</span></span> | <span data-ttu-id="f1862-364">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-365">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-365">Description</span></span>    | <span data-ttu-id="f1862-366">CLSID, qui peut être un GUID ou une chaîne de moniker, pour activer un autre programme pendant le processus de traitement d’un programme de composants en file d’attente qui échoue à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="f1862-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="f1862-367">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-367">Access</span></span>         | <span data-ttu-id="f1862-368">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f1862-369">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-369">Type</span></span>           | <span data-ttu-id="f1862-370">String</span><span class="sxs-lookup"><span data-stu-id="f1862-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f1862-371">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-371">Default</span></span>        | <span data-ttu-id="f1862-372">""</span><span class="sxs-lookup"><span data-stu-id="f1862-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="f1862-373">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-373">Minimum system</span></span> | <span data-ttu-id="f1862-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="f1862-375">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="f1862-375">FireInParallel</span></span>



| <span data-ttu-id="f1862-376">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-376">Entry</span></span> | <span data-ttu-id="f1862-377">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f1862-378">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-378">Description</span></span>    | <span data-ttu-id="f1862-379">Active les événements à déclencher en parallèle si le composant est une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1862-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="f1862-380">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-380">Access</span></span>         | <span data-ttu-id="f1862-381">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="f1862-382">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-382">Type</span></span>           | <span data-ttu-id="f1862-383">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-383">Bool</span></span>                                                                       |
| <span data-ttu-id="f1862-384">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-384">Default</span></span>        | <span data-ttu-id="f1862-385">False</span><span class="sxs-lookup"><span data-stu-id="f1862-385">False</span></span>                                                                      |
| <span data-ttu-id="f1862-386">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-386">Minimum system</span></span> | <span data-ttu-id="f1862-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="f1862-388">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f1862-388">IISIntrinsics</span></span>



| <span data-ttu-id="f1862-389">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-389">Entry</span></span> | <span data-ttu-id="f1862-390">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-391">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-391">Description</span></span>    | <span data-ttu-id="f1862-392">Permet de passer des propriétés de contexte IIS, telles qu’un objet de session d’application ou un objet de session utilisateur, dans le contexte de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1862-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="f1862-393">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-393">Access</span></span>         | <span data-ttu-id="f1862-394">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="f1862-395">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-395">Type</span></span>           | <span data-ttu-id="f1862-396">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="f1862-397">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-397">Default</span></span>        | <span data-ttu-id="f1862-398">False</span><span class="sxs-lookup"><span data-stu-id="f1862-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="f1862-399">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-399">Minimum system</span></span> | <span data-ttu-id="f1862-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="f1862-401">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="f1862-401">InitializeServerApplication</span></span>



| <span data-ttu-id="f1862-402">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-402">Entry</span></span> | <span data-ttu-id="f1862-403">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f1862-404">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-404">Description</span></span>    | <span data-ttu-id="f1862-405">Indique si le composant est utilisé pour initialiser une application serveur.</span><span class="sxs-lookup"><span data-stu-id="f1862-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="f1862-406">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-406">Access</span></span>         | <span data-ttu-id="f1862-407">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="f1862-408">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-408">Type</span></span>           | <span data-ttu-id="f1862-409">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-409">Bool</span></span>                                                                        |
| <span data-ttu-id="f1862-410">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-410">Default</span></span>        | <span data-ttu-id="f1862-411">False</span><span class="sxs-lookup"><span data-stu-id="f1862-411">False</span></span>                                                                       |
| <span data-ttu-id="f1862-412">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-412">Minimum system</span></span> | <span data-ttu-id="f1862-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1862-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="f1862-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-414">IsEnabled</span></span>



| <span data-ttu-id="f1862-415">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-415">Entry</span></span> | <span data-ttu-id="f1862-416">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-417">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-417">Description</span></span>    | <span data-ttu-id="f1862-418">False si l’application ou le composant COM+ est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f1862-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="f1862-419">Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="f1862-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="f1862-420">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-420">Access</span></span>         | <span data-ttu-id="f1862-421">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="f1862-422">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-422">Type</span></span>           | <span data-ttu-id="f1862-423">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="f1862-424">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-424">Default</span></span>        | <span data-ttu-id="f1862-425">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1862-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="f1862-426">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-426">Minimum system</span></span> | <span data-ttu-id="f1862-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1862-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="f1862-428">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="f1862-428">IsEventClass</span></span>



| <span data-ttu-id="f1862-429">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-429">Entry</span></span> | <span data-ttu-id="f1862-430">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="f1862-431">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-431">Description</span></span>    | <span data-ttu-id="f1862-432">Indique si le composant est une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1862-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="f1862-433">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-433">Access</span></span>         | <span data-ttu-id="f1862-434">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="f1862-435">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-435">Type</span></span>           | <span data-ttu-id="f1862-436">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-436">Bool</span></span>                                               |
| <span data-ttu-id="f1862-437">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-437">Default</span></span>        | <span data-ttu-id="f1862-438">False</span><span class="sxs-lookup"><span data-stu-id="f1862-438">False</span></span>                                              |
| <span data-ttu-id="f1862-439">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-439">Minimum system</span></span> | <span data-ttu-id="f1862-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="f1862-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="f1862-441">IsInstalled</span></span>



| <span data-ttu-id="f1862-442">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-442">Entry</span></span> | <span data-ttu-id="f1862-443">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="f1862-444">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-444">Description</span></span>    | <span data-ttu-id="f1862-445">Indique si le composant est installé dans une application.</span><span class="sxs-lookup"><span data-stu-id="f1862-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="f1862-446">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-446">Access</span></span>         | <span data-ttu-id="f1862-447">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="f1862-448">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-448">Type</span></span>           | <span data-ttu-id="f1862-449">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-449">Bool</span></span>                                                            |
| <span data-ttu-id="f1862-450">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-450">Default</span></span>        | <span data-ttu-id="f1862-451">False</span><span class="sxs-lookup"><span data-stu-id="f1862-451">False</span></span>                                                           |
| <span data-ttu-id="f1862-452">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-452">Minimum system</span></span> | <span data-ttu-id="f1862-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1862-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="f1862-454">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f1862-454">IsPrivateComponent</span></span>



| <span data-ttu-id="f1862-455">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-455">Entry</span></span> | <span data-ttu-id="f1862-456">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-457">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-457">Description</span></span>    | <span data-ttu-id="f1862-458">Détermine si une application serveur est un composant privé.</span><span class="sxs-lookup"><span data-stu-id="f1862-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="f1862-459">Un composant privé dans une application serveur ne peut être activé qu’à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="f1862-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="f1862-460">Par exemple, si vous appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) sur un composant privé, il échoue à partir de out-of-process mais fonctionne en mode in-process.</span><span class="sxs-lookup"><span data-stu-id="f1862-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="f1862-461">En revanche, si vous appelez **CoCreateInstance** sur un composant public, il est exécuté en mode in-process et out-of-process.</span><span class="sxs-lookup"><span data-stu-id="f1862-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="f1862-462">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-462">Access</span></span>         | <span data-ttu-id="f1862-463">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f1862-464">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-464">Type</span></span>           | <span data-ttu-id="f1862-465">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f1862-466">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-466">Default</span></span>        | <span data-ttu-id="f1862-467">False</span><span class="sxs-lookup"><span data-stu-id="f1862-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f1862-468">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-468">Minimum system</span></span> | <span data-ttu-id="f1862-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1862-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="f1862-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="f1862-470">JustInTimeActivation</span></span>



| <span data-ttu-id="f1862-471">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-471">Entry</span></span> | <span data-ttu-id="f1862-472">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-473">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-473">Description</span></span>    | <span data-ttu-id="f1862-474">Détermine si l' [activation JIT](enabling-jit-activation-for-a-component.md) est activée pour le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="f1862-475">Cette propriété a la valeur true lorsque la [prise en charge des transactions](setting-the-transaction-attribute.md) est définie sur obligatoire, nécessite une nouvelle ou est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f1862-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="f1862-476">Lorsque JustInTimeActivation est défini sur true, la [prise en charge](setting-the-synchronization-attribute.md) de la synchronisation doit être définie sur Required (valeur par défaut) ou nécessite New.</span><span class="sxs-lookup"><span data-stu-id="f1862-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="f1862-477">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-477">Access</span></span>         | <span data-ttu-id="f1862-478">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f1862-479">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-479">Type</span></span>           | <span data-ttu-id="f1862-480">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f1862-481">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-481">Default</span></span>        | <span data-ttu-id="f1862-482">False</span><span class="sxs-lookup"><span data-stu-id="f1862-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f1862-483">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-483">Minimum system</span></span> | <span data-ttu-id="f1862-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="f1862-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="f1862-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="f1862-486">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-486">Entry</span></span> | <span data-ttu-id="f1862-487">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-488">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-488">Description</span></span>    | <span data-ttu-id="f1862-489">Si le service d’équilibrage de charge des composants est installé et activé sur le serveur, détermine si le composant participe à l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="f1862-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="f1862-490">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-490">Access</span></span>         | <span data-ttu-id="f1862-491">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="f1862-492">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-492">Type</span></span>           | <span data-ttu-id="f1862-493">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="f1862-494">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-494">Default</span></span>        | <span data-ttu-id="f1862-495">False</span><span class="sxs-lookup"><span data-stu-id="f1862-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="f1862-496">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-496">Minimum system</span></span> | <span data-ttu-id="f1862-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="f1862-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="f1862-498">MaxPoolSize</span></span>



| <span data-ttu-id="f1862-499">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-499">Entry</span></span> | <span data-ttu-id="f1862-500">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="f1862-501">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-501">Description</span></span>    | <span data-ttu-id="f1862-502">Nombre maximal d’objets regroupés.</span><span class="sxs-lookup"><span data-stu-id="f1862-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="f1862-503">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-503">Access</span></span>         | <span data-ttu-id="f1862-504">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-504">ReadWrite</span></span>                         |
| <span data-ttu-id="f1862-505">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-505">Type</span></span>           | <span data-ttu-id="f1862-506">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="f1862-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="f1862-507">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-507">Default</span></span>        | <span data-ttu-id="f1862-508">1 048 576</span><span class="sxs-lookup"><span data-stu-id="f1862-508">1048576</span></span>                           |
| <span data-ttu-id="f1862-509">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-509">Minimum system</span></span> | <span data-ttu-id="f1862-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="f1862-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="f1862-511">MinPoolSize</span></span>



| <span data-ttu-id="f1862-512">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-512">Entry</span></span> | <span data-ttu-id="f1862-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="f1862-514">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-514">Description</span></span>    | <span data-ttu-id="f1862-515">Nombre minimal d’objets regroupés.</span><span class="sxs-lookup"><span data-stu-id="f1862-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="f1862-516">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-516">Access</span></span>         | <span data-ttu-id="f1862-517">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-517">ReadWrite</span></span>                         |
| <span data-ttu-id="f1862-518">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-518">Type</span></span>           | <span data-ttu-id="f1862-519">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="f1862-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="f1862-520">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-520">Default</span></span>        | <span data-ttu-id="f1862-521">0</span><span class="sxs-lookup"><span data-stu-id="f1862-521">0</span></span>                                 |
| <span data-ttu-id="f1862-522">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-522">Minimum system</span></span> | <span data-ttu-id="f1862-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="f1862-524">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="f1862-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="f1862-525">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-525">Entry</span></span> | <span data-ttu-id="f1862-526">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f1862-527">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-527">Description</span></span>    | <span data-ttu-id="f1862-528">CLSID du filtre de l’éditeur utilisé si le composant est une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1862-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="f1862-529">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-529">Access</span></span>         | <span data-ttu-id="f1862-530">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="f1862-531">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-531">Type</span></span>           | <span data-ttu-id="f1862-532">String</span><span class="sxs-lookup"><span data-stu-id="f1862-532">String</span></span>                                                                  |
| <span data-ttu-id="f1862-533">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-533">Default</span></span>        | <span data-ttu-id="f1862-534">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-534">N/A</span></span>                                                                     |
| <span data-ttu-id="f1862-535">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-535">Minimum system</span></span> | <span data-ttu-id="f1862-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="f1862-537">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="f1862-537">MustRunInClientContext</span></span>



| <span data-ttu-id="f1862-538">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-538">Entry</span></span> | <span data-ttu-id="f1862-539">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-540">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-540">Description</span></span>    | <span data-ttu-id="f1862-541">Indique que le composant doit être activé dans le contexte de son appelant d’origine.</span><span class="sxs-lookup"><span data-stu-id="f1862-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="f1862-542">Dans le cas contraire, l’activation échoue.</span><span class="sxs-lookup"><span data-stu-id="f1862-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="f1862-543">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-543">Access</span></span>         | <span data-ttu-id="f1862-544">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="f1862-545">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-545">Type</span></span>           | <span data-ttu-id="f1862-546">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="f1862-547">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-547">Default</span></span>        | <span data-ttu-id="f1862-548">False</span><span class="sxs-lookup"><span data-stu-id="f1862-548">False</span></span>                                                                                                     |
| <span data-ttu-id="f1862-549">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-549">Minimum system</span></span> | <span data-ttu-id="f1862-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1862-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="f1862-551">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f1862-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="f1862-552">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-552">Entry</span></span> | <span data-ttu-id="f1862-553">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-554">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-554">Description</span></span>    | <span data-ttu-id="f1862-555">Indique que le composant doit être activé dans le contexte de l’appelant par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1862-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="f1862-556">Dans le cas contraire, l’activation échoue.</span><span class="sxs-lookup"><span data-stu-id="f1862-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="f1862-557">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-557">Access</span></span>         | <span data-ttu-id="f1862-558">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="f1862-559">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-559">Type</span></span>           | <span data-ttu-id="f1862-560">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="f1862-561">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-561">Default</span></span>        | <span data-ttu-id="f1862-562">False</span><span class="sxs-lookup"><span data-stu-id="f1862-562">False</span></span>                                                                                                        |
| <span data-ttu-id="f1862-563">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-563">Minimum system</span></span> | <span data-ttu-id="f1862-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="f1862-565">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="f1862-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="f1862-566">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-566">Entry</span></span> | <span data-ttu-id="f1862-567">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-568">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-568">Description</span></span>    | <span data-ttu-id="f1862-569">Détermine si le [regroupement d’objets com+](com--object-pooling.md) est activé pour le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="f1862-570">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-570">Access</span></span>         | <span data-ttu-id="f1862-571">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="f1862-572">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-572">Type</span></span>           | <span data-ttu-id="f1862-573">Bool</span><span class="sxs-lookup"><span data-stu-id="f1862-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="f1862-574">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-574">Default</span></span>        | <span data-ttu-id="f1862-575">False</span><span class="sxs-lookup"><span data-stu-id="f1862-575">False</span></span>                                                                                           |
| <span data-ttu-id="f1862-576">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-576">Minimum system</span></span> | <span data-ttu-id="f1862-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="f1862-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="f1862-578">ProgID</span></span>



| <span data-ttu-id="f1862-579">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-579">Entry</span></span> | <span data-ttu-id="f1862-580">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-581">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-581">Description</span></span>    | <span data-ttu-id="f1862-582">Nom convivial utilisé pour identifier le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="f1862-583">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="f1862-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f1862-584">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-584">Access</span></span>         | <span data-ttu-id="f1862-585">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f1862-586">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-586">Type</span></span>           | <span data-ttu-id="f1862-587">String</span><span class="sxs-lookup"><span data-stu-id="f1862-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="f1862-588">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-588">Default</span></span>        | <span data-ttu-id="f1862-589">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f1862-590">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-590">Minimum system</span></span> | <span data-ttu-id="f1862-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="f1862-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="f1862-592">PublisherID</span></span>



| <span data-ttu-id="f1862-593">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-593">Entry</span></span> | <span data-ttu-id="f1862-594">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="f1862-595">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-595">Description</span></span>    | <span data-ttu-id="f1862-596">Identificateur de l’éditeur d’événements si le composant est une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1862-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="f1862-597">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-597">Access</span></span>         | <span data-ttu-id="f1862-598">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="f1862-599">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-599">Type</span></span>           | <span data-ttu-id="f1862-600">String</span><span class="sxs-lookup"><span data-stu-id="f1862-600">String</span></span>                                                                 |
| <span data-ttu-id="f1862-601">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-601">Default</span></span>        | <span data-ttu-id="f1862-602">""</span><span class="sxs-lookup"><span data-stu-id="f1862-602">""</span></span>                                                                     |
| <span data-ttu-id="f1862-603">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-603">Minimum system</span></span> | <span data-ttu-id="f1862-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="f1862-605">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="f1862-605">SoapAssemblyName</span></span>



| <span data-ttu-id="f1862-606">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-606">Entry</span></span> | <span data-ttu-id="f1862-607">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-608">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-608">Description</span></span>    | <span data-ttu-id="f1862-609">GUID identifiant l’assembly du GAC qui est exécuté lorsque le composant est appelé en tant que service SOAP.</span><span class="sxs-lookup"><span data-stu-id="f1862-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="f1862-610">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-610">Access</span></span>         | <span data-ttu-id="f1862-611">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="f1862-612">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-612">Type</span></span>           | <span data-ttu-id="f1862-613">String</span><span class="sxs-lookup"><span data-stu-id="f1862-613">String</span></span>                                                                                           |
| <span data-ttu-id="f1862-614">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-614">Default</span></span>        | <span data-ttu-id="f1862-615">NULL</span><span class="sxs-lookup"><span data-stu-id="f1862-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="f1862-616">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-616">Minimum system</span></span> | <span data-ttu-id="f1862-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1862-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="f1862-618">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="f1862-618">SoapTypeName</span></span>



| <span data-ttu-id="f1862-619">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-619">Entry</span></span> | <span data-ttu-id="f1862-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-621">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-621">Description</span></span>    | <span data-ttu-id="f1862-622">Nom du type managé pour un composant qui peut être appelé en tant que service SOAP.</span><span class="sxs-lookup"><span data-stu-id="f1862-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="f1862-623">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-623">Access</span></span>         | <span data-ttu-id="f1862-624">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="f1862-625">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-625">Type</span></span>           | <span data-ttu-id="f1862-626">String</span><span class="sxs-lookup"><span data-stu-id="f1862-626">String</span></span>                                                                       |
| <span data-ttu-id="f1862-627">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-627">Default</span></span>        | <span data-ttu-id="f1862-628">NULL</span><span class="sxs-lookup"><span data-stu-id="f1862-628">NULL</span></span>                                                                         |
| <span data-ttu-id="f1862-629">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-629">Minimum system</span></span> | <span data-ttu-id="f1862-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1862-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="f1862-631">Synchronization</span><span class="sxs-lookup"><span data-stu-id="f1862-631">Synchronization</span></span>



| <span data-ttu-id="f1862-632">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-632">Entry</span></span> | <span data-ttu-id="f1862-633">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-634">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-634">Description</span></span>    | <span data-ttu-id="f1862-635">Détermine la [synchronisation](setting-the-synchronization-attribute.md) des appels pour le composant.</span><span class="sxs-lookup"><span data-stu-id="f1862-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="f1862-636">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-636">Access</span></span>         | <span data-ttu-id="f1862-637">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="f1862-638">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-638">Type</span></span>           | <span data-ttu-id="f1862-639">Valeurs possibles longues : COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="f1862-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="f1862-640">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-640">Default</span></span>        | <span data-ttu-id="f1862-641">COMAdminSynchronizationIgnored (0)</span><span class="sxs-lookup"><span data-stu-id="f1862-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="f1862-642">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-642">Minimum system</span></span> | <span data-ttu-id="f1862-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="f1862-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f1862-644">ThreadingModel</span></span>



| <span data-ttu-id="f1862-645">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-645">Entry</span></span> | <span data-ttu-id="f1862-646">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-647">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-647">Description</span></span>    | <span data-ttu-id="f1862-648">Détermine le mode d’affectation des instances du composant aux threads pour l’exécution de la méthode.</span><span class="sxs-lookup"><span data-stu-id="f1862-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="f1862-649">Les valeurs correspondent aux modèles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="f1862-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="f1862-650">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-650">Access</span></span>         | <span data-ttu-id="f1862-651">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="f1862-652">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-652">Type</span></span>           | <span data-ttu-id="f1862-653">Valeurs possibles longues : COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)</span><span class="sxs-lookup"><span data-stu-id="f1862-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="f1862-654">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-654">Default</span></span>        | <span data-ttu-id="f1862-655">N/A</span><span class="sxs-lookup"><span data-stu-id="f1862-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="f1862-656">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-656">Minimum system</span></span> | <span data-ttu-id="f1862-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="f1862-658">Transaction</span><span class="sxs-lookup"><span data-stu-id="f1862-658">Transaction</span></span>



| <span data-ttu-id="f1862-659">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-659">Entry</span></span> | <span data-ttu-id="f1862-660">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-661">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-661">Description</span></span>    | <span data-ttu-id="f1862-662">Détermine la façon dont un composant prend en charge les [transactions](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="f1862-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="f1862-663">Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="f1862-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="f1862-664">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-664">Access</span></span>         | <span data-ttu-id="f1862-665">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f1862-666">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-666">Type</span></span>           | <span data-ttu-id="f1862-667">Valeurs possibles longues : COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="f1862-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="f1862-668">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-668">Default</span></span>        | <span data-ttu-id="f1862-669">COMAdminTransactionNone (1)</span><span class="sxs-lookup"><span data-stu-id="f1862-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="f1862-670">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-670">Minimum system</span></span> | <span data-ttu-id="f1862-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="f1862-672">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="f1862-672">TxIsolationLevel</span></span>



| <span data-ttu-id="f1862-673">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-673">Entry</span></span> | <span data-ttu-id="f1862-674">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1862-675">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-675">Description</span></span>    | <span data-ttu-id="f1862-676">Indique les niveaux d’isolation de la transaction.</span><span class="sxs-lookup"><span data-stu-id="f1862-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="f1862-677">Il existe cinq niveaux d’isolement : aucun, lecture non validée, lecture validée, lecture renouvelable et sérialisé.</span><span class="sxs-lookup"><span data-stu-id="f1862-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="f1862-678">Le niveau d’isolation par défaut est sérialisé.</span><span class="sxs-lookup"><span data-stu-id="f1862-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="f1862-679">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-679">Access</span></span>         | <span data-ttu-id="f1862-680">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f1862-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="f1862-681">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-681">Type</span></span>           | <span data-ttu-id="f1862-682">Valeurs possibles longues : COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="f1862-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="f1862-683">Default</span><span class="sxs-lookup"><span data-stu-id="f1862-683">Default</span></span>        | <span data-ttu-id="f1862-684">COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="f1862-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f1862-685">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-685">Minimum system</span></span> | <span data-ttu-id="f1862-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1862-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="f1862-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="f1862-687">VersionBuild</span></span>



| <span data-ttu-id="f1862-688">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-688">Entry</span></span> | <span data-ttu-id="f1862-689">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="f1862-690">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-690">Description</span></span>    | <span data-ttu-id="f1862-691">Identificateur de la build de la version.</span><span class="sxs-lookup"><span data-stu-id="f1862-691">Version build identifier.</span></span> |
| <span data-ttu-id="f1862-692">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-692">Access</span></span>         | <span data-ttu-id="f1862-693">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-693">ReadOnly</span></span>                  |
| <span data-ttu-id="f1862-694">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-694">Type</span></span>           | <span data-ttu-id="f1862-695">String</span><span class="sxs-lookup"><span data-stu-id="f1862-695">String</span></span>                    |
| <span data-ttu-id="f1862-696">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-696">Default</span></span>        | <span data-ttu-id="f1862-697">""</span><span class="sxs-lookup"><span data-stu-id="f1862-697">""</span></span>                        |
| <span data-ttu-id="f1862-698">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-698">Minimum system</span></span> | <span data-ttu-id="f1862-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="f1862-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="f1862-700">VersionMajor</span></span>



| <span data-ttu-id="f1862-701">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-701">Entry</span></span> | <span data-ttu-id="f1862-702">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="f1862-703">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-703">Description</span></span>    | <span data-ttu-id="f1862-704">Identificateur de version.</span><span class="sxs-lookup"><span data-stu-id="f1862-704">Version identifier.</span></span> |
| <span data-ttu-id="f1862-705">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-705">Access</span></span>         | <span data-ttu-id="f1862-706">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-706">ReadOnly</span></span>            |
| <span data-ttu-id="f1862-707">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-707">Type</span></span>           | <span data-ttu-id="f1862-708">String</span><span class="sxs-lookup"><span data-stu-id="f1862-708">String</span></span>              |
| <span data-ttu-id="f1862-709">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-709">Default</span></span>        | <span data-ttu-id="f1862-710">""</span><span class="sxs-lookup"><span data-stu-id="f1862-710">""</span></span>                  |
| <span data-ttu-id="f1862-711">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-711">Minimum system</span></span> | <span data-ttu-id="f1862-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="f1862-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="f1862-713">VersionMinor</span></span>



| <span data-ttu-id="f1862-714">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-714">Entry</span></span> | <span data-ttu-id="f1862-715">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="f1862-716">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-716">Description</span></span>    | <span data-ttu-id="f1862-717">Sous-identificateur de version.</span><span class="sxs-lookup"><span data-stu-id="f1862-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="f1862-718">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-718">Access</span></span>         | <span data-ttu-id="f1862-719">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-719">ReadOnly</span></span>                |
| <span data-ttu-id="f1862-720">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-720">Type</span></span>           | <span data-ttu-id="f1862-721">String</span><span class="sxs-lookup"><span data-stu-id="f1862-721">String</span></span>                  |
| <span data-ttu-id="f1862-722">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-722">Default</span></span>        | <span data-ttu-id="f1862-723">""</span><span class="sxs-lookup"><span data-stu-id="f1862-723">""</span></span>                      |
| <span data-ttu-id="f1862-724">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-724">Minimum system</span></span> | <span data-ttu-id="f1862-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="f1862-726">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="f1862-726">VersionSubBuild</span></span>



| <span data-ttu-id="f1862-727">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1862-727">Entry</span></span> | <span data-ttu-id="f1862-728">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1862-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="f1862-729">Description</span><span class="sxs-lookup"><span data-stu-id="f1862-729">Description</span></span>    | <span data-ttu-id="f1862-730">Identificateur de sous-Build de version.</span><span class="sxs-lookup"><span data-stu-id="f1862-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="f1862-731">Accès</span><span class="sxs-lookup"><span data-stu-id="f1862-731">Access</span></span>         | <span data-ttu-id="f1862-732">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1862-732">ReadOnly</span></span>                      |
| <span data-ttu-id="f1862-733">Type</span><span class="sxs-lookup"><span data-stu-id="f1862-733">Type</span></span>           | <span data-ttu-id="f1862-734">String</span><span class="sxs-lookup"><span data-stu-id="f1862-734">String</span></span>                        |
| <span data-ttu-id="f1862-735">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f1862-735">Default</span></span>        | <span data-ttu-id="f1862-736">""</span><span class="sxs-lookup"><span data-stu-id="f1862-736">""</span></span>                            |
| <span data-ttu-id="f1862-737">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f1862-737">Minimum system</span></span> | <span data-ttu-id="f1862-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f1862-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="f1862-739">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1862-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1862-740">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="f1862-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
