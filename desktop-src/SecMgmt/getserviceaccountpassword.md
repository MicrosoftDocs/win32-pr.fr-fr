---
description: Récupère le mot de passe du compte de service.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: GetServiceAccountPassword, fonction (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520053"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="58a28-103">GetServiceAccountPassword fonction)</span><span class="sxs-lookup"><span data-stu-id="58a28-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="58a28-104">Récupère le mot de passe du compte de service, disponible pour les [*fournisseurs de support de sécurité*](/windows/desktop/SecGloss/s-gly) (SSP), tels que Kerberos ssp.</span><span class="sxs-lookup"><span data-stu-id="58a28-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a28-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="58a28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58a28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a28-107">*AccountName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58a28-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-108">Nom de compte terminé par le caractère null du compte de service administré de groupe (gMSA).</span><span class="sxs-lookup"><span data-stu-id="58a28-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="58a28-109">Le nom d’utilisateur peut prendre l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="58a28-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="58a28-110">Nom de compte SAM du gMSA.</span><span class="sxs-lookup"><span data-stu-id="58a28-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="58a28-111">Nom d’utilisateur dans un nom de domaine complet (FQDN), tel que *nom_domaine \* **\\** _NomUtilisateur_ ou **www.** _domaine_* _. com \\_ \* _nom_.</span><span class="sxs-lookup"><span data-stu-id="58a28-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="58a28-112">Le nom d’utilisateur doit être un nom SAM uniquement.</span><span class="sxs-lookup"><span data-stu-id="58a28-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="58a28-113">Le nom de domaine peut être un nom DNS ou un nom NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="58a28-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="58a28-114">Nom d’utilisateur principal (UPN) implicite pour le compte gMSA, par exemple, *nom \* **@** _domaine_*_. com_\* où, en fonction de la définition d’un UPN implicite, le *domaine \* \* *. com** est le nom DNS de domaine réel.</span><span class="sxs-lookup"><span data-stu-id="58a28-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="58a28-115">*Nom_domaine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="58a28-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-116">Nom de domaine se terminant par un caractère null facultatif.</span><span class="sxs-lookup"><span data-stu-id="58a28-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="58a28-117">Cela n’est valide que si le paramètre *AccountName* est un nom de compte Sam.</span><span class="sxs-lookup"><span data-stu-id="58a28-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="58a28-118">Le nom de domaine ne peut être qu’un nom NetBIOS ou un nom de domaine complet (FQDN).</span><span class="sxs-lookup"><span data-stu-id="58a28-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="58a28-119">*CredFetch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58a28-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-120">Valeur de l’énumération d' [**\_ extraction de cred**](cred-fetch.md) qui spécifie comment récupérer les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="58a28-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="58a28-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a28-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="58a28-122">Signification</span><span class="sxs-lookup"><span data-stu-id="58a28-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="58a28-123"><dt>**CredFetchDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="58a28-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="58a28-124">Le système d’exploitation tente d’abord de récupérer le mot de passe à partir du cache local s’il n’est pas nécessaire d’extraire le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="58a28-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="58a28-125">S’il est temps de récupérer le mot de passe, le système d’exploitation contacte le contrôleur de domaine, sinon, retourne tous les mots de passe mis en cache dont la valeur d’État est Success.</span><span class="sxs-lookup"><span data-stu-id="58a28-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="58a28-126"><dt>**CredFetchDPAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="58a28-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="58a28-127">Retourne les informations d’identification DPAPI locales à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="58a28-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="58a28-128">Les SSP n’ont généralement pas besoin d’utiliser cette valeur.</span><span class="sxs-lookup"><span data-stu-id="58a28-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="58a28-129"><dt>**CredFetchForced**</dt></span><span class="sxs-lookup"><span data-stu-id="58a28-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="58a28-130">Force le système d’exploitation à tenter de lire le mot de passe à partir du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="58a28-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="58a28-131">Pendant l’heure de substitution du mot de passe, le mot de passe peut avoir changé au niveau du contrôleur de domaine et d’autres hôtes membres, mais l’hôte du membre gMSA reconnaît le mot de passe comme étant toujours valide.</span><span class="sxs-lookup"><span data-stu-id="58a28-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="58a28-132">Cela peut se produire en raison de problèmes d’inclinaison de l’horloge entre les différents contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="58a28-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="58a28-133">Lorsque cette valeur est spécifiée, le système d’exploitation détermine s’il peut y avoir une possibilité de modification de mot de passe en raison de l’inclinaison de l’horloge et, le cas échéant, récupère le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="58a28-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="58a28-134">Dans le cas contraire, les informations d’identification mises en cache sont retournées.</span><span class="sxs-lookup"><span data-stu-id="58a28-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="58a28-135">S’il n’y a pas d’informations d’identification mises en cache, le système d’exploitation tente d’en récupérer un à partir du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="58a28-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58a28-136">*FileTimeExpiry* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="58a28-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-137">En entrée, si cette valeur n’est pas null et n’est pas un **fileTime** zéro, *FileTimeExpiry* contient l’heure d’expiration des informations d’identification du compte de service, comme l’appelant l’appelle.</span><span class="sxs-lookup"><span data-stu-id="58a28-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="58a28-138">Si le paramètre *FileTimeExpiry* est identique à l’une des informations d’identification actuelles, cet appel échoue.</span><span class="sxs-lookup"><span data-stu-id="58a28-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="58a28-139">Lors de la sortie, le paramètre *FileTimeExpiry* contient l’heure d’expiration des informations d’identification retournées.</span><span class="sxs-lookup"><span data-stu-id="58a28-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="58a28-140">*CurrentPassword* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="58a28-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-141">Mot de passe actuel du gMSA.</span><span class="sxs-lookup"><span data-stu-id="58a28-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="58a28-142">*PreviousPassword* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="58a28-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-143">Mot de passe précédent de gMSA.</span><span class="sxs-lookup"><span data-stu-id="58a28-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="58a28-144">*FileTimeCurrPwdValidForOutbound* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="58a28-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a28-145">Indique l’heure après laquelle le mot de passe actuel est valide pour les demandes sortantes.</span><span class="sxs-lookup"><span data-stu-id="58a28-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="58a28-146">L’appelant doit comparer l’heure actuelle avec cette valeur et utiliser le mot de passe actuel retourné uniquement si l’heure actuelle est supérieure ou égale à la valeur retournée par ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="58a28-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="58a28-147">L’utilisation de ce paramètre est conçue pour les appelants qui n’ont pas de nouvelle tentative dans la logique sortante, par exemple, NTLM.</span><span class="sxs-lookup"><span data-stu-id="58a28-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a28-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58a28-148">Return value</span></span>

<span data-ttu-id="58a28-149">Si la fonction réussit, la valeur de retour est STATUs \_ successful.</span><span class="sxs-lookup"><span data-stu-id="58a28-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="58a28-150">Si la fonction échoue, la valeur de retour est un code NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="58a28-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="58a28-151">Pour plus d’informations, consultez valeurs de retour de la [fonction de stratégie LSA](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="58a28-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="58a28-152">Vous pouvez utiliser la fonction [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) pour convertir le code NTSTATUS en code d’erreur Windows.</span><span class="sxs-lookup"><span data-stu-id="58a28-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="58a28-153">Lorsque vous avez terminé d’utiliser les mémoires tampons retournées dans les paramètres *CurrentPassword* et *PreviousPassword* , libérez-les en appelant la fonction [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .</span><span class="sxs-lookup"><span data-stu-id="58a28-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="58a28-154">Notes</span><span class="sxs-lookup"><span data-stu-id="58a28-154">Remarks</span></span>

<span data-ttu-id="58a28-155">La fonction **GetServiceAccountPassword** peut être appelée dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="58a28-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="58a28-156">À partir des fonctions d’ouverture de session des fournisseurs SSP (Security Support Provider), le SSP doit détecter que le \_ mot de passe du compte de service \_ est utilisé pour se connecter à l’entité et doit vérifier que l’appelant possède un privilège TCB ou est un service réseau.</span><span class="sxs-lookup"><span data-stu-id="58a28-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="58a28-157">Ensuite, le SSP doit autoriser le processus de connexion à continuer en obtenant les informations d’identification les plus récentes en appelant la fonction **GetServiceAccountPassword** avec la valeur **CredFetchDefault** dans l’énumération [**\_ Fetch FETCH**](cred-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="58a28-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="58a28-158">Des SSP dans leurs appels [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) et [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="58a28-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="58a28-159">Les SSP doivent détecter que le \_ \_ mot de passe du compte de service est utilisé pour ces appels, et si l’appel concerne les informations d’identification non principales, le SSP doit s’assurer que l’appelant possède un privilège TCB ou est un service réseau.</span><span class="sxs-lookup"><span data-stu-id="58a28-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="58a28-160">Le SSP doit ensuite appeler la fonction **GetServiceAccountPassword** avec la valeur **CredFetchDefault** dans l’énumération d' [**\_ extraction cred**](cred-fetch.md) et procéder à l’appel.</span><span class="sxs-lookup"><span data-stu-id="58a28-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="58a28-161">Si les appels **InitializeSecurityContext** et **AcceptSecurityContext** échouent, le SSP doit utiliser le *FileTimeExpiry* récupéré à partir de l’appel précédent à **GetServiceAccountPassword** et l’utiliser comme entrée pour appeler à nouveau **GetServiceAccountPassword** à l’aide de la valeur **CredFetchForced** dans l’énumération **\_ Fetch FETCH** .</span><span class="sxs-lookup"><span data-stu-id="58a28-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="58a28-162">Si de nouvelles informations d’identification gMSA sont disponibles, le deuxième appel sera correctement effectué avec les nouvelles informations d’identification et le SSP devra ensuite réessayer avec les nouvelles informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="58a28-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a28-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58a28-163">Requirements</span></span>



| <span data-ttu-id="58a28-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58a28-164">Requirement</span></span> | <span data-ttu-id="58a28-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a28-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58a28-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a28-166">Minimum supported client</span></span><br/> | <span data-ttu-id="58a28-167">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a28-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58a28-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a28-168">Minimum supported server</span></span><br/> | <span data-ttu-id="58a28-169">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a28-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="58a28-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="58a28-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a28-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="58a28-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

