---
description: Pour améliorer la sécurité du processus hôte du fournisseur partagé (wmiprvse.exe) Windows Management Instrumentation (WMI), des modifications ont été apportées aux plateformes Windows qui sécurisent le processus hôte du fournisseur à l’aide d’un identificateur de sécurité (SID) de service.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Clés et valeurs de Registre pour le contrôle de la sécurité du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538170"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="5fa29-103">Clés et valeurs de Registre pour le contrôle de la sécurité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="5fa29-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="5fa29-104">Pour améliorer la sécurité du processus hôte du fournisseur partagé (wmiprvse.exe) Windows Management Instrumentation (WMI), des modifications ont été apportées aux plateformes Windows qui sécurisent le processus hôte du fournisseur à l’aide d’un [*identificateur de sécurité (SID) de service*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5fa29-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="5fa29-105">Ces modifications introduisent les modes d’exécution suivants pour l’hôte partagé WMI : sécurisé et compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="5fa29-106">Les sections suivantes sont traitées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="5fa29-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="5fa29-107">Modes sécurisés et compatibles</span><span class="sxs-lookup"><span data-stu-id="5fa29-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="5fa29-108">Clés et valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="5fa29-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="5fa29-109">Configuration d’un fournisseur pour qu’il s’exécute en mode sécurisé ou compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="5fa29-110">Modes sécurisés et compatibles</span><span class="sxs-lookup"><span data-stu-id="5fa29-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="5fa29-111">À compter de Windows 7, les deux modes d’exécution suivants du processus hôte partagé WMI ont été ajoutés :</span><span class="sxs-lookup"><span data-stu-id="5fa29-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="5fa29-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Mode sécurisé</span><span class="sxs-lookup"><span data-stu-id="5fa29-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-113">Les ressources de processus hôte du fournisseur WMI sont sécurisées avec un [*SID de service*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5fa29-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="5fa29-114">Seul le *SID du service* dispose d’autorisations pour ces ressources.</span><span class="sxs-lookup"><span data-stu-id="5fa29-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="5fa29-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Mode compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-116">Le processus hôte du fournisseur partagé WMI n’est pas sécurisé avec un [*SID de service*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5fa29-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="5fa29-117">Le processus hôte du fournisseur autorise l’accès aux comptes NetworkService ou LocalService en fonction du modèle d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="5fa29-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="5fa29-118">Pour plus d’informations sur les modèles d’hébergement, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="5fa29-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="5fa29-119">**Windows Vista et Windows Server 2008 :** Pour accéder aux clés de Registre et aux valeurs de contrôle des modes sécurisé et compatible pour le processus hôte du fournisseur, vous devez installer la mise à jour de sécurité dans l' [article 959454](https://support.microsoft.com/kb/959454)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="5fa29-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="5fa29-120">Pour plus d’informations, consultez le [Bulletin de sécurité Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="5fa29-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="5fa29-121">Clés et valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="5fa29-121">Registry Keys and Values</span></span>

<span data-ttu-id="5fa29-122">Les paramètres de mode sécurisé et compatible sont spécifiés via des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="5fa29-123">Les clés de Registre pour WMI se trouvent dans le registre de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="5fa29-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="5fa29-124">Les clés de Registre et la valeur **DWORD** suivantes décrites dans la liste suivante ont été ajoutées pour contrôler le comportement des fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="5fa29-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="5fa29-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-126">Cette clé contrôle le comportement des fournisseurs individuels.</span><span class="sxs-lookup"><span data-stu-id="5fa29-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="5fa29-127">Tous les fournisseurs répertoriés dans cette clé s’exécutent toujours en mode sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="5fa29-128">Tous les fournisseurs de boîtes de réception fournis avec Windows sont répertoriés sous cette clé et sont exécutés en mode sécurisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fa29-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="5fa29-129">Cette clé est prioritaire sur les fournisseurs listés dans la clé **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="5fa29-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="5fa29-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-131">Cette clé contrôle le comportement des fournisseurs individuels.</span><span class="sxs-lookup"><span data-stu-id="5fa29-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="5fa29-132">Tous les fournisseurs répertoriés dans cette clé s’exécutent toujours en mode compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="5fa29-133">Cette clé est vide par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fa29-133">This key is empty by default.</span></span>

<span data-ttu-id="5fa29-134">Si un fournisseur est listé à la fois dans la clé **SecuredHostProviders** et dans la clé **CompatibleHostProviders** , le fournisseur est exécuté en mode sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="5fa29-135">La clé **CompatibleHostProviders** fournit une compatibilité d’application pour les applications tierces si la clé **DefaultSecuredHost** est définie sur 1 et que le fournisseur est connu pour ne pas fonctionner en mode sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="5fa29-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="5fa29-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-137">Valeur **DWORD** de Registre globale qui détermine si tous les fournisseurs, qui ne sont pas répertoriés dans les clés **SecuredHostProviders** ou **CompatibleHostProviders** , sont exécutés en mode sécurisé ou compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="5fa29-138">Cette valeur **DWORD** permet à l’administrateur de décider du mode d’exécution d’un fournisseur tiers.</span><span class="sxs-lookup"><span data-stu-id="5fa29-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="5fa29-139">Par défaut, cette valeur est définie sur zéro et tous les fournisseurs tiers sont exécutés en mode compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="5fa29-140">Les administrateurs peuvent renforcer la sécurité de leur ordinateur par défaut en définissant la valeur **DefaultSecuredHost** sur 1.</span><span class="sxs-lookup"><span data-stu-id="5fa29-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="5fa29-141">La valeur **DefaultSecuredHost** n’affecte pas les autres clés de registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="5fa29-142">Les fournisseurs répertoriés dans la clé **SecuredHostProviders** restent en mode sécurisé, tandis que ceux qui sont répertoriés dans la clé **CompatibleHostProviders** restent en mode compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="5fa29-143">Les paramètres suivants sont possibles :</span><span class="sxs-lookup"><span data-stu-id="5fa29-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="5fa29-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="5fa29-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-145">Spécifie que les fournisseurs s’exécutent en mode compatible.</span><span class="sxs-lookup"><span data-stu-id="5fa29-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="5fa29-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="5fa29-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="5fa29-147">Spécifie que les fournisseurs s’exécutent en mode sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="5fa29-148">La liste suivante répertorie les paramètres de Registre possibles et les modes d’exécution associés pour un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5fa29-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="5fa29-149">Listé sous SecuredHostProviders</span><span class="sxs-lookup"><span data-stu-id="5fa29-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="5fa29-150">Listé sous CompatibleHostProviders</span><span class="sxs-lookup"><span data-stu-id="5fa29-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="5fa29-151">Paramètre DefaultSecuredHost</span><span class="sxs-lookup"><span data-stu-id="5fa29-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="5fa29-152">Mode</span><span class="sxs-lookup"><span data-stu-id="5fa29-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="5fa29-153">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-153">No</span></span>                                | <span data-ttu-id="5fa29-154">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-154">No</span></span>                                   | <span data-ttu-id="5fa29-155">0</span><span class="sxs-lookup"><span data-stu-id="5fa29-155">0</span></span>                          | <span data-ttu-id="5fa29-156">Compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-156">Compatible</span></span> |
| <span data-ttu-id="5fa29-157">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-157">No</span></span>                                | <span data-ttu-id="5fa29-158">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-158">Yes</span></span>                                  | <span data-ttu-id="5fa29-159">0</span><span class="sxs-lookup"><span data-stu-id="5fa29-159">0</span></span>                          | <span data-ttu-id="5fa29-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-160">Compatible</span></span> |
| <span data-ttu-id="5fa29-161">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-161">Yes</span></span>                               | <span data-ttu-id="5fa29-162">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-162">No</span></span>                                   | <span data-ttu-id="5fa29-163">0</span><span class="sxs-lookup"><span data-stu-id="5fa29-163">0</span></span>                          | <span data-ttu-id="5fa29-164">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="5fa29-164">Secure</span></span>     |
| <span data-ttu-id="5fa29-165">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-165">Yes</span></span>                               | <span data-ttu-id="5fa29-166">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-166">Yes</span></span>                                  | <span data-ttu-id="5fa29-167">0</span><span class="sxs-lookup"><span data-stu-id="5fa29-167">0</span></span>                          | <span data-ttu-id="5fa29-168">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="5fa29-168">Secure</span></span>     |
| <span data-ttu-id="5fa29-169">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-169">No</span></span>                                | <span data-ttu-id="5fa29-170">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-170">No</span></span>                                   | <span data-ttu-id="5fa29-171">1</span><span class="sxs-lookup"><span data-stu-id="5fa29-171">1</span></span>                          | <span data-ttu-id="5fa29-172">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="5fa29-172">Secure</span></span>     |
| <span data-ttu-id="5fa29-173">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-173">No</span></span>                                | <span data-ttu-id="5fa29-174">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-174">Yes</span></span>                                  | <span data-ttu-id="5fa29-175">1</span><span class="sxs-lookup"><span data-stu-id="5fa29-175">1</span></span>                          | <span data-ttu-id="5fa29-176">Compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-176">Compatible</span></span> |
| <span data-ttu-id="5fa29-177">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-177">Yes</span></span>                               | <span data-ttu-id="5fa29-178">Non</span><span class="sxs-lookup"><span data-stu-id="5fa29-178">No</span></span>                                   | <span data-ttu-id="5fa29-179">1</span><span class="sxs-lookup"><span data-stu-id="5fa29-179">1</span></span>                          | <span data-ttu-id="5fa29-180">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="5fa29-180">Secure</span></span>     |
| <span data-ttu-id="5fa29-181">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-181">Yes</span></span>                               | <span data-ttu-id="5fa29-182">Oui</span><span class="sxs-lookup"><span data-stu-id="5fa29-182">Yes</span></span>                                  | <span data-ttu-id="5fa29-183">1</span><span class="sxs-lookup"><span data-stu-id="5fa29-183">1</span></span>                          | <span data-ttu-id="5fa29-184">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="5fa29-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="5fa29-185">Configuration d’un fournisseur pour qu’il s’exécute en mode sécurisé ou compatible</span><span class="sxs-lookup"><span data-stu-id="5fa29-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="5fa29-186">Les clés de Registre peuvent être modifiées à l’aide de la Console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="5fa29-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="5fa29-187">Pour plus d’informations, consultez [console de gestion des stratégies de groupe](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="5fa29-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="5fa29-188">Les procédures suivantes montrent comment gérer les paramètres de mode sécurisé et compatible à l’aide des préférences de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="5fa29-189">Pour plus d’informations sur les préférences de stratégie de groupe, consultez la [stratégie de groupe vue d’ensemble des préférences](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="5fa29-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="5fa29-190">**Pour ajouter un fournisseur au mode sécurisé ou compatible à l’aide de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="5fa29-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="5fa29-191">Ouvrez la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="5fa29-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="5fa29-192">Créez un objet stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="5fa29-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="5fa29-193">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="5fa29-194">Accédez à Préférences/Paramètres Windows/registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5fa29-195">Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**.</span><span class="sxs-lookup"><span data-stu-id="5fa29-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5fa29-196">Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5fa29-197">Sélectionnez la commande **créer** .</span><span class="sxs-lookup"><span data-stu-id="5fa29-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="5fa29-198">Sélectionnez le chemin d’accès à la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="5fa29-198">Select the following registry key path:</span></span>

    <span data-ttu-id="5fa29-199">**Mode sécurisé : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="5fa29-200">**Mode compatible : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="5fa29-201">Dans le champ **nom** , entrez le nom du fournisseur que vous souhaitez ajouter à cette clé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="5fa29-202">Le nom du fournisseur doit être au format suivant : <namespace> : <\_ \_ RelPath>.</span><span class="sxs-lookup"><span data-stu-id="5fa29-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="5fa29-203">Par exemple, \\ cimv2 racine : \_ \_ win32provider. Name = "MyProvider".</span><span class="sxs-lookup"><span data-stu-id="5fa29-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="5fa29-204">Dans le champ **données** , entrez 0.</span><span class="sxs-lookup"><span data-stu-id="5fa29-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="5fa29-205">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="5fa29-205">Click OK.</span></span>

<span data-ttu-id="5fa29-206">**Pour supprimer un fournisseur du mode sécurisé ou compatible à l’aide de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="5fa29-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="5fa29-207">Ouvrez la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="5fa29-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="5fa29-208">Créez un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-208">Create a GPO.</span></span>
3.  <span data-ttu-id="5fa29-209">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="5fa29-210">Accédez à Préférences/Paramètres Windows/registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5fa29-211">Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**.</span><span class="sxs-lookup"><span data-stu-id="5fa29-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5fa29-212">Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5fa29-213">Sélectionnez la commande **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="5fa29-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="5fa29-214">Sélectionnez le chemin d’accès à la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="5fa29-214">Select the following registry key path:</span></span>

    <span data-ttu-id="5fa29-215">**Mode sécurisé : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="5fa29-216">**Mode compatible : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5fa29-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="5fa29-217">Dans le champ **nom** , entrez le nom du fournisseur que vous souhaitez supprimer de cette clé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="5fa29-218">Dans le champ **données** , entrez 0.</span><span class="sxs-lookup"><span data-stu-id="5fa29-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="5fa29-219">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="5fa29-219">Click OK.</span></span>

<span data-ttu-id="5fa29-220">La procédure suivante fournit des détails sur la modification du comportement des fournisseurs qui ne sont pas répertoriés dans les clés **SecuredHostProviders** ou **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="5fa29-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="5fa29-221">**Pour modifier la valeur par défaut de la clé DefaultSecuredHost à l’aide de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="5fa29-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="5fa29-222">Ouvrez la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="5fa29-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="5fa29-223">Créez un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-223">Create a GPO.</span></span>
3.  <span data-ttu-id="5fa29-224">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5fa29-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="5fa29-225">Accédez à Préférences/Paramètres Windows/registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5fa29-226">Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**.</span><span class="sxs-lookup"><span data-stu-id="5fa29-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5fa29-227">Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.</span><span class="sxs-lookup"><span data-stu-id="5fa29-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5fa29-228">Sélectionnez la commande **mettre à jour** .</span><span class="sxs-lookup"><span data-stu-id="5fa29-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="5fa29-229">Sélectionnez le chemin d’accès de clé de Registre suivant : **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="5fa29-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="5fa29-230">Dans le champ **nom** , entrez **DefaultSecuredHost**.</span><span class="sxs-lookup"><span data-stu-id="5fa29-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="5fa29-231">Dans le champ de **données** , entrez 0 pour le mode compatible ou 1 pour le mode sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5fa29-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="5fa29-232">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="5fa29-232">Click OK.</span></span>

 

 
