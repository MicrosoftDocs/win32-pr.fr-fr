---
description: Joint un système informatique à un domaine ou à un groupe de travail.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Méthode JoinDomainOrWorkgroup de la classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861526"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="2d583-103">Méthode JoinDomainOrWorkgroup de la \_ classe Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="2d583-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="2d583-104">La méthode **JoinDomainOrWorkGroup** joint un système informatique à un domaine ou à un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="2d583-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="2d583-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2d583-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2d583-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2d583-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d583-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d583-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="2d583-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d583-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d583-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d583-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d583-110">Spécifie le domaine ou le groupe de travail à joindre.</span><span class="sxs-lookup"><span data-stu-id="2d583-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="2d583-111">Ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="2d583-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-112">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d583-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d583-113">Si le paramètre de *nom d’utilisateur* spécifie un nom de compte, le paramètre *de mot de passe* doit pointer vers le mot de passe à utiliser lors de la connexion au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="2d583-114">Dans le cas contraire, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2d583-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-115">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d583-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d583-116">Pointeur vers une chaîne de caractères constante se terminant par un caractère **null** qui spécifie le nom du compte à utiliser lors de la connexion au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="2d583-117">Vous devez spécifier un nom de domaine NetBIOS et un compte d’utilisateur, par exemple, domaine \\ utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d583-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="2d583-118">Si ce paramètre a la **valeur null**, les informations de l’appelant sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="2d583-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="2d583-119">Vous pouvez également utiliser le nom d’utilisateur principal (UPPED) sous la forme user@domain .</span><span class="sxs-lookup"><span data-stu-id="2d583-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-120">*AccountOU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d583-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d583-121">Spécifie le pointeur vers une chaîne de caractères constante se terminant par un caractère **null** qui contient le nom de format [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) de l’unité d’organisation (UO) pour le compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d583-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="2d583-122">Si vous spécifiez ce paramètre, la chaîne doit contenir un chemin d’accès complet, sinon l' *accent* doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="2d583-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="2d583-123">Exemple : «OU = testOU ; DC = domaine ; DC = domaine ; DC = com "</span><span class="sxs-lookup"><span data-stu-id="2d583-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="2d583-124">*FJoinOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d583-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d583-125">Jeu d’indicateurs binaires qui définissent les options de jointure.</span><span class="sxs-lookup"><span data-stu-id="2d583-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="2d583-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="2d583-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d583-127">Default.</span></span> <span data-ttu-id="2d583-128">Aucune option de jointure.</span><span class="sxs-lookup"><span data-stu-id="2d583-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="2d583-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETsetup \_ JOINDRE un \_ domaine** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="2d583-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-130">Joint l’ordinateur à un domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-130">Joins the computer to a domain.</span></span> <span data-ttu-id="2d583-131">Si cette valeur n’est pas spécifiée, joint l’ordinateur à un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="2d583-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="2d583-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETsetup \_ \_Création de compte** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="2d583-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-133">Crée le compte sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="2d583-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETsetup \_ \_Mise à niveau de Win9x** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="2d583-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-135">L’opération de jointure se produit dans le cadre d’une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="2d583-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="2d583-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETsetup \_ Jonction de domaine \_ \_ si \_ jointe** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="2d583-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-137">Autorise une jointure à un nouveau domaine même si l’ordinateur est déjà joint à un domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="2d583-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETsetup \_ JONCTION \_ non sécurisée** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="2d583-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-139">Effectue une jonction non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2d583-139">Performs an unsecured join.</span></span>

<span data-ttu-id="2d583-140">Cette option demande une jonction de domaine à un compte créé au préalable sans authentification avec les informations d’identification de l’utilisateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="2d583-141">Cette option peut être utilisée conjointement avec l’option de configuration de l' **\_ ordinateur par mot de \_ \_ passe** .</span><span class="sxs-lookup"><span data-stu-id="2d583-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="2d583-142">Dans ce cas, *Password* est le mot de passe du compte d’ordinateur créé au préalable.</span><span class="sxs-lookup"><span data-stu-id="2d583-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="2d583-143">Avant Windows Vista avec SP1 et Windows Server 2008, une jonction non sécurisée ne s’est pas authentifiée auprès du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="2d583-144">Toutes les communications ont été effectuées à l’aide d’une session null (non authentifiée).</span><span class="sxs-lookup"><span data-stu-id="2d583-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="2d583-145">À compter de Windows Vista avec SP1 et Windows Server 2008, le nom et le mot de passe du compte d’ordinateur sont utilisés pour l’authentification auprès du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="2d583-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETsetup \_ ORDINATEUR \_ Pwd \_ passé** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="2d583-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-147">Indique que le paramètre *de mot de passe* spécifie un mot de passe de compte d’ordinateur local plutôt qu’un mot de passe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d583-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="2d583-148">Cet indicateur n’est valide que pour les jointures non sécurisées, que vous devez indiquer en définissant également l' \_ indicateur de non-sécurisation de la jonction d’installation \_ .</span><span class="sxs-lookup"><span data-stu-id="2d583-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="2d583-149">Si vous définissez cet indicateur, une fois l’opération de jointure réussie, le mot de passe de l’ordinateur est défini sur la valeur du *mot* de passe, si cette valeur est un mot de passe d’ordinateur valide.</span><span class="sxs-lookup"><span data-stu-id="2d583-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="2d583-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETsetup \_ AJOURNEr le \_ \_ jeu de noms de principal** de service (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="2d583-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-151">Indique que le nom de principal du service (SPN) et les propriétés DnsHostName de l’objet ordinateur ne doivent pas être mis à jour pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="2d583-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="2d583-152">En règle générale, ces propriétés sont mises à jour pendant l’opération de jointure.</span><span class="sxs-lookup"><span data-stu-id="2d583-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="2d583-153">Au lieu de cela, ces propriétés doivent être mises à jour lors d’un appel ultérieur à la méthode [**Rename**](rename-method-in-class-win32-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="2d583-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="2d583-154">Ces propriétés sont toujours mises à jour lors de l’opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="2d583-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="2d583-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETsetup \_ JOINDRE \_ un \_ compte DC** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="2d583-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-156">Autoriser la jonction de domaine si le compte existant est un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-157">Cet indicateur est pris en charge sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="2d583-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETsetup \_ \_Contrôleur de périphérique ambigu** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="2d583-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-159">Lorsque vous rejoignez le domaine, n’essayez pas de définir le contrôleur de domaine préféré dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2d583-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-160">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="2d583-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETsetup \_ AUCUN \_ \_ cache Netlogon** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="2d583-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-162">Lorsque vous rejoignez le domaine, ne créez pas le cache Netlogon.</span><span class="sxs-lookup"><span data-stu-id="2d583-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-163">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="2d583-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETsetup \_ Ne pas \_ contrôler les \_ services** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="2d583-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-165">Lorsque vous rejoignez le domaine, ne forcez pas le démarrage du service Netlogon.</span><span class="sxs-lookup"><span data-stu-id="2d583-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-166">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="2d583-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETsetup \_ DÉFINIR \_ le \_ nom** de l’ordinateur (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="2d583-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-168">Quand vous joignez le domaine pour une jointure hors connexion uniquement, définissez le nom d’hôte de l’ordinateur cible et le nom NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="2d583-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-169">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="2d583-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETsetup \_ FORCER \_ le \_ jeu de SPN** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="2d583-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-171">Quand vous joignez le domaine, remplacez d’autres paramètres lors de la jonction de domaine et définissez le nom de principal du service (SPN).</span><span class="sxs-lookup"><span data-stu-id="2d583-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="2d583-172">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="2d583-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETsetup \_ AUCUNE \_ \_ réutilisation de compte** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="2d583-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-174">Quand vous joignez le domaine, ne réutilisez pas un compte existant.</span><span class="sxs-lookup"><span data-stu-id="2d583-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="2d583-175">Cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d583-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="2d583-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETsetup \_ IGNORER les \_ \_ indicateurs non pris en charge** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="2d583-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="2d583-177">Si ce bit est défini, les indicateurs non reconnus sont ignorés par la fonction **JoinDomainOrWorkGroup** et [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comporte comme si les indicateurs n’étaient pas définis.</span><span class="sxs-lookup"><span data-stu-id="2d583-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d583-178">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d583-178">Return value</span></span>

<span data-ttu-id="2d583-179">Retourne un [code d’erreur système](/windows/desktop/Debug/system-error-codes), qui peut inclure l’une des valeurs numériques suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d583-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="2d583-180">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="2d583-180">Any other number indicates an error.</span></span> <span data-ttu-id="2d583-181">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2d583-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="2d583-182">**Success**</span><span class="sxs-lookup"><span data-stu-id="2d583-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-183">0</span><span class="sxs-lookup"><span data-stu-id="2d583-183">0</span></span>

</dd> <dt>

<span data-ttu-id="2d583-184">**5**</span><span class="sxs-lookup"><span data-stu-id="2d583-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-185">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="2d583-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-186">**87**</span><span class="sxs-lookup"><span data-stu-id="2d583-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-187">Le paramètre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="2d583-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-188">**110**</span><span class="sxs-lookup"><span data-stu-id="2d583-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-189">le système ne peut pas ouvrir l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d583-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="2d583-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-191">Impossible de mettre à jour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2d583-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="2d583-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-193">Échec de l’ouverture de session : nom d’utilisateur inconnu ou mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="2d583-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="2d583-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-195">Le domaine spécifié n’existe pas ou n’a pas pu être contacté.</span><span class="sxs-lookup"><span data-stu-id="2d583-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="2d583-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-197">Le compte existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2d583-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="2d583-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-199">L’ordinateur est déjà joint au domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="2d583-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-201">L’ordinateur n’est pas actuellement joint à un domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-202">**\_ \_ connexion chiffrée WBEM \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="2d583-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="2d583-203">0x80041087</span></span>

<span data-ttu-id="2d583-204">Le *mot de passe* et le *nom d’utilisateur* sont spécifiés, mais le niveau d’authentification n’est pas le niveau d’authentification RPC de la **\_ \_ \_ \_ \_ confidentialité**.</span><span class="sxs-lookup"><span data-stu-id="2d583-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="2d583-205">Pour Visual Basic, **wbemErrEncryptedConnectionRequired** est retourné.</span><span class="sxs-lookup"><span data-stu-id="2d583-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="2d583-206">**Autres**</span><span class="sxs-lookup"><span data-stu-id="2d583-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2d583-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="2d583-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d583-208">Notes</span><span class="sxs-lookup"><span data-stu-id="2d583-208">Remarks</span></span>

<span data-ttu-id="2d583-209">Lors du déplacement d’un ordinateur d’un domaine vers un groupe de travail, vous devez supprimer l’ordinateur du domaine (avec un appel à [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) avant d’appeler cette méthode pour joindre un groupe de travail (avec un appel à **JoinDomainOrWorkGroup**).</span><span class="sxs-lookup"><span data-stu-id="2d583-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="2d583-210">Après avoir appelé cette méthode, redémarrez l’ordinateur affecté pour appliquer les modifications.</span><span class="sxs-lookup"><span data-stu-id="2d583-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="2d583-211">Le *nom d’utilisateur* et le *mot de passe* peuvent être **null**.</span><span class="sxs-lookup"><span data-stu-id="2d583-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="2d583-212">Toutefois, l’authentification de la connexion à WMI doit être 6 dans script ou **WbemAuthenticationLevelPktPrivacy** dans Visual Basic et dans d’autres langues qui peuvent utiliser la bibliothèque [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) .</span><span class="sxs-lookup"><span data-stu-id="2d583-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="2d583-213">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="2d583-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="2d583-214">En C++, définissez l’authentification au **niveau de la \_ \_ \_ \_ \_ confidentialité** de l’authentification au niveau de l’authentification RPC C dans [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), pour l’ensemble du processus, ou dans [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), pour une connexion au proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="2d583-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="2d583-215">Pour plus d’informations, consultez Définition de l' [authentification à l’aide de C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) et [définition de la sécurité sur IWbemServices et d’autres proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span><span class="sxs-lookup"><span data-stu-id="2d583-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="2d583-216">Exemples</span><span class="sxs-lookup"><span data-stu-id="2d583-216">Examples</span></span>

<span data-ttu-id="2d583-217">L’exemple [rejoindre un ordinateur dans un domaine](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell joint un ordinateur à un domaine.</span><span class="sxs-lookup"><span data-stu-id="2d583-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="2d583-218">L’exemple de code VBScript suivant joint un ordinateur à un domaine et crée le compte de l’ordinateur dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d583-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="2d583-219">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d583-219">Requirements</span></span>



| <span data-ttu-id="2d583-220">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d583-220">Requirement</span></span> | <span data-ttu-id="2d583-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d583-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d583-222">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d583-222">Minimum supported client</span></span><br/> | <span data-ttu-id="2d583-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d583-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d583-224">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d583-224">Minimum supported server</span></span><br/> | <span data-ttu-id="2d583-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d583-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d583-226">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d583-226">Namespace</span></span><br/>                | <span data-ttu-id="2d583-227">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2d583-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d583-228">MOF</span><span class="sxs-lookup"><span data-stu-id="2d583-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d583-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d583-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d583-230">DLL</span><span class="sxs-lookup"><span data-stu-id="2d583-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d583-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d583-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d583-232">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d583-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d583-233">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="2d583-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="2d583-234">**Méthode UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="2d583-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

