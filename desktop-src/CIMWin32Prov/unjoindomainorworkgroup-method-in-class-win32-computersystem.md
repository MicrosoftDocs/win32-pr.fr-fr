---
description: Supprime un système informatique d’un domaine ou d’un groupe de travail.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Méthode UnjoinDomainOrWorkgroup de la classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861601"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="16e3c-103">Méthode UnjoinDomainOrWorkgroup de la \_ classe Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="16e3c-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="16e3c-104">La méthode **UnjoinDomainOrWorkgroup** supprime un système informatique d’un domaine ou d’un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="16e3c-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="16e3c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="16e3c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="16e3c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="16e3c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="16e3c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16e3c-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="16e3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16e3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e3c-109">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16e3c-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e3c-110">Si le paramètre de *nom d’utilisateur* spécifie un nom de compte, le paramètre *de mot de passe* doit pointer vers le mot de passe à utiliser lors de la connexion au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="16e3c-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="16e3c-111">Dans le cas contraire, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="16e3c-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="16e3c-112">Le *mot de passe* doit utiliser un niveau d’authentification élevé, non inférieur à la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC**, lors de la connexion à winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur le pointeur [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="16e3c-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="16e3c-113">S’il est local à winmgmt, ce n’est pas un problème.</span><span class="sxs-lookup"><span data-stu-id="16e3c-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="16e3c-114">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16e3c-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e3c-115">Pointeur vers une chaîne de caractères constante se terminant par un caractère null qui spécifie le nom du compte à utiliser lors de la connexion au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="16e3c-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="16e3c-116">Vous devez spécifier un domaine et un compte d’utilisateur, par exemple, « domaine \\ utilisateur » ou « user@domain ».</span><span class="sxs-lookup"><span data-stu-id="16e3c-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="16e3c-117">Si ce paramètre a la **valeur null**, le contexte de l’appelant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="16e3c-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="16e3c-118">Le *nom d’utilisateur* doit utiliser un niveau d’authentification élevé, non inférieur à la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC**, lors de la connexion à winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur le pointeur [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="16e3c-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="16e3c-119">S’il est local à winmgmt, ce n’est pas un problème.</span><span class="sxs-lookup"><span data-stu-id="16e3c-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="16e3c-120">*FUnjoinOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16e3c-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e3c-121">Jeu d’indicateurs binaires définissant les options de jointure.</span><span class="sxs-lookup"><span data-stu-id="16e3c-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="16e3c-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="16e3c-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="16e3c-123">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="16e3c-123">Default.</span></span> <span data-ttu-id="16e3c-124">Aucune option.</span><span class="sxs-lookup"><span data-stu-id="16e3c-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="16e3c-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETsetup \_ \_Suppression de compte** (4)</span><span class="sxs-lookup"><span data-stu-id="16e3c-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="16e3c-126">Désactivez le compte de Active Directory après l’opération d’annulation de la jointure, mais ne supprimez pas le compte.</span><span class="sxs-lookup"><span data-stu-id="16e3c-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e3c-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16e3c-127">Return value</span></span>

<span data-ttu-id="16e3c-128">La méthode **UnjoinDomainOrWorkgroup** retourne 0 (zéro) en cas de réussite ou lorsqu’aucune option n’est impliquée.</span><span class="sxs-lookup"><span data-stu-id="16e3c-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="16e3c-129">Toute autre valeur indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="16e3c-129">Any other value indicates an error.</span></span> <span data-ttu-id="16e3c-130">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="16e3c-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="16e3c-131">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="16e3c-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="16e3c-132">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="16e3c-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16e3c-133">**Autre** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="16e3c-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="16e3c-134">Notes</span><span class="sxs-lookup"><span data-stu-id="16e3c-134">Remarks</span></span>

<span data-ttu-id="16e3c-135">Après avoir appelé cette méthode, redémarrez l’ordinateur affecté pour appliquer les modifications.</span><span class="sxs-lookup"><span data-stu-id="16e3c-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="16e3c-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="16e3c-136">Examples</span></span>

<span data-ttu-id="16e3c-137">[L’ordinateur n’est pas joint à un domaine](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) L’exemple VBScript disjoint l’ordinateur local de son domaine actuel et désactive le compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="16e3c-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="16e3c-138">L’exemple de non- [jointure d’un ordinateur d’un domaine à l’aide d’un script VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) déjoint un ordinateur spécifié d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="16e3c-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="16e3c-139">.</span><span class="sxs-lookup"><span data-stu-id="16e3c-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e3c-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16e3c-140">Requirements</span></span>



| <span data-ttu-id="16e3c-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16e3c-141">Requirement</span></span> | <span data-ttu-id="16e3c-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="16e3c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16e3c-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16e3c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="16e3c-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16e3c-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16e3c-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16e3c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="16e3c-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16e3c-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16e3c-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16e3c-147">Namespace</span></span><br/>                | <span data-ttu-id="16e3c-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="16e3c-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16e3c-149">MOF</span><span class="sxs-lookup"><span data-stu-id="16e3c-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16e3c-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16e3c-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16e3c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="16e3c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e3c-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e3c-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e3c-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16e3c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e3c-154">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="16e3c-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="16e3c-155">**Méthode JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="16e3c-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

