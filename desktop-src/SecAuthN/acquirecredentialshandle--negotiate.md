---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: AcquireCredentialsHandle (Negotiate), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530686"
---
# <a name="acquirecredentialshandle-negotiate-function"></a><span data-ttu-id="0e51c-103">AcquireCredentialsHandle (Negotiate) (fonction)</span><span class="sxs-lookup"><span data-stu-id="0e51c-103">AcquireCredentialsHandle (Negotiate) function</span></span>

<span data-ttu-id="0e51c-104">La fonction **AcquireCredentialsHandle (Negotiate)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0e51c-104">The **AcquireCredentialsHandle (Negotiate)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0e51c-105">Ce handle est requis par les fonctions [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) et [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-105">This handle is required by the [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) and [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) functions.</span></span> <span data-ttu-id="0e51c-106">Il peut s’agir *d’informations d’identification* préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="0e51c-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="0e51c-107">Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="0e51c-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0e51c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e51c-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="0e51c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e51c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e51c-110">*pszPrincipal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.</span><span class="sxs-lookup"><span data-stu-id="0e51c-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="0e51c-112">Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e51c-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="0e51c-113">Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="0e51c-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="0e51c-114">*pszPackage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="0e51c-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="0e51c-116">Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="0e51c-117">Une fois qu’un contexte est établi, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0e51c-117">After a context is established, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="0e51c-118">Pour appeler correctement cette fonction à l’aide du SSP Negotiate, définissez ce paramètre sur « Negotiate ».</span><span class="sxs-lookup"><span data-stu-id="0e51c-118">To successfully call this function using the Negotiate SSP, set this parameter to "Negotiate".</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-119">*fCredentialUse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-119">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-120">Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="0e51c-120">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="0e51c-121">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e51c-121">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0e51c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e51c-122">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0e51c-123">Signification</span><span class="sxs-lookup"><span data-stu-id="0e51c-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="0e51c-124"><dt>**SECPKG \_ \_ \_ Accès**</dt> automatique à cred-limité <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-124"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="0e51c-125">La sécurité n’utilise pas les informations d’identification d’ouverture de session par défaut ou les informations d’identification du [Gestionnaire d’informations d’identification](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="0e51c-125">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="0e51c-126">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e51c-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="0e51c-127"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-127"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="0e51c-128">Validez les informations d’identification entrantes ou utilisez des informations d’identification locales pour préparer un jeton sortant.</span><span class="sxs-lookup"><span data-stu-id="0e51c-128">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="0e51c-129">Cet indicateur active à la fois d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="0e51c-129">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="0e51c-130"><dt>**SECPKG \_ cred \_ entrant**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-130"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="0e51c-131">Validez les informations d’identification du serveur entrant.</span><span class="sxs-lookup"><span data-stu-id="0e51c-131">Validate an incoming server credential.</span></span> <span data-ttu-id="0e51c-132">Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) ou [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="0e51c-132">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) or [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) is called.</span></span> <span data-ttu-id="0e51c-133">Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ .</span><span class="sxs-lookup"><span data-stu-id="0e51c-133">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="0e51c-134">La validation est spécifique au package.</span><span class="sxs-lookup"><span data-stu-id="0e51c-134">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="0e51c-135"><dt>**SECPKG \_ cred \_ sortant**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-135"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="0e51c-136">Autorisez les informations d’identification du client local à préparer un jeton sortant.</span><span class="sxs-lookup"><span data-stu-id="0e51c-136">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="0e51c-137"><dt>**SECPKG \_ \_Stratégie de processus cred \_ \_ uniquement**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-137"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="0e51c-138">La fonction traite la stratégie de serveur et retourne **sec \_ E \_ sans \_ informations d’identification**, ce qui indique que l’application doit demander des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="0e51c-138">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="0e51c-139">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e51c-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="0e51c-140">*pvLogonID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-140">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-141">Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e51c-141">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="0e51c-142">Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau.</span><span class="sxs-lookup"><span data-stu-id="0e51c-142">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="0e51c-143">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0e51c-143">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-144">*pAuthData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-144">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-145">Pointeur vers des données spécifiques au package.</span><span class="sxs-lookup"><span data-stu-id="0e51c-145">A pointer to package-specific data.</span></span> <span data-ttu-id="0e51c-146">Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="0e51c-146">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="0e51c-147">Pour utiliser les informations d’identification fournies, transmettez une structure **opaque d’identité d' \_ \_ authentification \_ \_ PSEC Winnt** retournée à partir d’un appel précédent à la fonction [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-147">To use supplied credentials, pass a **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** structure returned from a previous call to the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function.</span></span>

<span data-ttu-id="0e51c-148">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Le **type \_ \_ opaque d' \_ identité \_ d’authentification PSEC Winnt** et la fonction [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e51c-148">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** The **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** type and the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function are not supported.</span></span> <span data-ttu-id="0e51c-149">Pour utiliser les informations d’identification fournies, transmettez un pointeur vers une [**\_ \_ \_ identité Winnt auth**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ou une structure d' [**\_ \_ \_ identité \_ d’authentification winnt winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) qui comprend ces informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="0e51c-149">To use supplied credentials, pass a pointer to either a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) or [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) structure that includes those credentials.</span></span>

<span data-ttu-id="0e51c-150">Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="0e51c-150">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="0e51c-151">Lorsque vous utilisez le package Negotiate, les longueurs maximales de caractères pour le nom d’utilisateur, le mot de passe et le domaine sont respectivement 256, 256 et 15.</span><span class="sxs-lookup"><span data-stu-id="0e51c-151">When using the Negotiate package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-152">*pGetKeyFn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-152">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-153">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e51c-153">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-154">*pvGetKeyArgument* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-154">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-155">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e51c-155">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-156">*phCredential* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-156">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-157">Pointeur vers une structure [CredHandle](sspi-handles.md) pour recevoir le handle d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="0e51c-157">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="0e51c-158">*ptsExpiry* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-158">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51c-159">Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent.</span><span class="sxs-lookup"><span data-stu-id="0e51c-159">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="0e51c-160">La valeur retournée dans cette structure d' **horodatage** dépend de la [*délégation avec restriction*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0e51c-160">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0e51c-161">Le [*package de sécurité*](../secgloss/s-gly.md) doit retourner cette valeur en heure locale.</span><span class="sxs-lookup"><span data-stu-id="0e51c-161">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e51c-162">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e51c-162">Return value</span></span>

<span data-ttu-id="0e51c-163">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e51c-163">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="0e51c-164">Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="0e51c-164">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="0e51c-165">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0e51c-165">Return code</span></span>                                                                                                 | <span data-ttu-id="0e51c-166">Description</span><span class="sxs-lookup"><span data-stu-id="0e51c-166">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e51c-167"><dt>**s \_ E \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-167"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="0e51c-168">La mémoire disponible est insuffisante pour terminer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="0e51c-168">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="0e51c-169"><dt>**SEC \_ E \_ \_ erreur interne**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-169"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="0e51c-170">Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0e51c-170">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="0e51c-171"><dt>**s \_ E \_ aucune \_ information d’identification**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-171"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="0e51c-172">Aucune information d’identification n’est disponible dans la [*délégation conpressionnelle*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0e51c-172">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="0e51c-173"><dt>**SEC \_ E \_ non \_ propriétaire**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-173"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="0e51c-174">L’appelant de la fonction n’a pas les informations d’identification nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0e51c-174">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="0e51c-175"><dt>**SEC \_ E \_ SECPKG \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-175"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="0e51c-176">Le [*package de sécurité*](../secgloss/s-gly.md) demandé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0e51c-176">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="0e51c-177"><dt>**SEC \_ E \_ \_ informations d’identification inconnues**</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-177"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="0e51c-178">Les informations d’identification fournies au package n’ont pas été reconnues.</span><span class="sxs-lookup"><span data-stu-id="0e51c-178">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="0e51c-179">Notes</span><span class="sxs-lookup"><span data-stu-id="0e51c-179">Remarks</span></span>

<span data-ttu-id="0e51c-180">La fonction **AcquireCredentialsHandle (Negotiate)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="0e51c-180">The **AcquireCredentialsHandle (Negotiate)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0e51c-181">Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner.</span><span class="sxs-lookup"><span data-stu-id="0e51c-181">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="0e51c-182">Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) et [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-182">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) and [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) functions.</span></span>

<span data-ttu-id="0e51c-183">En général, **AcquireCredentialsHandle (Negotiate)** ne permet pas à un processus d’obtenir un handle pour les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e51c-183">In general, **AcquireCredentialsHandle (Negotiate)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="0e51c-184">Toutefois, un appelant avec \_ \_ le [*privilège*](../secgloss/s-gly.md) se TCB nom a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session.</span><span class="sxs-lookup"><span data-stu-id="0e51c-184">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="0e51c-185">En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="0e51c-185">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="0e51c-186">Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="0e51c-186">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="0e51c-187">Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0e51c-187">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="0e51c-188">Pour les appelants en mode noyau, les différences suivantes doivent être notées :</span><span class="sxs-lookup"><span data-stu-id="0e51c-188">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="0e51c-189">Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-189">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="0e51c-190">Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.</span><span class="sxs-lookup"><span data-stu-id="0e51c-190">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="0e51c-191">Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="0e51c-191">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e51c-192">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e51c-192">Requirements</span></span>



| <span data-ttu-id="0e51c-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e51c-193">Requirement</span></span> | <span data-ttu-id="0e51c-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e51c-194">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e51c-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e51c-195">Minimum supported client</span></span><br/> | <span data-ttu-id="0e51c-196">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-196">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0e51c-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e51c-197">Minimum supported server</span></span><br/> | <span data-ttu-id="0e51c-198">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e51c-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0e51c-199">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e51c-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e51c-200"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-200"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e51c-201">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e51c-201">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e51c-202"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-202"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="0e51c-203">DLL</span><span class="sxs-lookup"><span data-stu-id="0e51c-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e51c-204"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e51c-204"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="0e51c-205">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="0e51c-205">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e51c-206">**AcquireCredentialsHandleW** (Unicode) et **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e51c-206">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0e51c-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e51c-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e51c-208">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="0e51c-208">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="0e51c-209">**AcceptSecurityContext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="0e51c-209">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="0e51c-210">**InitializeSecurityContext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="0e51c-210">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="0e51c-211">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="0e51c-211">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
