---
description: Contient un objet pour chaque composant non configuré dans la collection d’applications. Les composants non configurés ne peuvent pas utiliser les services COM+. Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Collection LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748173"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="058b7-105">Collection LegacyComponents</span><span class="sxs-lookup"><span data-stu-id="058b7-105">LegacyComponents collection</span></span>

<span data-ttu-id="058b7-106">Contient un objet pour chaque composant non configuré dans la collection d’applications.</span><span class="sxs-lookup"><span data-stu-id="058b7-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="058b7-107">Les composants non configurés ne peuvent pas utiliser les services COM+.</span><span class="sxs-lookup"><span data-stu-id="058b7-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="058b7-108">Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="058b7-109">Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="058b7-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="058b7-110">Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="058b7-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="058b7-111">Membres</span><span class="sxs-lookup"><span data-stu-id="058b7-111">Members</span></span>

<span data-ttu-id="058b7-112">La collection **LegacyComponents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="058b7-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="058b7-113">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="058b7-113">Related Collections</span></span>

<span data-ttu-id="058b7-114">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="058b7-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="058b7-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="058b7-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="058b7-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="058b7-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="058b7-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="058b7-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="058b7-118">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="058b7-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="058b7-119">**Applications**</span><span class="sxs-lookup"><span data-stu-id="058b7-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="058b7-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="058b7-120">Properties</span></span>

<span data-ttu-id="058b7-121">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="058b7-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="058b7-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="058b7-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="058b7-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="058b7-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="058b7-124">AppID</span><span class="sxs-lookup"><span data-stu-id="058b7-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="058b7-125">AppName</span><span class="sxs-lookup"><span data-stu-id="058b7-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="058b7-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="058b7-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="058b7-127">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="058b7-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="058b7-128">NomClasse</span><span class="sxs-lookup"><span data-stu-id="058b7-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="058b7-129">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="058b7-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="058b7-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="058b7-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="058b7-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="058b7-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="058b7-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="058b7-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="058b7-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="058b7-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="058b7-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="058b7-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="058b7-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="058b7-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="058b7-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="058b7-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="058b7-137">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="058b7-137">Password</span></span>](#password)
-   [<span data-ttu-id="058b7-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="058b7-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="058b7-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="058b7-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="058b7-140">RunAs</span><span class="sxs-lookup"><span data-stu-id="058b7-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="058b7-141">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="058b7-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="058b7-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="058b7-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="058b7-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="058b7-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="058b7-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="058b7-144">AccessPermissions</span></span>



| <span data-ttu-id="058b7-145">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-145">Entry</span></span> | <span data-ttu-id="058b7-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-147">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-147">Description</span></span>    | <span data-ttu-id="058b7-148">Spécifie les comptes d’utilisateurs qui sont autorisés ou non à accéder au composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="058b7-149">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-149">Access</span></span>         | <span data-ttu-id="058b7-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="058b7-151">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-151">Type</span></span>           | <span data-ttu-id="058b7-152">String</span><span class="sxs-lookup"><span data-stu-id="058b7-152">String</span></span>                                                                          |
| <span data-ttu-id="058b7-153">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-153">Default</span></span>        | <span data-ttu-id="058b7-154">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-154">N/A</span></span>                                                                             |
| <span data-ttu-id="058b7-155">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-155">Minimum system</span></span> | <span data-ttu-id="058b7-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="058b7-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="058b7-157">ActivateAtStorage</span></span>



| <span data-ttu-id="058b7-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-158">Entry</span></span> | <span data-ttu-id="058b7-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="058b7-160">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-160">Description</span></span>    | <span data-ttu-id="058b7-161">Spécifie si le serveur doit être exécuté sur l’ordinateur de stockage de données.</span><span class="sxs-lookup"><span data-stu-id="058b7-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="058b7-162">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-162">Access</span></span>         | <span data-ttu-id="058b7-163">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="058b7-164">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-164">Type</span></span>           | <span data-ttu-id="058b7-165">Valeurs possibles de chaîne : "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="058b7-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="058b7-166">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-166">Default</span></span>        | <span data-ttu-id="058b7-167">"N"</span><span class="sxs-lookup"><span data-stu-id="058b7-167">"N"</span></span>                                                              |
| <span data-ttu-id="058b7-168">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-168">Minimum system</span></span> | <span data-ttu-id="058b7-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="058b7-170">AppID</span><span class="sxs-lookup"><span data-stu-id="058b7-170">AppID</span></span>



| <span data-ttu-id="058b7-171">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-171">Entry</span></span> | <span data-ttu-id="058b7-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="058b7-173">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-173">Description</span></span>    | <span data-ttu-id="058b7-174">L’ID de l'application.</span><span class="sxs-lookup"><span data-stu-id="058b7-174">The application ID.</span></span> |
| <span data-ttu-id="058b7-175">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-175">Access</span></span>         | <span data-ttu-id="058b7-176">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-176">ReadOnly</span></span>            |
| <span data-ttu-id="058b7-177">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-177">Type</span></span>           | <span data-ttu-id="058b7-178">String</span><span class="sxs-lookup"><span data-stu-id="058b7-178">String</span></span>              |
| <span data-ttu-id="058b7-179">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-179">Default</span></span>        | <span data-ttu-id="058b7-180">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-180">N/A</span></span>                 |
| <span data-ttu-id="058b7-181">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-181">Minimum system</span></span> | <span data-ttu-id="058b7-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="058b7-183">AppName</span><span class="sxs-lookup"><span data-stu-id="058b7-183">AppName</span></span>



| <span data-ttu-id="058b7-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-184">Entry</span></span> | <span data-ttu-id="058b7-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="058b7-186">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-186">Description</span></span>    | <span data-ttu-id="058b7-187">Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="058b7-187">The name of the application.</span></span> |
| <span data-ttu-id="058b7-188">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-188">Access</span></span>         | <span data-ttu-id="058b7-189">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-189">ReadOnly</span></span>                     |
| <span data-ttu-id="058b7-190">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-190">Type</span></span>           | <span data-ttu-id="058b7-191">String</span><span class="sxs-lookup"><span data-stu-id="058b7-191">String</span></span>                       |
| <span data-ttu-id="058b7-192">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-192">Default</span></span>        | <span data-ttu-id="058b7-193">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-193">N/A</span></span>                          |
| <span data-ttu-id="058b7-194">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-194">Minimum system</span></span> | <span data-ttu-id="058b7-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="058b7-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="058b7-196">AuthenticationLevel</span></span>



| <span data-ttu-id="058b7-197">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-197">Entry</span></span> | <span data-ttu-id="058b7-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-199">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-199">Description</span></span>    | <span data-ttu-id="058b7-200">Définit le niveau d’authentification pour les appels, avec les valeurs correspondant aux paramètres d’authentification de l’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="058b7-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="058b7-201">Lorsque COMAdminAuthenticationDefault est choisi, le paramètre dans la propriété DefaultAuthenticationLevel de la collection [**LocalComputer**](localcomputer.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="058b7-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="058b7-202">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-202">Access</span></span>         | <span data-ttu-id="058b7-203">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="058b7-204">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-204">Type</span></span>           | <span data-ttu-id="058b7-205">Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="058b7-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="058b7-206">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-206">Default</span></span>        | <span data-ttu-id="058b7-207">COMAdminAuthenticationDefault (0)</span><span class="sxs-lookup"><span data-stu-id="058b7-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="058b7-208">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-208">Minimum system</span></span> | <span data-ttu-id="058b7-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="058b7-210">Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="058b7-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="058b7-211">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="058b7-211">Bitness</span></span>



| <span data-ttu-id="058b7-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-212">Entry</span></span> | <span data-ttu-id="058b7-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-214">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-214">Description</span></span>    | <span data-ttu-id="058b7-215">Représente le type de bits binaire du composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="058b7-216">Sur les systèmes qui utilisent Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits.</span><span class="sxs-lookup"><span data-stu-id="058b7-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="058b7-217">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-217">Access</span></span>         | <span data-ttu-id="058b7-218">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="058b7-219">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-219">Type</span></span>           | <span data-ttu-id="058b7-220">Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="058b7-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="058b7-221">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-221">Default</span></span>        | <span data-ttu-id="058b7-222">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="058b7-223">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-223">Minimum system</span></span> | <span data-ttu-id="058b7-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="058b7-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="058b7-225">ClassName</span></span>



| <span data-ttu-id="058b7-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-226">Entry</span></span> | <span data-ttu-id="058b7-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="058b7-228">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-228">Description</span></span>    | <span data-ttu-id="058b7-229">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="058b7-229">The name of the class.</span></span> |
| <span data-ttu-id="058b7-230">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-230">Access</span></span>         | <span data-ttu-id="058b7-231">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-231">ReadOnly</span></span>               |
| <span data-ttu-id="058b7-232">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-232">Type</span></span>           | <span data-ttu-id="058b7-233">String</span><span class="sxs-lookup"><span data-stu-id="058b7-233">String</span></span>                 |
| <span data-ttu-id="058b7-234">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-234">Default</span></span>        | <span data-ttu-id="058b7-235">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-235">N/A</span></span>                    |
| <span data-ttu-id="058b7-236">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-236">Minimum system</span></span> | <span data-ttu-id="058b7-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="058b7-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="058b7-238">CLSID</span></span>



| <span data-ttu-id="058b7-239">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-239">Entry</span></span> | <span data-ttu-id="058b7-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-241">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-241">Description</span></span>    | <span data-ttu-id="058b7-242">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-242">A GUID for the component.</span></span> <span data-ttu-id="058b7-243">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="058b7-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="058b7-244">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-244">Access</span></span>         | <span data-ttu-id="058b7-245">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="058b7-246">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-246">Type</span></span>           | <span data-ttu-id="058b7-247">String</span><span class="sxs-lookup"><span data-stu-id="058b7-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="058b7-248">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-248">Default</span></span>        | <span data-ttu-id="058b7-249">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="058b7-250">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-250">Minimum system</span></span> | <span data-ttu-id="058b7-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="058b7-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="058b7-252">DllSurrogate</span></span>



| <span data-ttu-id="058b7-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-253">Entry</span></span> | <span data-ttu-id="058b7-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="058b7-255">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-255">Description</span></span>    | <span data-ttu-id="058b7-256">Spécifie le chemin d’accès complet à une application serveur surragate.</span><span class="sxs-lookup"><span data-stu-id="058b7-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="058b7-257">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-257">Access</span></span>         | <span data-ttu-id="058b7-258">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="058b7-259">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-259">Type</span></span>           | <span data-ttu-id="058b7-260">String</span><span class="sxs-lookup"><span data-stu-id="058b7-260">String</span></span>                                                     |
| <span data-ttu-id="058b7-261">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-261">Default</span></span>        | <span data-ttu-id="058b7-262">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-262">N/A</span></span>                                                        |
| <span data-ttu-id="058b7-263">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-263">Minimum system</span></span> | <span data-ttu-id="058b7-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="058b7-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="058b7-265">InprocHandler32</span></span>



| <span data-ttu-id="058b7-266">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-266">Entry</span></span> | <span data-ttu-id="058b7-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="058b7-268">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-268">Description</span></span>    | <span data-ttu-id="058b7-269">Spécifie le chemin d’accès complet à une DLL du gestionnaire personnalisé in-process 32 bits.</span><span class="sxs-lookup"><span data-stu-id="058b7-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="058b7-270">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-270">Access</span></span>         | <span data-ttu-id="058b7-271">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="058b7-272">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-272">Type</span></span>           | <span data-ttu-id="058b7-273">String</span><span class="sxs-lookup"><span data-stu-id="058b7-273">String</span></span>                                                             |
| <span data-ttu-id="058b7-274">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-274">Default</span></span>        | <span data-ttu-id="058b7-275">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-275">N/A</span></span>                                                                |
| <span data-ttu-id="058b7-276">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-276">Minimum system</span></span> | <span data-ttu-id="058b7-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="058b7-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="058b7-278">InprocServer32</span></span>



| <span data-ttu-id="058b7-279">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-279">Entry</span></span> | <span data-ttu-id="058b7-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="058b7-281">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-281">Description</span></span>    | <span data-ttu-id="058b7-282">Spécifie le chemin d’accès complet à une DLL de serveur in-process 32 bits.</span><span class="sxs-lookup"><span data-stu-id="058b7-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="058b7-283">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-283">Access</span></span>         | <span data-ttu-id="058b7-284">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="058b7-285">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-285">Type</span></span>           | <span data-ttu-id="058b7-286">String</span><span class="sxs-lookup"><span data-stu-id="058b7-286">String</span></span>                                                     |
| <span data-ttu-id="058b7-287">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-287">Default</span></span>        | <span data-ttu-id="058b7-288">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-288">N/A</span></span>                                                        |
| <span data-ttu-id="058b7-289">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-289">Minimum system</span></span> | <span data-ttu-id="058b7-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="058b7-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="058b7-291">IsEnabled</span></span>



| <span data-ttu-id="058b7-292">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-292">Entry</span></span> | <span data-ttu-id="058b7-293">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-294">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-294">Description</span></span>    | <span data-ttu-id="058b7-295">Si l’application ou le composant COM+ est désactivé, IsEnabled a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="058b7-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="058b7-296">Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="058b7-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="058b7-297">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-297">Access</span></span>         | <span data-ttu-id="058b7-298">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="058b7-299">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-299">Type</span></span>           | <span data-ttu-id="058b7-300">Bool</span><span class="sxs-lookup"><span data-stu-id="058b7-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="058b7-301">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-301">Default</span></span>        | <span data-ttu-id="058b7-302">Vrai</span><span class="sxs-lookup"><span data-stu-id="058b7-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="058b7-303">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-303">Minimum system</span></span> | <span data-ttu-id="058b7-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="058b7-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="058b7-305">LaunchPermissions</span></span>



| <span data-ttu-id="058b7-306">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-306">Entry</span></span> | <span data-ttu-id="058b7-307">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-308">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-308">Description</span></span>    | <span data-ttu-id="058b7-309">Spécifie les comptes d’utilisateurs autorisés ou non à démarrer ce composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="058b7-310">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-310">Access</span></span>         | <span data-ttu-id="058b7-311">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="058b7-312">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-312">Type</span></span>           | <span data-ttu-id="058b7-313">String</span><span class="sxs-lookup"><span data-stu-id="058b7-313">String</span></span>                                                                                 |
| <span data-ttu-id="058b7-314">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-314">Default</span></span>        | <span data-ttu-id="058b7-315">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="058b7-316">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-316">Minimum system</span></span> | <span data-ttu-id="058b7-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="058b7-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="058b7-318">LocalServer32</span></span>



| <span data-ttu-id="058b7-319">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-319">Entry</span></span> | <span data-ttu-id="058b7-320">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-321">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-321">Description</span></span>    | <span data-ttu-id="058b7-322">Spécifie le chemin d’accès complet à une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="058b7-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="058b7-323">Pour aider à protéger la sécurité du système, utilisez des chaînes entre guillemets dans le chemin d’accès pour indiquer l’emplacement où se termine le nom de fichier exécutable et les arguments Begin.</span><span class="sxs-lookup"><span data-stu-id="058b7-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="058b7-324">Par exemple, « \\ C : \\ Program Files fichiers de la \\ société \\Application.exe\\ «param1 param2 ».</span><span class="sxs-lookup"><span data-stu-id="058b7-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="058b7-325">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-325">Access</span></span>         | <span data-ttu-id="058b7-326">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="058b7-327">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-327">Type</span></span>           | <span data-ttu-id="058b7-328">String</span><span class="sxs-lookup"><span data-stu-id="058b7-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="058b7-329">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-329">Default</span></span>        | <span data-ttu-id="058b7-330">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="058b7-331">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-331">Minimum system</span></span> | <span data-ttu-id="058b7-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="058b7-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="058b7-333">LocalService</span></span>



| <span data-ttu-id="058b7-334">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-334">Entry</span></span> | <span data-ttu-id="058b7-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="058b7-336">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-336">Description</span></span>    | <span data-ttu-id="058b7-337">Spécifie le chemin d’accès complet à l’application de service.</span><span class="sxs-lookup"><span data-stu-id="058b7-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="058b7-338">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-338">Access</span></span>         | <span data-ttu-id="058b7-339">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="058b7-340">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-340">Type</span></span>           | <span data-ttu-id="058b7-341">String</span><span class="sxs-lookup"><span data-stu-id="058b7-341">String</span></span>                                              |
| <span data-ttu-id="058b7-342">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-342">Default</span></span>        | <span data-ttu-id="058b7-343">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-343">N/A</span></span>                                                 |
| <span data-ttu-id="058b7-344">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-344">Minimum system</span></span> | <span data-ttu-id="058b7-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="058b7-346">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="058b7-346">Password</span></span>



| <span data-ttu-id="058b7-347">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-347">Entry</span></span> | <span data-ttu-id="058b7-348">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-349">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-349">Description</span></span>    | <span data-ttu-id="058b7-350">Définit le mot de passe utilisé par le processus serveur pour ouvrir une session sous l’identité RunAs spécifiée.</span><span class="sxs-lookup"><span data-stu-id="058b7-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="058b7-351">Le mot de passe doit être défini en même temps que l’identité RunAs, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="058b7-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="058b7-352">Si le mot de passe et l’identité ne sont pas synchronisés, le composant ne peut pas être lancé tant qu’il n’est pas réinitialisé par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="058b7-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="058b7-353">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-353">Access</span></span>         | <span data-ttu-id="058b7-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="058b7-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="058b7-355">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-355">Type</span></span>           | <span data-ttu-id="058b7-356">String</span><span class="sxs-lookup"><span data-stu-id="058b7-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="058b7-357">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-357">Default</span></span>        | <span data-ttu-id="058b7-358">NULL</span><span class="sxs-lookup"><span data-stu-id="058b7-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="058b7-359">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-359">Minimum system</span></span> | <span data-ttu-id="058b7-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="058b7-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="058b7-361">ProgID</span></span>



| <span data-ttu-id="058b7-362">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-362">Entry</span></span> | <span data-ttu-id="058b7-363">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-364">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-364">Description</span></span>    | <span data-ttu-id="058b7-365">Nom identifiant le composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-365">A name identifying the component.</span></span> <span data-ttu-id="058b7-366">Cette propriété est retournée lorsque la méthode de propriété Name est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="058b7-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="058b7-367">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-367">Access</span></span>         | <span data-ttu-id="058b7-368">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="058b7-369">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-369">Type</span></span>           | <span data-ttu-id="058b7-370">String</span><span class="sxs-lookup"><span data-stu-id="058b7-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="058b7-371">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-371">Default</span></span>        | <span data-ttu-id="058b7-372">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="058b7-373">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-373">Minimum system</span></span> | <span data-ttu-id="058b7-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="058b7-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="058b7-375">RemoteServer</span></span>



| <span data-ttu-id="058b7-376">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-376">Entry</span></span> | <span data-ttu-id="058b7-377">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="058b7-378">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-378">Description</span></span>    | <span data-ttu-id="058b7-379">Spécifie l’ordinateur serveur distant.</span><span class="sxs-lookup"><span data-stu-id="058b7-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="058b7-380">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-380">Access</span></span>         | <span data-ttu-id="058b7-381">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-381">ReadWrite</span></span>                             |
| <span data-ttu-id="058b7-382">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-382">Type</span></span>           | <span data-ttu-id="058b7-383">String</span><span class="sxs-lookup"><span data-stu-id="058b7-383">String</span></span>                                |
| <span data-ttu-id="058b7-384">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-384">Default</span></span>        | <span data-ttu-id="058b7-385">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-385">N/A</span></span>                                   |
| <span data-ttu-id="058b7-386">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-386">Minimum system</span></span> | <span data-ttu-id="058b7-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="058b7-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="058b7-388">RunAs</span></span>



| <span data-ttu-id="058b7-389">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-389">Entry</span></span> | <span data-ttu-id="058b7-390">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-391">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-391">Description</span></span>    | <span data-ttu-id="058b7-392">Spécifie l’utilisateur sous dont l’identité doit être exécutée par le composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="058b7-393">Le mot de passe doit être défini en même temps que l’identité RunAs, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="058b7-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="058b7-394">Si le mot de passe et l’identité ne sont pas synchronisés, le composant ne peut pas être lancé tant qu’il n’est pas réinitialisé par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="058b7-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="058b7-395">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-395">Access</span></span>         | <span data-ttu-id="058b7-396">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="058b7-397">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-397">Type</span></span>           | <span data-ttu-id="058b7-398">String</span><span class="sxs-lookup"><span data-stu-id="058b7-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="058b7-399">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-399">Default</span></span>        | <span data-ttu-id="058b7-400">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="058b7-401">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-401">Minimum system</span></span> | <span data-ttu-id="058b7-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="058b7-403">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="058b7-403">ServiceParameter</span></span>



| <span data-ttu-id="058b7-404">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-404">Entry</span></span> | <span data-ttu-id="058b7-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-406">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-406">Description</span></span>    | <span data-ttu-id="058b7-407">Spécifie les paramètres passés à l’application lorsqu’elle est appelée en tant qu’application de service.</span><span class="sxs-lookup"><span data-stu-id="058b7-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="058b7-408">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-408">Access</span></span>         | <span data-ttu-id="058b7-409">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="058b7-410">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-410">Type</span></span>           | <span data-ttu-id="058b7-411">String</span><span class="sxs-lookup"><span data-stu-id="058b7-411">String</span></span>                                                                                    |
| <span data-ttu-id="058b7-412">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="058b7-412">Default</span></span>        | <span data-ttu-id="058b7-413">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="058b7-414">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-414">Minimum system</span></span> | <span data-ttu-id="058b7-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="058b7-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="058b7-416">SRPTrustLevel</span></span>



| <span data-ttu-id="058b7-417">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-417">Entry</span></span> | <span data-ttu-id="058b7-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-419">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-419">Description</span></span>    | <span data-ttu-id="058b7-420">Indique le niveau de confiance de la stratégie de restriction logicielle (SRP) du composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="058b7-421">Le niveau de confiance du SRP fait référence au niveau de confiance que vous êtes prêt à attribuer à un composant.</span><span class="sxs-lookup"><span data-stu-id="058b7-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="058b7-422">Un niveau de confiance SRP non restreint correspond à la \_ valeur enum LEVELID FULLYTRUSTED plus sécurisée \_ , tandis qu’un niveau de confiance SRP non autorisé correspond à la \_ valeur enum non autorisée LEVELID plus sûre \_ .</span><span class="sxs-lookup"><span data-stu-id="058b7-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="058b7-423">L’énumération pour les niveaux de confiance est définie dans Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="058b7-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="058b7-424">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-424">Access</span></span>         | <span data-ttu-id="058b7-425">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="058b7-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="058b7-426">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-426">Type</span></span>           | <span data-ttu-id="058b7-427">Valeurs possibles longues : LEVELID sécurisé \_ non \_ autorisé (0x0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="058b7-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="058b7-428">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-428">Default</span></span>        | <span data-ttu-id="058b7-429">\_FULLYTRUSTED LEVELID plus \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="058b7-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="058b7-430">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-430">Minimum system</span></span> | <span data-ttu-id="058b7-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="058b7-432">La sécurité la plus stricte doit être attachée à un composant que vous êtes disposé à approuver avec un accès non restreint.</span><span class="sxs-lookup"><span data-stu-id="058b7-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="058b7-433">Les applications non restreintes ne peuvent charger que des composants non restreints, tandis que les applications non autorisées ne sont pas autorisées à s’exécuter et ne peuvent donc pas charger de composants.</span><span class="sxs-lookup"><span data-stu-id="058b7-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="058b7-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="058b7-434">ThreadingModel</span></span>



| <span data-ttu-id="058b7-435">Entrée</span><span class="sxs-lookup"><span data-stu-id="058b7-435">Entry</span></span> | <span data-ttu-id="058b7-436">Valeur</span><span class="sxs-lookup"><span data-stu-id="058b7-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058b7-437">Description</span><span class="sxs-lookup"><span data-stu-id="058b7-437">Description</span></span>    | <span data-ttu-id="058b7-438">Détermine le mode d’affectation des instances du composant aux threads pour l’exécution de la méthode.</span><span class="sxs-lookup"><span data-stu-id="058b7-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="058b7-439">Les valeurs correspondent aux modèles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="058b7-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="058b7-440">Accès</span><span class="sxs-lookup"><span data-stu-id="058b7-440">Access</span></span>         | <span data-ttu-id="058b7-441">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="058b7-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="058b7-442">Type</span><span class="sxs-lookup"><span data-stu-id="058b7-442">Type</span></span>           | <span data-ttu-id="058b7-443">Valeurs possibles longues : COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)</span><span class="sxs-lookup"><span data-stu-id="058b7-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="058b7-444">Default</span><span class="sxs-lookup"><span data-stu-id="058b7-444">Default</span></span>        | <span data-ttu-id="058b7-445">N/A</span><span class="sxs-lookup"><span data-stu-id="058b7-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="058b7-446">Système minimal</span><span class="sxs-lookup"><span data-stu-id="058b7-446">Minimum system</span></span> | <span data-ttu-id="058b7-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="058b7-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="058b7-448">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="058b7-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058b7-449">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="058b7-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
