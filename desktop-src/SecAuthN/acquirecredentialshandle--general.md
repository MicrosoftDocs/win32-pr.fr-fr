---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: AcquireCredentialsHandle (général), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521896"
---
# <a name="acquirecredentialshandle-general-function"></a><span data-ttu-id="c97ca-103">AcquireCredentialsHandle (général) (fonction)</span><span class="sxs-lookup"><span data-stu-id="c97ca-103">AcquireCredentialsHandle (General) function</span></span>

<span data-ttu-id="c97ca-104">La fonction **AcquireCredentialsHandle (général)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c97ca-104">The **AcquireCredentialsHandle (General)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c97ca-105">Ce handle est requis par les fonctions [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) et [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="c97ca-105">This handle is required by the [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) and [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) functions.</span></span> <span data-ttu-id="c97ca-106">Il peut s’agir d’informations d’identification préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c97ca-106">These can be either preexisting credentials, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="c97ca-107">Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c97ca-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

<span data-ttu-id="c97ca-108">Pour plus d’informations sur l’utilisation de cette fonction avec un fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) spécifique, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="c97ca-108">For information about using this function with a specific [*security support provider*](../secgloss/s-gly.md) (SSP), see the following topics.</span></span>



| <span data-ttu-id="c97ca-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c97ca-109">Topic</span></span>                                                                                           | <span data-ttu-id="c97ca-110">Description</span><span class="sxs-lookup"><span data-stu-id="c97ca-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c97ca-111">**AcquireCredentialsHandle (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-111">**AcquireCredentialsHandle (CredSSP)**</span></span>](acquirecredentialshandle--credssp.md)<br/>     | <span data-ttu-id="c97ca-112">Acquiert un handle aux informations d’identification préexistantes d’un principal de sécurité qui utilise le protocole CredSSP (Credential Security Support Provider).</span><span class="sxs-lookup"><span data-stu-id="c97ca-112">Acquires a handle to preexisting credentials of a security principal that is using Credential Security Support Provider (CredSSP).</span></span><br/> |
| [<span data-ttu-id="c97ca-113">**AcquireCredentialsHandle (Digest)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-113">**AcquireCredentialsHandle (Digest)**</span></span>](acquirecredentialshandle--digest.md)<br/>       | <span data-ttu-id="c97ca-114">Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Digest.</span><span class="sxs-lookup"><span data-stu-id="c97ca-114">Acquires a handle to preexisting credentials of a security principal that is using Digest.</span></span><br/>                                         |
| [<span data-ttu-id="c97ca-115">**AcquireCredentialsHandle (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-115">**AcquireCredentialsHandle (Kerberos)**</span></span>](acquirecredentialshandle--kerberos.md)<br/>   | <span data-ttu-id="c97ca-116">Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c97ca-116">Acquires a handle to preexisting credentials of a security principal that is using Kerberos.</span></span><br/>                                       |
| [<span data-ttu-id="c97ca-117">**AcquireCredentialsHandle (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-117">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)<br/> | <span data-ttu-id="c97ca-118">Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c97ca-118">Acquires a handle to preexisting credentials of a security principal that is using Negotiate.</span></span><br/>                                      |
| [<span data-ttu-id="c97ca-119">**AcquireCredentialsHandle (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-119">**AcquireCredentialsHandle (NTLM)**</span></span>](acquirecredentialshandle--ntlm.md)<br/>           | <span data-ttu-id="c97ca-120">Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise NTLM.</span><span class="sxs-lookup"><span data-stu-id="c97ca-120">Acquires a handle to preexisting credentials of a security principal that is using NTLM.</span></span><br/>                                           |
| [<span data-ttu-id="c97ca-121">**AcquireCredentialsHandle (SChannel)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-121">**AcquireCredentialsHandle (Schannel)**</span></span>](acquirecredentialshandle--schannel.md)<br/>   | <span data-ttu-id="c97ca-122">Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Schannel.</span><span class="sxs-lookup"><span data-stu-id="c97ca-122">Acquires a handle to preexisting credentials of a security principal that is using Schannel.</span></span><br/>                                       |



 

## <a name="syntax"></a><span data-ttu-id="c97ca-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c97ca-123">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c97ca-124">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c97ca-124">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97ca-125">*pszPrincipal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-125">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-126">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.</span><span class="sxs-lookup"><span data-stu-id="c97ca-126">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="c97ca-127">Lorsque vous utilisez le SSP Digest, ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c97ca-127">When using the Digest SSP, this parameter is optional.</span></span>

<span data-ttu-id="c97ca-128">Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-128">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="c97ca-129">Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="c97ca-129">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="c97ca-130">Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="c97ca-130">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="c97ca-131">*pszPackage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-131">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-132">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="c97ca-132">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="c97ca-133">Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="c97ca-133">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="c97ca-134">Une fois qu’un contexte est établi, [**QueryContextAttributes (général)**](querycontextattributes--general.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c97ca-134">After a context is established, [**QueryContextAttributes (General)**](querycontextattributes--general.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="c97ca-135">Lorsque vous utilisez le SSP Digest, définissez ce paramètre sur WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="c97ca-135">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

<span data-ttu-id="c97ca-136">Lorsque vous utilisez le SSP Schannel, définissez ce paramètre sur UNISP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="c97ca-136">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-137">*fCredentialUse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-137">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-138">Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="c97ca-138">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="c97ca-139">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c97ca-139">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c97ca-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c97ca-140">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="c97ca-141">Signification</span><span class="sxs-lookup"><span data-stu-id="c97ca-141">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="c97ca-142"><dt>**SECPKG \_ \_ \_ Accès**</dt> automatique à cred-limité <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-142"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="c97ca-143">La sécurité n’utilise pas les informations d’identification d’ouverture de session par défaut ou les informations d’identification du [Gestionnaire d’informations d’identification](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c97ca-143">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="c97ca-144">Cette valeur est prise en charge uniquement par la [*délégation conpressionnelle*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c97ca-144">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="c97ca-145">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c97ca-145">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="c97ca-146"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-146"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="c97ca-147">Validez les informations d’identification entrantes ou utilisez des informations d’identification locales pour préparer un jeton sortant.</span><span class="sxs-lookup"><span data-stu-id="c97ca-147">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="c97ca-148">Cet indicateur active à la fois d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c97ca-148">This flag enables both other flags.</span></span> <span data-ttu-id="c97ca-149">Cet indicateur n’est pas valide avec les SSP condensé et Schannel.</span><span class="sxs-lookup"><span data-stu-id="c97ca-149">This flag is not valid with the Digest and Schannel SSPs.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="c97ca-150"><dt>**SECPKG \_ cred \_ entrant**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-150"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="c97ca-151">Validez les informations d’identification du serveur entrant.</span><span class="sxs-lookup"><span data-stu-id="c97ca-151">Validate an incoming server credential.</span></span> <span data-ttu-id="c97ca-152">Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) ou [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="c97ca-152">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) or [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) is called.</span></span> <span data-ttu-id="c97ca-153">Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ .</span><span class="sxs-lookup"><span data-stu-id="c97ca-153">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="c97ca-154">La validation est spécifique au package.</span><span class="sxs-lookup"><span data-stu-id="c97ca-154">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="c97ca-155"><dt>**SECPKG \_ cred \_ sortant**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-155"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="c97ca-156">Autorisez les informations d’identification du client local à préparer un jeton sortant.</span><span class="sxs-lookup"><span data-stu-id="c97ca-156">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="c97ca-157"><dt>**SECPKG \_ \_Stratégie de processus cred \_ \_ uniquement**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-157"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="c97ca-158">La fonction traite la stratégie de serveur et retourne **sec \_ E \_ sans \_ informations d’identification**, ce qui indique que l’application doit demander des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c97ca-158">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="c97ca-159">Cette valeur est prise en charge uniquement par la [*délégation conpressionnelle*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c97ca-159">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="c97ca-160">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c97ca-160">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="c97ca-161">*pvLogonID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-161">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-162">Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c97ca-162">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="c97ca-163">Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau.</span><span class="sxs-lookup"><span data-stu-id="c97ca-163">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="c97ca-164">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-164">This parameter can be **NULL**.</span></span>

<span data-ttu-id="c97ca-165">Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-165">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-166">*pAuthData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-166">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-167">Pointeur vers des données spécifiques au package.</span><span class="sxs-lookup"><span data-stu-id="c97ca-167">A pointer to package-specific data.</span></span> <span data-ttu-id="c97ca-168">Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="c97ca-168">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="c97ca-169">Pour utiliser les informations d’identification fournies, transmettez une structure d' [**\_ \_ \_ identité Winnt auth s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui comprend ces informations d’identification dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="c97ca-169">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="c97ca-170">Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="c97ca-170">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="c97ca-171">Lorsque vous utilisez le SSP Digest, ce paramètre est un pointeur vers une structure d’identité d’authentification [**\_ winnt \_ \_ s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui contient les informations d’authentification à utiliser pour localiser les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c97ca-171">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

<span data-ttu-id="c97ca-172">Quand vous utilisez le SSP Schannel, spécifiez une structure [**Schannel \_ cred**](/windows/win32/api/schannel/ns-schannel-schannel_cred) qui indique le protocole à utiliser et les paramètres des différentes fonctionnalités de canal personnalisables.</span><span class="sxs-lookup"><span data-stu-id="c97ca-172">When using the Schannel SSP, specify an [**SCHANNEL\_CRED**](/windows/win32/api/schannel/ns-schannel-schannel_cred) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

<span data-ttu-id="c97ca-173">Lors de l’utilisation des packages NTLM ou Negotiate, les longueurs maximales de caractères pour le nom d’utilisateur, le mot de passe et le domaine sont respectivement 256, 256 et 15.</span><span class="sxs-lookup"><span data-stu-id="c97ca-173">When using the NTLM or Negotiate packages, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-174">*pGetKeyFn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-174">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-175">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-175">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-176">*pvGetKeyArgument* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-176">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-177">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-177">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-178">*phCredential* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-178">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-179">Pointeur vers une structure [CredHandle](sspi-handles.md) pour recevoir le handle d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c97ca-179">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="c97ca-180">*ptsExpiry* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-180">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ca-181">Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent.</span><span class="sxs-lookup"><span data-stu-id="c97ca-181">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="c97ca-182">La valeur retournée dans cette structure d' **horodatage** dépend de la [*délégation avec restriction*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c97ca-182">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c97ca-183">Le [*package de sécurité*](../secgloss/s-gly.md) doit retourner cette valeur en heure locale.</span><span class="sxs-lookup"><span data-stu-id="c97ca-183">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="c97ca-184">Ce paramètre est défini sur une durée maximale constante.</span><span class="sxs-lookup"><span data-stu-id="c97ca-184">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="c97ca-185">Il n’y a pas de délai d’expiration pour les informations d’identification ou les informations d’identification du [*contexte de sécurité*](../secgloss/s-gly.md)Digest ou lors de l’utilisation du SSP Digest.</span><span class="sxs-lookup"><span data-stu-id="c97ca-185">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

<span data-ttu-id="c97ca-186">Lorsque vous utilisez le SSP Schannel, ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c97ca-186">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="c97ca-187">Lorsque les informations d’identification à utiliser pour l’authentification sont un certificat, ce paramètre reçoit l’heure d’expiration de ce certificat.</span><span class="sxs-lookup"><span data-stu-id="c97ca-187">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="c97ca-188">Si aucun certificat n’a été fourni, une valeur de temps maximale est retournée.</span><span class="sxs-lookup"><span data-stu-id="c97ca-188">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97ca-189">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c97ca-189">Return value</span></span>

<span data-ttu-id="c97ca-190">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c97ca-190">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="c97ca-191">Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="c97ca-191">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="c97ca-192">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c97ca-192">Return code</span></span>                                                                                                 | <span data-ttu-id="c97ca-193">Description</span><span class="sxs-lookup"><span data-stu-id="c97ca-193">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c97ca-194"><dt>**s \_ E \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-194"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="c97ca-195">La mémoire disponible est insuffisante pour terminer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="c97ca-195">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="c97ca-196"><dt>**SEC \_ E \_ \_ erreur interne**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-196"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="c97ca-197">Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c97ca-197">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="c97ca-198"><dt>**s \_ E \_ aucune \_ information d’identification**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-198"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="c97ca-199">Aucune information d’identification n’est disponible dans la [*délégation conpressionnelle*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c97ca-199">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="c97ca-200"><dt>**SEC \_ E \_ non \_ propriétaire**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-200"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="c97ca-201">L’appelant de la fonction n’a pas les informations d’identification nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c97ca-201">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="c97ca-202"><dt>**SEC \_ E \_ SECPKG \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-202"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="c97ca-203">Le [*package de sécurité*](../secgloss/s-gly.md) demandé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c97ca-203">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="c97ca-204"><dt>**SEC \_ E \_ \_ informations d’identification inconnues**</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-204"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="c97ca-205">Les informations d’identification fournies au package n’ont pas été reconnues.</span><span class="sxs-lookup"><span data-stu-id="c97ca-205">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c97ca-206">Notes</span><span class="sxs-lookup"><span data-stu-id="c97ca-206">Remarks</span></span>

<span data-ttu-id="c97ca-207">La fonction **AcquireCredentialsHandle (General)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="c97ca-207">The **AcquireCredentialsHandle (General)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c97ca-208">Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner.</span><span class="sxs-lookup"><span data-stu-id="c97ca-208">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="c97ca-209">Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) et [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="c97ca-209">This handle can be used in subsequent calls to the [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) and [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) functions.</span></span>

<span data-ttu-id="c97ca-210">En général, **AcquireCredentialsHandle (général)** ne permet pas à un processus d’obtenir un handle pour les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c97ca-210">In general, **AcquireCredentialsHandle (General)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="c97ca-211">Toutefois, un appelant avec \_ \_ le [*privilège*](../secgloss/s-gly.md) se TCB nom a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session.</span><span class="sxs-lookup"><span data-stu-id="c97ca-211">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="c97ca-212">En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="c97ca-212">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="c97ca-213">Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="c97ca-213">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="c97ca-214">Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c97ca-214">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="c97ca-215">Pour les appelants en mode noyau, les différences suivantes doivent être notées :</span><span class="sxs-lookup"><span data-stu-id="c97ca-215">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="c97ca-216">Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c97ca-216">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="c97ca-217">Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.</span><span class="sxs-lookup"><span data-stu-id="c97ca-217">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="c97ca-218">Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="c97ca-218">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97ca-219">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c97ca-219">Requirements</span></span>



| <span data-ttu-id="c97ca-220">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c97ca-220">Requirement</span></span> | <span data-ttu-id="c97ca-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="c97ca-221">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97ca-222">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97ca-222">Minimum supported client</span></span><br/> | <span data-ttu-id="c97ca-223">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-223">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c97ca-224">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97ca-224">Minimum supported server</span></span><br/> | <span data-ttu-id="c97ca-225">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c97ca-225">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c97ca-226">En-tête</span><span class="sxs-lookup"><span data-stu-id="c97ca-226">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97ca-227"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-227"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="c97ca-228">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c97ca-228">Library</span></span><br/>                  | <dl> <span data-ttu-id="c97ca-229"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-229"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="c97ca-230">DLL</span><span class="sxs-lookup"><span data-stu-id="c97ca-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c97ca-231"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c97ca-231"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="c97ca-232">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c97ca-232">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c97ca-233">**AcquireCredentialsHandleW** (Unicode) et **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c97ca-233">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c97ca-234">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c97ca-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97ca-235">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="c97ca-235">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="c97ca-236">**AcceptSecurityContext (général)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-236">**AcceptSecurityContext (General)**</span></span>](acceptsecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="c97ca-237">**InitializeSecurityContext (général)**</span><span class="sxs-lookup"><span data-stu-id="c97ca-237">**InitializeSecurityContext (General)**</span></span>](initializesecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="c97ca-238">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="c97ca-238">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
