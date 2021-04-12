---
title: Valeurs de registre de la méthode d’homologue EAP
description: En savoir plus sur les valeurs de Registre spécifiques requises pour les méthodes homologues EAP. Affichez une liste de valeurs de Registre et affichez des ressources supplémentaires disponibles.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316493"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="06525-104">Valeurs de registre de la méthode d’homologue EAP</span><span class="sxs-lookup"><span data-stu-id="06525-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="06525-105">Des valeurs de Registre spécifiques sont requises pour les méthodes homologues EAP.</span><span class="sxs-lookup"><span data-stu-id="06525-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="06525-106">Chemins DLL de la méthode d’homologue EAP</span><span class="sxs-lookup"><span data-stu-id="06525-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="06525-107">Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode homologue EAP standard.</span><span class="sxs-lookup"><span data-stu-id="06525-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="06525-108">**HKLM \\ System \\ CCS \\ services \\ \\ \\ *&lt; EAPHost méthodes de réfaut à l’EapTypeId &gt;* \\ \* &lt;&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="06525-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="06525-109">Par exemple, un chemin d' **accès d’installation** d’une méthode EAP donné un réécriture de « 311 » (indiquant que « Microsoft » est l’auteur) et un **EapTypeId** de « 40 », s’affichent comme suit.</span><span class="sxs-lookup"><span data-stu-id="06525-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="06525-110">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ méthodes \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="06525-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="06525-111">Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode EAP étendue.</span><span class="sxs-lookup"><span data-stu-id="06525-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="06525-112">Les dll de méthodes EAP étendues sont prises en charge dans Windows Vista avec Service Pack 1 (SP1) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="06525-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="06525-113">**HKLM \\ System \\ CCS \\ services \\ EAPHost \\ Methods ID d' \\ *&lt; auteur &gt;* \\ 254 \\ *&lt; ID &gt;* de service \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="06525-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="06525-114">Par exemple, un chemin d’accès d’installation d’une méthode EAP donné un ID d' **auteur** « 311 » (indiquant que « Microsoft » est l’auteur), un **ID** de formulaire « 311 » et un **EapTypeId** de « 40 », s’affichent comme suit.</span><span class="sxs-lookup"><span data-stu-id="06525-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="06525-115">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ méthodes \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="06525-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="06525-116">Pour plus d’informations sur l’allocation des types de méthode EAP, consultez la section 6,2 de la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="06525-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="06525-117">Valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="06525-117">Registry Values</span></span>

<span data-ttu-id="06525-118">Les valeurs de registre des méthodes homologues EAPHost suivantes sont requises.</span><span class="sxs-lookup"><span data-stu-id="06525-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="06525-119">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="06525-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="06525-120">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06525-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="06525-121">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="06525-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="06525-122">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="06525-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="06525-123">Les valeurs de Registre suivantes de la méthode d’homologue AP sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="06525-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="06525-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06525-124">Properties</span></span>](#properties)

<span data-ttu-id="06525-125">Les valeurs de registre de la méthode d’homologue AP suivantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="06525-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="06525-126">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="06525-127">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="06525-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="06525-128">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="06525-129">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="06525-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="06525-130">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="06525-131">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-131">Constant Value</span></span> | <span data-ttu-id="06525-132">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-133">Type</span><span class="sxs-lookup"><span data-stu-id="06525-133">Type</span></span>           | <span data-ttu-id="06525-134">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="06525-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="06525-135">Description</span><span class="sxs-lookup"><span data-stu-id="06525-135">Description</span></span>    | <span data-ttu-id="06525-136">Chemin d’accès à la DLL qui contient l’implémentation de la boîte de dialogue de configuration utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06525-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="06525-137">Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="06525-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="06525-138">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="06525-138">PeerDllPath</span></span>



| <span data-ttu-id="06525-139">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-139">Constant Value</span></span> | <span data-ttu-id="06525-140">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="06525-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-141">Type</span><span class="sxs-lookup"><span data-stu-id="06525-141">Type</span></span>           | <span data-ttu-id="06525-142">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="06525-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="06525-143">Description</span><span class="sxs-lookup"><span data-stu-id="06525-143">Description</span></span>    | <span data-ttu-id="06525-144">Chemin d’accès à la DLL de méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="06525-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="06525-145">Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="06525-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="06525-146">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06525-146">PeerFriendlyName</span></span>



| <span data-ttu-id="06525-147">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-147">Constant Value</span></span> | <span data-ttu-id="06525-148">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06525-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="06525-149">Type</span><span class="sxs-lookup"><span data-stu-id="06525-149">Type</span></span>           | <span data-ttu-id="06525-150">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="06525-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="06525-151">Description</span><span class="sxs-lookup"><span data-stu-id="06525-151">Description</span></span>    | <span data-ttu-id="06525-152">Chaîne qui contient le nom convivial de la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="06525-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="06525-153">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="06525-153">PeerIdentityPath</span></span>



| <span data-ttu-id="06525-154">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-154">Constant Value</span></span> | <span data-ttu-id="06525-155">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="06525-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-156">Type</span><span class="sxs-lookup"><span data-stu-id="06525-156">Type</span></span>           | <span data-ttu-id="06525-157">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="06525-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="06525-158">Description</span><span class="sxs-lookup"><span data-stu-id="06525-158">Description</span></span>    | <span data-ttu-id="06525-159">Chemin d’accès à la DLL qui contient l’implémentation des fonctions d’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06525-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="06525-160">Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="06525-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="06525-161">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="06525-162">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-162">Constant Value</span></span> | <span data-ttu-id="06525-163">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="06525-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-164">Type</span><span class="sxs-lookup"><span data-stu-id="06525-164">Type</span></span>           | <span data-ttu-id="06525-165">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="06525-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="06525-166">Description</span><span class="sxs-lookup"><span data-stu-id="06525-166">Description</span></span>    | <span data-ttu-id="06525-167">Chemin d’accès à la DLL qui contient l’implémentation de l’interface utilisateur interactive utilisée pour obtenir les informations utilisateur lors de l’exécution de la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="06525-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="06525-168">Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="06525-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="06525-169">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="06525-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="06525-170">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-170">Constant Value</span></span> | <span data-ttu-id="06525-171">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="06525-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-172">Type</span><span class="sxs-lookup"><span data-stu-id="06525-172">Type</span></span>           | <span data-ttu-id="06525-173">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="06525-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="06525-174">Description</span><span class="sxs-lookup"><span data-stu-id="06525-174">Description</span></span>    | <span data-ttu-id="06525-175">1-pour récupérer les informations d’identification à l’aide de la boîte de dialogue mot de passe et domaine EAPHost générique.</span><span class="sxs-lookup"><span data-stu-id="06525-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="06525-176">0-pour utiliser une boîte de dialogue personnalisée.</span><span class="sxs-lookup"><span data-stu-id="06525-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="06525-177">Si la boîte de dialogue générique est utilisée, les informations d’identification sont définies par la méthode [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="06525-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="06525-178">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="06525-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06525-179">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-179">Constant Value</span></span></th>
<th><span data-ttu-id="06525-180">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="06525-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06525-181">Type</span><span class="sxs-lookup"><span data-stu-id="06525-181">Type</span></span></td>
<td><span data-ttu-id="06525-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="06525-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06525-183">Description</span><span class="sxs-lookup"><span data-stu-id="06525-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="06525-184">1-pour récupérer les informations d’identification à l’aide de la boîte de dialogue générique EAPHost User Name.</span><span class="sxs-lookup"><span data-stu-id="06525-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="06525-185">0-pour utiliser une boîte de dialogue personnalisée.</span><span class="sxs-lookup"><span data-stu-id="06525-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="06525-186">Si la boîte de dialogue générique est utilisée, les informations d’identification sont définies par la méthode [<strong>EapPeerSetCredentials</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials).</span><span class="sxs-lookup"><span data-stu-id="06525-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="06525-187">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="06525-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="06525-188">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-188">Constant Value</span></span> | <span data-ttu-id="06525-189">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="06525-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-190">Type</span><span class="sxs-lookup"><span data-stu-id="06525-190">Type</span></span>           | <span data-ttu-id="06525-191">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="06525-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="06525-192">Description</span><span class="sxs-lookup"><span data-stu-id="06525-192">Description</span></span>    | <span data-ttu-id="06525-193">0 si une boîte de dialogue d’interface utilisateur de configuration est implémentée pour cette méthode ; 1 si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="06525-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="06525-194">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06525-194">Properties</span></span>



| <span data-ttu-id="06525-195">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="06525-195">Constant Value</span></span> | <span data-ttu-id="06525-196">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06525-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06525-197">Type</span><span class="sxs-lookup"><span data-stu-id="06525-197">Type</span></span>           | <span data-ttu-id="06525-198">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="06525-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="06525-199">Description</span><span class="sxs-lookup"><span data-stu-id="06525-199">Description</span></span>    | <span data-ttu-id="06525-200">Les bits dans la valeur DWORD sont définis pour indiquer la prise en charge de la propriété.</span><span class="sxs-lookup"><span data-stu-id="06525-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="06525-201">Pour obtenir la liste des valeurs prises en charge, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="06525-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="06525-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06525-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06525-203">Clés de registre de la méthode d’authentificateur EAP</span><span class="sxs-lookup"><span data-stu-id="06525-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="06525-204">Configuration du Registre pour les types EAP étendus</span><span class="sxs-lookup"><span data-stu-id="06525-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="06525-205">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="06525-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="06525-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="06525-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 