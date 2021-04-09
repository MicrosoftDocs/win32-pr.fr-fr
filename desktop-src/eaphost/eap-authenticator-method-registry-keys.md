---
title: Valeurs de registre de la méthode d’authentificateur EAP
description: En savoir plus sur les valeurs de registre de la méthode d’authentificateur EAP. Ces valeurs de Registre spécifiques sont requises pour les méthodes d’authentificateur EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941377"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="6e9ac-104">Valeurs de registre de la méthode d’authentificateur EAP</span><span class="sxs-lookup"><span data-stu-id="6e9ac-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="6e9ac-105">Des valeurs de Registre spécifiques sont requises pour les méthodes d’authentificateur EAP.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="6e9ac-106">Chemins DLL de la méthode d’authentificateur EAP</span><span class="sxs-lookup"><span data-stu-id="6e9ac-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="6e9ac-107">Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode d’authentificateur EAP standard.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="6e9ac-108">**HKLM \\ System \\ CCS \\ services \\ \\ \\ *&lt; EAPHost méthodes de réfaut à l’EapTypeId &gt;* \\ \* &lt;&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="6e9ac-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="6e9ac-109">Par exemple, le chemin d’accès d’installation d’une méthode de l’authentificateur EAP, en fonction de la **valeur de l’identificateur d’auteur «** 311 » (indiquant que « Microsoft » est l’auteur) et d’un **EapTypeId** de « 40 », s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="6e9ac-110">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ méthodes \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="6e9ac-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="6e9ac-111">Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode d’authentificateur EAP étendue.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="6e9ac-112">**HKLM \\ System \\ CCS \\ services \\ EAPHost \\ Methods ID d' \\ *&lt; auteur &gt;* \\ 254 \\ *&lt; ID &gt;* de \\ \* &lt; la méthode&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="6e9ac-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="6e9ac-113">Par exemple, un chemin d’accès d’installation d’une méthode d’authentificateur EAP donné un **ID** d' **auteur** « 311 » (indiquant que « Microsoft » est l’auteur), un identificateur de formulaire « 311 » et un **EapTypeId** de « 40 », s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="6e9ac-114">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ méthodes \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="6e9ac-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="6e9ac-115">Pour plus d’informations sur l’allocation des types de méthode EAP, consultez la section 6,2 de la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="6e9ac-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="6e9ac-116">Valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="6e9ac-116">Registry Values</span></span>

<span data-ttu-id="6e9ac-117">Les valeurs de registre de la méthode d’authentificateur suivantes sont requises.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="6e9ac-118">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="6e9ac-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="6e9ac-119">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6e9ac-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="6e9ac-120">Outre les valeurs de Registre ci-dessus, la valeur de registre de la méthode d’authentificateur suivante est recommandée.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="6e9ac-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e9ac-121">Properties</span></span>](#properties)

<span data-ttu-id="6e9ac-122">Les valeurs de registre de la méthode d’authentificateur restante sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="6e9ac-123">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="6e9ac-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="6e9ac-124">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="6e9ac-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="6e9ac-125">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="6e9ac-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="6e9ac-126">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="6e9ac-126">Constant Value</span></span> | <span data-ttu-id="6e9ac-127">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="6e9ac-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9ac-128">Type</span><span class="sxs-lookup"><span data-stu-id="6e9ac-128">Type</span></span>           | <span data-ttu-id="6e9ac-129">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6e9ac-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="6e9ac-130">Description</span><span class="sxs-lookup"><span data-stu-id="6e9ac-130">Description</span></span>    | <span data-ttu-id="6e9ac-131">Chemin d’accès à la DLL de méthode de l’authentificateur EAP.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="6e9ac-132">Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="6e9ac-133">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6e9ac-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="6e9ac-134">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="6e9ac-134">Constant Value</span></span> | <span data-ttu-id="6e9ac-135">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6e9ac-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9ac-136">Type</span><span class="sxs-lookup"><span data-stu-id="6e9ac-136">Type</span></span>           | <span data-ttu-id="6e9ac-137">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="6e9ac-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="6e9ac-138">Description</span><span class="sxs-lookup"><span data-stu-id="6e9ac-138">Description</span></span>    | <span data-ttu-id="6e9ac-139">Chaîne qui contient le nom convivial de la méthode d’authentificateur EAP.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="6e9ac-140">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="6e9ac-140">ConfigCLSID</span></span>



| <span data-ttu-id="6e9ac-141">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="6e9ac-141">Constant Value</span></span> | <span data-ttu-id="6e9ac-142">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="6e9ac-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9ac-143">Type</span><span class="sxs-lookup"><span data-stu-id="6e9ac-143">Type</span></span>           | <span data-ttu-id="6e9ac-144">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="6e9ac-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="6e9ac-145">Description</span><span class="sxs-lookup"><span data-stu-id="6e9ac-145">Description</span></span>    | <span data-ttu-id="6e9ac-146">Chaîne qui contient le GUID de la classe de configuration pour cette méthode de l’authentificateur, au format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="6e9ac-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="6e9ac-147">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e9ac-147">Properties</span></span>



| <span data-ttu-id="6e9ac-148">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="6e9ac-148">Constant Value</span></span> | <span data-ttu-id="6e9ac-149">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e9ac-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9ac-150">Type</span><span class="sxs-lookup"><span data-stu-id="6e9ac-150">Type</span></span>           | <span data-ttu-id="6e9ac-151">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="6e9ac-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="6e9ac-152">Description</span><span class="sxs-lookup"><span data-stu-id="6e9ac-152">Description</span></span>    | <span data-ttu-id="6e9ac-153">Les bits dans la valeur DWORD sont définis pour indiquer la prise en charge de la propriété.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="6e9ac-154">Pour obtenir la liste des valeurs prises en charge, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6e9ac-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="6e9ac-155">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="6e9ac-155">StandaloneSupported</span></span>



| <span data-ttu-id="6e9ac-156">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="6e9ac-156">Constant Value</span></span> | <span data-ttu-id="6e9ac-157">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="6e9ac-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="6e9ac-158">Type</span><span class="sxs-lookup"><span data-stu-id="6e9ac-158">Type</span></span>           | <span data-ttu-id="6e9ac-159">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="6e9ac-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="6e9ac-160">Description</span><span class="sxs-lookup"><span data-stu-id="6e9ac-160">Description</span></span>    | <span data-ttu-id="6e9ac-161">0 s’il s’agit d’une méthode d’authentificateur autonome ; 1 si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="6e9ac-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e9ac-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e9ac-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e9ac-163">Clés de registre de la méthode d’homologue EAP</span><span class="sxs-lookup"><span data-stu-id="6e9ac-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="6e9ac-164">Configuration du Registre pour les types EAP étendus</span><span class="sxs-lookup"><span data-stu-id="6e9ac-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="6e9ac-165">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="6e9ac-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="6e9ac-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="6e9ac-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




