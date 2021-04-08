---
description: Contient un objet unique qui correspond à l’ordinateur dont vous accédez au catalogue. Cet objet contient des informations sur les paramètres au niveau de l’ordinateur.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Collection LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748997"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="67f79-104">Collection LocalComputer</span><span class="sxs-lookup"><span data-stu-id="67f79-104">LocalComputer collection</span></span>

<span data-ttu-id="67f79-105">Contient un objet unique qui correspond à l’ordinateur dont vous accédez au catalogue.</span><span class="sxs-lookup"><span data-stu-id="67f79-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="67f79-106">Cet objet contient des informations sur les paramètres au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67f79-106">This object holds computer level settings information.</span></span> <span data-ttu-id="67f79-107">Si vous appelez la méthode [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) sur un objet créé à partir de la classe [**COMAdminCatalog**](comadmincatalog.md) , l’objet de la collection **LocalComputer** contient des informations sur l’ordinateur distant dont vous accédez au catalogue.</span><span class="sxs-lookup"><span data-stu-id="67f79-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="67f79-108">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="67f79-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="67f79-109">Membres</span><span class="sxs-lookup"><span data-stu-id="67f79-109">Members</span></span>

<span data-ttu-id="67f79-110">La collection **LocalComputer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="67f79-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="67f79-111">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="67f79-111">Related Collections</span></span>

<span data-ttu-id="67f79-112">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="67f79-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="67f79-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="67f79-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="67f79-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="67f79-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="67f79-115">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="67f79-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="67f79-116">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="67f79-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="67f79-117">**Causes**</span><span class="sxs-lookup"><span data-stu-id="67f79-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="67f79-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67f79-118">Properties</span></span>

<span data-ttu-id="67f79-119">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="67f79-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="67f79-120">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="67f79-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="67f79-121">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="67f79-122">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="67f79-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="67f79-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="67f79-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="67f79-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="67f79-125">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="67f79-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="67f79-126">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-126">Description</span></span>](#description)
-   [<span data-ttu-id="67f79-127">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="67f79-128">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="67f79-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="67f79-129">IsRouter</span><span class="sxs-lookup"><span data-stu-id="67f79-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="67f79-130">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="67f79-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="67f79-131">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="67f79-132">Nom</span><span class="sxs-lookup"><span data-stu-id="67f79-132">Name</span></span>](#name)
-   [<span data-ttu-id="67f79-133">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67f79-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="67f79-134">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="67f79-135">Ports</span><span class="sxs-lookup"><span data-stu-id="67f79-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="67f79-136">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="67f79-137">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="67f79-138">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="67f79-139">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="67f79-140">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="67f79-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="67f79-141">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="67f79-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="67f79-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="67f79-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="67f79-143">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="67f79-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="67f79-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-144">Entry</span></span> | <span data-ttu-id="67f79-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="67f79-146">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-146">Description</span></span>    | <span data-ttu-id="67f79-147">Nom du serveur distant utilisé par les proxys d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="67f79-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="67f79-148">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-148">Access</span></span>         | <span data-ttu-id="67f79-149">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="67f79-150">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-150">Type</span></span>           | <span data-ttu-id="67f79-151">String</span><span class="sxs-lookup"><span data-stu-id="67f79-151">String</span></span>                                                     |
| <span data-ttu-id="67f79-152">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="67f79-152">Default</span></span>        | <span data-ttu-id="67f79-153">""</span><span class="sxs-lookup"><span data-stu-id="67f79-153">""</span></span>                                                         |
| <span data-ttu-id="67f79-154">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-154">Minimum system</span></span> | <span data-ttu-id="67f79-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="67f79-156">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-156">CISEnabled</span></span>



| <span data-ttu-id="67f79-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-157">Entry</span></span> | <span data-ttu-id="67f79-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="67f79-159">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-159">Description</span></span>    | <span data-ttu-id="67f79-160">Indique si les services Internet COM sont activés.</span><span class="sxs-lookup"><span data-stu-id="67f79-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="67f79-161">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-161">Access</span></span>         | <span data-ttu-id="67f79-162">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="67f79-163">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-163">Type</span></span>           | <span data-ttu-id="67f79-164">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-164">Bool</span></span>                                                |
| <span data-ttu-id="67f79-165">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-165">Default</span></span>        | <span data-ttu-id="67f79-166">False</span><span class="sxs-lookup"><span data-stu-id="67f79-166">False</span></span>                                               |
| <span data-ttu-id="67f79-167">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-167">Minimum system</span></span> | <span data-ttu-id="67f79-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="67f79-169">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-169">DCOMEnabled</span></span>



| <span data-ttu-id="67f79-170">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-170">Entry</span></span> | <span data-ttu-id="67f79-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="67f79-172">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-172">Description</span></span>    | <span data-ttu-id="67f79-173">Affectez la valeur true pour activer DCOM sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67f79-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="67f79-174">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-174">Access</span></span>         | <span data-ttu-id="67f79-175">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="67f79-176">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-176">Type</span></span>           | <span data-ttu-id="67f79-177">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-177">Bool</span></span>                                        |
| <span data-ttu-id="67f79-178">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-178">Default</span></span>        | <span data-ttu-id="67f79-179">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-179">True</span></span>                                        |
| <span data-ttu-id="67f79-180">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-180">Minimum system</span></span> | <span data-ttu-id="67f79-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="67f79-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="67f79-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="67f79-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-183">Entry</span></span> | <span data-ttu-id="67f79-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-185">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-185">Description</span></span>    | <span data-ttu-id="67f79-186">Niveau d’authentification utilisé par les applications dont l’authentification est définie sur par défaut.</span><span class="sxs-lookup"><span data-stu-id="67f79-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="67f79-187">Les valeurs correspondent aux paramètres d’authentification de l’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="67f79-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="67f79-188">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-188">Access</span></span>         | <span data-ttu-id="67f79-189">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="67f79-190">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-190">Type</span></span>           | <span data-ttu-id="67f79-191">Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="67f79-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="67f79-192">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-192">Default</span></span>        | <span data-ttu-id="67f79-193">COMAdminAuthenticationConnect (2)</span><span class="sxs-lookup"><span data-stu-id="67f79-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="67f79-194">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-194">Minimum system</span></span> | <span data-ttu-id="67f79-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="67f79-196">COMAdminAuthenticationDefault est mappé à COMAdminAuthenticationConnect quand COM appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="67f79-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="67f79-197">Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="67f79-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="67f79-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="67f79-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="67f79-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-199">Entry</span></span> | <span data-ttu-id="67f79-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-201">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-201">Description</span></span>    | <span data-ttu-id="67f79-202">Niveau d’emprunt d’identité à autoriser si aucun n’est défini.</span><span class="sxs-lookup"><span data-stu-id="67f79-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="67f79-203">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-203">Access</span></span>         | <span data-ttu-id="67f79-204">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="67f79-205">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-205">Type</span></span>           | <span data-ttu-id="67f79-206">Valeurs possibles longues : COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="67f79-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="67f79-207">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-207">Default</span></span>        | <span data-ttu-id="67f79-208">COMAdminImpersonationIdentify (2)</span><span class="sxs-lookup"><span data-stu-id="67f79-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="67f79-209">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-209">Minimum system</span></span> | <span data-ttu-id="67f79-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="67f79-211">Il est recommandé d’utiliser les constantes dans l’énumération, et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="67f79-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="67f79-212">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="67f79-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="67f79-213">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-213">Entry</span></span> | <span data-ttu-id="67f79-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-215">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-215">Description</span></span>    | <span data-ttu-id="67f79-216">Détermine si le type de port par défaut fourni doit être Internet (true) ou intranet (false).</span><span class="sxs-lookup"><span data-stu-id="67f79-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="67f79-217">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-217">Access</span></span>         | <span data-ttu-id="67f79-218">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="67f79-219">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-219">Type</span></span>           | <span data-ttu-id="67f79-220">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="67f79-221">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-221">Default</span></span>        | <span data-ttu-id="67f79-222">False</span><span class="sxs-lookup"><span data-stu-id="67f79-222">False</span></span>                                                                                               |
| <span data-ttu-id="67f79-223">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-223">Minimum system</span></span> | <span data-ttu-id="67f79-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="67f79-225">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-225">Description</span></span>



| <span data-ttu-id="67f79-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-226">Entry</span></span> | <span data-ttu-id="67f79-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="67f79-228">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-228">Description</span></span>    | <span data-ttu-id="67f79-229">Description de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67f79-229">A description of the computer.</span></span> |
| <span data-ttu-id="67f79-230">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-230">Access</span></span>         | <span data-ttu-id="67f79-231">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-231">ReadWrite</span></span>                      |
| <span data-ttu-id="67f79-232">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-232">Type</span></span>           | <span data-ttu-id="67f79-233">String</span><span class="sxs-lookup"><span data-stu-id="67f79-233">String</span></span>                         |
| <span data-ttu-id="67f79-234">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="67f79-234">Default</span></span>        | <span data-ttu-id="67f79-235">""</span><span class="sxs-lookup"><span data-stu-id="67f79-235">""</span></span>                             |
| <span data-ttu-id="67f79-236">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-236">Minimum system</span></span> | <span data-ttu-id="67f79-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="67f79-238">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="67f79-239">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-239">Entry</span></span> | <span data-ttu-id="67f79-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-241">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-241">Description</span></span>    | <span data-ttu-id="67f79-242">Indique si l’utilisateur des mappages de partition est archivé dans le magasin de domaines.</span><span class="sxs-lookup"><span data-stu-id="67f79-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="67f79-243">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-243">Access</span></span>         | <span data-ttu-id="67f79-244">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="67f79-245">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-245">Type</span></span>           | <span data-ttu-id="67f79-246">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="67f79-247">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-247">Default</span></span>        | <span data-ttu-id="67f79-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-248">True</span></span>                                                                                   |
| <span data-ttu-id="67f79-249">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-249">Minimum system</span></span> | <span data-ttu-id="67f79-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67f79-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="67f79-251">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="67f79-251">InternetPortsListed</span></span>



| <span data-ttu-id="67f79-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-252">Entry</span></span> | <span data-ttu-id="67f79-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-254">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-254">Description</span></span>    | <span data-ttu-id="67f79-255">Détermine si les ports répertoriés dans la propriété ports doivent être utilisés pour Internet (true) ou pour l’intranet (false).</span><span class="sxs-lookup"><span data-stu-id="67f79-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="67f79-256">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-256">Access</span></span>         | <span data-ttu-id="67f79-257">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="67f79-258">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-258">Type</span></span>           | <span data-ttu-id="67f79-259">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="67f79-260">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-260">Default</span></span>        | <span data-ttu-id="67f79-261">False</span><span class="sxs-lookup"><span data-stu-id="67f79-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="67f79-262">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-262">Minimum system</span></span> | <span data-ttu-id="67f79-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="67f79-264">IsRouter</span><span class="sxs-lookup"><span data-stu-id="67f79-264">IsRouter</span></span>



| <span data-ttu-id="67f79-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-265">Entry</span></span> | <span data-ttu-id="67f79-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-267">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-267">Description</span></span>    | <span data-ttu-id="67f79-268">Affectez la valeur true si l’ordinateur est un routeur pour le service d’équilibrage de charge des composants (CLB).</span><span class="sxs-lookup"><span data-stu-id="67f79-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="67f79-269">Cette propriété ne peut être définie sur true que si le service d’équilibrage de charge de composant est actuellement installé sur l’ordinateur. Sinon, les erreurs avec comadmin \_ E \_ requièrent une \_ \_ plateforme différente.</span><span class="sxs-lookup"><span data-stu-id="67f79-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="67f79-270">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-270">Access</span></span>         | <span data-ttu-id="67f79-271">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="67f79-272">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-272">Type</span></span>           | <span data-ttu-id="67f79-273">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="67f79-274">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-274">Default</span></span>        | <span data-ttu-id="67f79-275">False</span><span class="sxs-lookup"><span data-stu-id="67f79-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="67f79-276">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-276">Minimum system</span></span> | <span data-ttu-id="67f79-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="67f79-278">Si cette propriété est définie sur true, le serveur CLB est configuré et démarre au démarrage.</span><span class="sxs-lookup"><span data-stu-id="67f79-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="67f79-279">Le serveur est ajouté à la collection ApplicationCluster si elle n’est pas déjà présente.</span><span class="sxs-lookup"><span data-stu-id="67f79-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="67f79-280">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="67f79-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="67f79-281">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-281">Entry</span></span> | <span data-ttu-id="67f79-282">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="67f79-283">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-283">Description</span></span>    | <span data-ttu-id="67f79-284">CLSID de l’objet à équilibrer.</span><span class="sxs-lookup"><span data-stu-id="67f79-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="67f79-285">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-285">Access</span></span>         | <span data-ttu-id="67f79-286">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-286">ReadWrite</span></span>                           |
| <span data-ttu-id="67f79-287">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-287">Type</span></span>           | <span data-ttu-id="67f79-288">String</span><span class="sxs-lookup"><span data-stu-id="67f79-288">String</span></span>                              |
| <span data-ttu-id="67f79-289">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="67f79-289">Default</span></span>        | <span data-ttu-id="67f79-290">NULL</span><span class="sxs-lookup"><span data-stu-id="67f79-290">NULL</span></span>                                |
| <span data-ttu-id="67f79-291">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-291">Minimum system</span></span> | <span data-ttu-id="67f79-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67f79-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="67f79-293">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="67f79-294">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-294">Entry</span></span> | <span data-ttu-id="67f79-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-296">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-296">Description</span></span>    | <span data-ttu-id="67f79-297">Indique si l’utilisateur des mappages de partition est archivé dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="67f79-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="67f79-298">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-298">Access</span></span>         | <span data-ttu-id="67f79-299">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="67f79-300">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-300">Type</span></span>           | <span data-ttu-id="67f79-301">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="67f79-302">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-302">Default</span></span>        | <span data-ttu-id="67f79-303">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-303">True</span></span>                                                                                  |
| <span data-ttu-id="67f79-304">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-304">Minimum system</span></span> | <span data-ttu-id="67f79-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67f79-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="67f79-306">Nom</span><span class="sxs-lookup"><span data-stu-id="67f79-306">Name</span></span>



| <span data-ttu-id="67f79-307">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-307">Entry</span></span> | <span data-ttu-id="67f79-308">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-309">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-309">Description</span></span>    | <span data-ttu-id="67f79-310">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67f79-310">The name of the computer.</span></span> <span data-ttu-id="67f79-311">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="67f79-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="67f79-312">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-312">Access</span></span>         | <span data-ttu-id="67f79-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="67f79-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="67f79-314">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-314">Type</span></span>           | <span data-ttu-id="67f79-315">String</span><span class="sxs-lookup"><span data-stu-id="67f79-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="67f79-316">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="67f79-316">Default</span></span>        | <span data-ttu-id="67f79-317">« Poste de travail »</span><span class="sxs-lookup"><span data-stu-id="67f79-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="67f79-318">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-318">Minimum system</span></span> | <span data-ttu-id="67f79-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="67f79-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67f79-320">OperatingSystem</span></span>



| <span data-ttu-id="67f79-321">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-321">Entry</span></span> | <span data-ttu-id="67f79-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-323">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-323">Description</span></span>    | <span data-ttu-id="67f79-324">Le système d’exploitation installé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="67f79-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="67f79-325">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-325">Access</span></span>         | <span data-ttu-id="67f79-326">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="67f79-327">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-327">Type</span></span>           | <span data-ttu-id="67f79-328">Valeurs possibles longues : COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)</span><span class="sxs-lookup"><span data-stu-id="67f79-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="67f79-329">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-329">Default</span></span>        | <span data-ttu-id="67f79-330">COMAdminOSNotInitialized (0)</span><span class="sxs-lookup"><span data-stu-id="67f79-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="67f79-331">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-331">Minimum system</span></span> | <span data-ttu-id="67f79-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="67f79-333">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-333">PartitionsEnabled</span></span>



| <span data-ttu-id="67f79-334">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-334">Entry</span></span> | <span data-ttu-id="67f79-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-336">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-336">Description</span></span>    | <span data-ttu-id="67f79-337">Indique si les partitions COM+ peuvent être utilisées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="67f79-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="67f79-338">Si cette propriété a la valeur false, toute tentative d’utilisation de partitions COM+ génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="67f79-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="67f79-339">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-339">Access</span></span>         | <span data-ttu-id="67f79-340">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="67f79-341">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-341">Type</span></span>           | <span data-ttu-id="67f79-342">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="67f79-343">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-343">Default</span></span>        | <span data-ttu-id="67f79-344">False</span><span class="sxs-lookup"><span data-stu-id="67f79-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="67f79-345">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-345">Minimum system</span></span> | <span data-ttu-id="67f79-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67f79-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="67f79-347">Ports</span><span class="sxs-lookup"><span data-stu-id="67f79-347">Ports</span></span>



| <span data-ttu-id="67f79-348">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-348">Entry</span></span> | <span data-ttu-id="67f79-349">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-350">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-350">Description</span></span>    | <span data-ttu-id="67f79-351">Chaîne qui décrit les ports utilisés pour l’utilisation d’Internet ou de l’intranet, en fonction de la propriété InternetPortsListed ; par exemple, « 500-599:600-800 ».</span><span class="sxs-lookup"><span data-stu-id="67f79-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="67f79-352">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-352">Access</span></span>         | <span data-ttu-id="67f79-353">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="67f79-354">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-354">Type</span></span>           | <span data-ttu-id="67f79-355">String</span><span class="sxs-lookup"><span data-stu-id="67f79-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="67f79-356">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="67f79-356">Default</span></span>        | <span data-ttu-id="67f79-357">""</span><span class="sxs-lookup"><span data-stu-id="67f79-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="67f79-358">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-358">Minimum system</span></span> | <span data-ttu-id="67f79-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="67f79-360">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="67f79-361">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-361">Entry</span></span> | <span data-ttu-id="67f79-362">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="67f79-363">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-363">Description</span></span>    | <span data-ttu-id="67f79-364">Permet l’utilisation de redistributeurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="67f79-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="67f79-365">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-365">Access</span></span>         | <span data-ttu-id="67f79-366">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-366">ReadWrite</span></span>                           |
| <span data-ttu-id="67f79-367">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-367">Type</span></span>           | <span data-ttu-id="67f79-368">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-368">Bool</span></span>                                |
| <span data-ttu-id="67f79-369">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-369">Default</span></span>        | <span data-ttu-id="67f79-370">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-370">True</span></span>                                |
| <span data-ttu-id="67f79-371">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-371">Minimum system</span></span> | <span data-ttu-id="67f79-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="67f79-373">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="67f79-374">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-374">Entry</span></span> | <span data-ttu-id="67f79-375">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-376">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-376">Description</span></span>    | <span data-ttu-id="67f79-377">Contrôle si le proxy IIS RPC est activé.</span><span class="sxs-lookup"><span data-stu-id="67f79-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="67f79-378">Le proxy IIS RPC est utilisé conjointement avec IIS pour transférer les appels au mécanisme RPC depuis IIS et est l’un des principaux éléments des services Internet COM, qui est activé en affectant à CISEnabled la valeur true.</span><span class="sxs-lookup"><span data-stu-id="67f79-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="67f79-379">Pour plus d’informations sur RPCProxyEnabled, consultez [sécurité RPC http](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="67f79-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="67f79-380">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-380">Access</span></span>         | <span data-ttu-id="67f79-381">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="67f79-382">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-382">Type</span></span>           | <span data-ttu-id="67f79-383">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="67f79-384">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-384">Default</span></span>        | <span data-ttu-id="67f79-385">False</span><span class="sxs-lookup"><span data-stu-id="67f79-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="67f79-386">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-386">Minimum system</span></span> | <span data-ttu-id="67f79-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="67f79-388">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="67f79-389">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-389">Entry</span></span> | <span data-ttu-id="67f79-390">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-391">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-391">Description</span></span>    | <span data-ttu-id="67f79-392">S’applique aux ordinateurs DCOM qui envoient des appels interprocessus aux méthodes [**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="67f79-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="67f79-393">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-393">Access</span></span>         | <span data-ttu-id="67f79-394">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="67f79-395">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-395">Type</span></span>           | <span data-ttu-id="67f79-396">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="67f79-397">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-397">Default</span></span>        | <span data-ttu-id="67f79-398">False</span><span class="sxs-lookup"><span data-stu-id="67f79-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="67f79-399">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-399">Minimum system</span></span> | <span data-ttu-id="67f79-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="67f79-401">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="67f79-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="67f79-402">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-402">Entry</span></span> | <span data-ttu-id="67f79-403">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="67f79-404">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-404">Description</span></span>    | <span data-ttu-id="67f79-405">Affectez la valeur true si le suivi de sécurité est activé sur les objets.</span><span class="sxs-lookup"><span data-stu-id="67f79-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="67f79-406">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-406">Access</span></span>         | <span data-ttu-id="67f79-407">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="67f79-408">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-408">Type</span></span>           | <span data-ttu-id="67f79-409">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-409">Bool</span></span>                                                    |
| <span data-ttu-id="67f79-410">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-410">Default</span></span>        | <span data-ttu-id="67f79-411">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-411">True</span></span>                                                    |
| <span data-ttu-id="67f79-412">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-412">Minimum system</span></span> | <span data-ttu-id="67f79-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="67f79-414">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="67f79-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="67f79-415">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-415">Entry</span></span> | <span data-ttu-id="67f79-416">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-417">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-417">Description</span></span>    | <span data-ttu-id="67f79-418">Détermine comment la stratégie de restriction logicielle (SRP) gère les connexions d’activation en tant qu’activateur.</span><span class="sxs-lookup"><span data-stu-id="67f79-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="67f79-419">Si la valeur est true, le niveau de confiance SRP configuré pour l’objet serveur est comparé au niveau de confiance SRP de l’objet client et le niveau de confiance le plus élevé (plus rigoureux) est utilisé pour exécuter l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="67f79-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="67f79-420">Si la valeur est false, l’objet serveur s’exécute avec le niveau de confiance SRP de l’objet client, quel que soit le niveau de confiance du SRP avec lequel le serveur est configuré.</span><span class="sxs-lookup"><span data-stu-id="67f79-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="67f79-421">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-421">Access</span></span>         | <span data-ttu-id="67f79-422">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="67f79-423">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-423">Type</span></span>           | <span data-ttu-id="67f79-424">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="67f79-425">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-425">Default</span></span>        | <span data-ttu-id="67f79-426">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="67f79-427">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-427">Minimum system</span></span> | <span data-ttu-id="67f79-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67f79-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="67f79-429">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="67f79-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="67f79-430">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-430">Entry</span></span> | <span data-ttu-id="67f79-431">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-432">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-432">Description</span></span>    | <span data-ttu-id="67f79-433">Détermine comment la stratégie de restriction logicielle (SRP) gère les tentatives de connexion aux processus existants.</span><span class="sxs-lookup"><span data-stu-id="67f79-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="67f79-434">Si la valeur est false, les tentatives de connexion aux objets en cours d’exécution ne sont pas vérifiées pour les niveaux de confiance SRP appropriés.</span><span class="sxs-lookup"><span data-stu-id="67f79-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="67f79-435">Si la valeur est true, l’objet en cours d’exécution doit avoir un niveau de confiance SRP égal ou supérieur à celui de l’objet client.</span><span class="sxs-lookup"><span data-stu-id="67f79-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="67f79-436">Par exemple, un objet client avec un niveau de confiance SRP non restreint ne peut pas se connecter à un objet en cours d’exécution avec un niveau de confiance SRP interdit.</span><span class="sxs-lookup"><span data-stu-id="67f79-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="67f79-437">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-437">Access</span></span>         | <span data-ttu-id="67f79-438">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="67f79-439">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-439">Type</span></span>           | <span data-ttu-id="67f79-440">Bool</span><span class="sxs-lookup"><span data-stu-id="67f79-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="67f79-441">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-441">Default</span></span>        | <span data-ttu-id="67f79-442">Vrai</span><span class="sxs-lookup"><span data-stu-id="67f79-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="67f79-443">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-443">Minimum system</span></span> | <span data-ttu-id="67f79-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67f79-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="67f79-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="67f79-445">TransactionTimeout</span></span>



| <span data-ttu-id="67f79-446">Entrée</span><span class="sxs-lookup"><span data-stu-id="67f79-446">Entry</span></span> | <span data-ttu-id="67f79-447">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f79-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f79-448">Description</span><span class="sxs-lookup"><span data-stu-id="67f79-448">Description</span></span>    | <span data-ttu-id="67f79-449">Doit être défini sur une valeur suffisante en secondes si vous effectuez de nombreuses opérations au sein d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="67f79-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="67f79-450">Le délai d’attente par défaut est de 60 secondes et le délai d’expiration maximal est de 3600 secondes (1 heure).</span><span class="sxs-lookup"><span data-stu-id="67f79-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="67f79-451">L’affectation de la valeur 0 à cette propriété désactive les délais d’expiration de la transaction.</span><span class="sxs-lookup"><span data-stu-id="67f79-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="67f79-452">Cette propriété peut être remplacée par des composants individuels à l’aide de la propriété ComponentTransactionTimeout de la collection [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="67f79-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="67f79-453">Accès</span><span class="sxs-lookup"><span data-stu-id="67f79-453">Access</span></span>         | <span data-ttu-id="67f79-454">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67f79-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="67f79-455">Type</span><span class="sxs-lookup"><span data-stu-id="67f79-455">Type</span></span>           | <span data-ttu-id="67f79-456">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="67f79-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="67f79-457">Default</span><span class="sxs-lookup"><span data-stu-id="67f79-457">Default</span></span>        | <span data-ttu-id="67f79-458">60</span><span class="sxs-lookup"><span data-stu-id="67f79-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="67f79-459">Système minimal</span><span class="sxs-lookup"><span data-stu-id="67f79-459">Minimum system</span></span> | <span data-ttu-id="67f79-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f79-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="67f79-461">Exemple</span><span class="sxs-lookup"><span data-stu-id="67f79-461">Example</span></span>

<span data-ttu-id="67f79-462">L’exemple de Visual Basic Microsoft suivant montre comment se connecter à un ordinateur distant et obtenir sa propriété SecurityTrackingEnabled à l’aide de la collection **LocalComputer** de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="67f79-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="67f79-463">Pour utiliser cet exemple, ajoutez la bibliothèque de types d’administration COM+ en tant que référence à votre projet Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="67f79-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="67f79-464">Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="67f79-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="67f79-465">Le code Visual Basic suivant montre comment se connecter à l’ordinateur nommé « RemoteComputerName ».</span><span class="sxs-lookup"><span data-stu-id="67f79-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="67f79-466">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67f79-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f79-467">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="67f79-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
