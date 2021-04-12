---
title: attribut ms-DS-REPL-authentication-mode
description: L’attribut ms-DS-REPL-authentication-mode est utilisé pour spécifier la méthode d’authentification utilisée pour authentifier les partenaires de réplication.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-REPL-authentication-mode
- Schéma Active Directory de l’attribut msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480357"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="76de2-105">attribut ms-DS-REPL-authentication-mode</span><span class="sxs-lookup"><span data-stu-id="76de2-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="76de2-106">L’attribut **ms-DS-REPL-authentication-mode** est utilisé pour spécifier la méthode d’authentification utilisée pour authentifier les partenaires de réplication.</span><span class="sxs-lookup"><span data-stu-id="76de2-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="76de2-107">Cet attribut s’applique à la partition de configuration d’une instance ADAM.</span><span class="sxs-lookup"><span data-stu-id="76de2-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="76de2-108">Les valeurs suivantes sont les valeurs possibles pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="76de2-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="76de2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="76de2-109">Value</span></span>        | <span data-ttu-id="76de2-110">Méthode d'authentification</span><span class="sxs-lookup"><span data-stu-id="76de2-110">Authentication method</span></span>                          | <span data-ttu-id="76de2-111">Description</span><span class="sxs-lookup"><span data-stu-id="76de2-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76de2-112">0</span><span class="sxs-lookup"><span data-stu-id="76de2-112">0</span></span><br/> | <span data-ttu-id="76de2-113">Authentification directe négociée</span><span class="sxs-lookup"><span data-stu-id="76de2-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="76de2-114">Toutes les instances ADAM dans le jeu de configuration utilisent un nom de compte et un mot de passe identiques en tant que compte de service ADAM.</span><span class="sxs-lookup"><span data-stu-id="76de2-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="76de2-115">1</span><span class="sxs-lookup"><span data-stu-id="76de2-115">1</span></span><br/> | <span data-ttu-id="76de2-116">Negotiated</span><span class="sxs-lookup"><span data-stu-id="76de2-116">Negotiated</span></span><br/>                          | <span data-ttu-id="76de2-117">L'authentification Kerberos (à l'aide de noms principaux de service) est tentée en premier.</span><span class="sxs-lookup"><span data-stu-id="76de2-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="76de2-118">Si elle échoue, l'authentification NTLM est tentée.</span><span class="sxs-lookup"><span data-stu-id="76de2-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="76de2-119">Si NTLM échoue, les instances ADAM ne seront pas répliquées.</span><span class="sxs-lookup"><span data-stu-id="76de2-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="76de2-120">2</span><span class="sxs-lookup"><span data-stu-id="76de2-120">2</span></span><br/> | <span data-ttu-id="76de2-121">Authentification mutuelle avec Kerberos</span><span class="sxs-lookup"><span data-stu-id="76de2-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="76de2-122">Authentification Kerberos, utilisation de noms principaux de services (SPN), obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76de2-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="76de2-123">Si l’authentification Kerberos échoue, les instances ADAM ne seront pas répliquées.</span><span class="sxs-lookup"><span data-stu-id="76de2-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="76de2-124">Le tableau suivant contient les identificateurs programmatiques pour les valeurs de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="76de2-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="76de2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="76de2-125">Value</span></span>        | <span data-ttu-id="76de2-126">Identificateur (à partir de ntdsapi. h)</span><span class="sxs-lookup"><span data-stu-id="76de2-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="76de2-127">0</span><span class="sxs-lookup"><span data-stu-id="76de2-127">0</span></span><br/> | <span data-ttu-id="76de2-128">**\_ \_ \_ relais en mode d’authentification REPL \_ \_ \_ par négociation**</span><span class="sxs-lookup"><span data-stu-id="76de2-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="76de2-129">1</span><span class="sxs-lookup"><span data-stu-id="76de2-129">1</span></span><br/> | <span data-ttu-id="76de2-130">**\_négociation du \_ mode d’authentification REPL par Adam \_ \_**</span><span class="sxs-lookup"><span data-stu-id="76de2-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="76de2-131">2</span><span class="sxs-lookup"><span data-stu-id="76de2-131">2</span></span><br/> | <span data-ttu-id="76de2-132">**\_ \_ authentification mutuelle du mode d’authentification REPL \_ \_ \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="76de2-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="76de2-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="76de2-133">Entry</span></span> | <span data-ttu-id="76de2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="76de2-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="76de2-135">CN</span><span class="sxs-lookup"><span data-stu-id="76de2-135">CN</span></span>                | <span data-ttu-id="76de2-136">ms-DS-REPL-authentication-mode</span><span class="sxs-lookup"><span data-stu-id="76de2-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="76de2-137">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="76de2-137">Ldap-Display-Name</span></span> | <span data-ttu-id="76de2-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="76de2-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="76de2-139">Taille</span><span class="sxs-lookup"><span data-stu-id="76de2-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="76de2-140">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="76de2-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="76de2-141">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="76de2-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="76de2-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76de2-142">Attribute-Id</span></span>      | <span data-ttu-id="76de2-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="76de2-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="76de2-144">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="76de2-144">System-Id-Guid</span></span>    | <span data-ttu-id="76de2-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="76de2-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="76de2-146">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76de2-146">Syntax</span></span>            | [<span data-ttu-id="76de2-147">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="76de2-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="76de2-148">Implémentations</span><span class="sxs-lookup"><span data-stu-id="76de2-148">Implementations</span></span>

-   [<span data-ttu-id="76de2-149">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="76de2-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="76de2-150">ADAM</span><span class="sxs-lookup"><span data-stu-id="76de2-150">ADAM</span></span>



| <span data-ttu-id="76de2-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="76de2-151">Entry</span></span> | <span data-ttu-id="76de2-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="76de2-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="76de2-153">ID de lien</span><span class="sxs-lookup"><span data-stu-id="76de2-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="76de2-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76de2-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="76de2-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="76de2-155">System-Only</span></span>            | <span data-ttu-id="76de2-156">Faux</span><span class="sxs-lookup"><span data-stu-id="76de2-156">False</span></span>                                               |
| <span data-ttu-id="76de2-157">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="76de2-157">Is-Single-Valued</span></span>       | <span data-ttu-id="76de2-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="76de2-158">True</span></span>                                                |
| <span data-ttu-id="76de2-159">Est indexé</span><span class="sxs-lookup"><span data-stu-id="76de2-159">Is Indexed</span></span>             | <span data-ttu-id="76de2-160">Faux</span><span class="sxs-lookup"><span data-stu-id="76de2-160">False</span></span>                                               |
| <span data-ttu-id="76de2-161">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="76de2-161">In Global Catalog</span></span>      | <span data-ttu-id="76de2-162">Faux</span><span class="sxs-lookup"><span data-stu-id="76de2-162">False</span></span>                                               |
| <span data-ttu-id="76de2-163">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="76de2-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="76de2-164">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="76de2-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="76de2-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76de2-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="76de2-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76de2-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="76de2-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76de2-167">Search-Flags</span></span>           | <span data-ttu-id="76de2-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76de2-168">0x00000000</span></span>                                          |
| <span data-ttu-id="76de2-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76de2-169">System-Flags</span></span>           | <span data-ttu-id="76de2-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76de2-170">0x00000010</span></span>                                          |
| <span data-ttu-id="76de2-171">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="76de2-171">Classes used in</span></span>        | [<span data-ttu-id="76de2-172">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="76de2-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





