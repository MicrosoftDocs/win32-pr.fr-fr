---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Digest.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: AcquireCredentialsHandle (Digest), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209711"
---
# <a name="acquirecredentialshandle-digest-function"></a><span data-ttu-id="5003f-103">AcquireCredentialsHandle (Digest) (fonction)</span><span class="sxs-lookup"><span data-stu-id="5003f-103">AcquireCredentialsHandle (Digest) function</span></span>

<span data-ttu-id="5003f-104">La fonction **AcquireCredentialsHandle (Digest)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5003f-104">The **AcquireCredentialsHandle (Digest)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5003f-105">Ce descripteur est requis par les fonctions [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) et [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="5003f-105">This handle is required by the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span> <span data-ttu-id="5003f-106">Il peut s’agir *d’informations d’identification* préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="5003f-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="5003f-107">Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="5003f-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5003f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5003f-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5003f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5003f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5003f-110">*pszPrincipal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.</span><span class="sxs-lookup"><span data-stu-id="5003f-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="5003f-112">Lorsque vous utilisez le SSP Digest, ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5003f-112">When using the Digest SSP, this parameter is optional.</span></span>

> [!Note]  
> <span data-ttu-id="5003f-113">Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="5003f-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="5003f-114">Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="5003f-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="5003f-115">*pszPackage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="5003f-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="5003f-117">Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="5003f-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="5003f-118">Une fois qu’un contexte est établi, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5003f-118">After a context is established, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="5003f-119">Lorsque vous utilisez le SSP Digest, définissez ce paramètre sur WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="5003f-119">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-120">*fCredentialUse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-121">Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="5003f-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="5003f-122">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5003f-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5003f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5003f-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="5003f-124">Signification</span><span class="sxs-lookup"><span data-stu-id="5003f-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="5003f-125"><dt>**SECPKG \_ cred \_ entrant**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="5003f-126">Validez les informations d’identification du serveur entrant.</span><span class="sxs-lookup"><span data-stu-id="5003f-126">Validate an incoming server credential.</span></span> <span data-ttu-id="5003f-127">Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) ou [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="5003f-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) or [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) is called.</span></span> <span data-ttu-id="5003f-128">Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ .</span><span class="sxs-lookup"><span data-stu-id="5003f-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="5003f-129">La validation est spécifique au package.</span><span class="sxs-lookup"><span data-stu-id="5003f-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="5003f-130"><dt>**SECPKG \_ cred \_ sortant**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="5003f-131">Autorisez les informations d’identification du client local à préparer un jeton sortant.</span><span class="sxs-lookup"><span data-stu-id="5003f-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="5003f-132">*pvLogonID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-132">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-133">Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5003f-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="5003f-134">Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau.</span><span class="sxs-lookup"><span data-stu-id="5003f-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="5003f-135">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5003f-135">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-136">*pAuthData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-136">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-137">Pointeur vers des données spécifiques au package.</span><span class="sxs-lookup"><span data-stu-id="5003f-137">A pointer to package-specific data.</span></span> <span data-ttu-id="5003f-138">Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="5003f-138">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="5003f-139">Pour utiliser les informations d’identification fournies, transmettez une structure d' [**\_ \_ \_ identité Winnt auth s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui comprend ces informations d’identification dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5003f-139">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="5003f-140">Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="5003f-140">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="5003f-141">Lorsque vous utilisez le SSP Digest, ce paramètre est un pointeur vers une structure d’identité d’authentification [**\_ winnt \_ \_ s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui contient les informations d’authentification à utiliser pour localiser les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="5003f-141">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-142">*pGetKeyFn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-143">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5003f-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-144">*pvGetKeyArgument* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5003f-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-145">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5003f-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-146">*phCredential* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5003f-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-147">Pointeur vers une structure [CredHandle](sspi-handles.md) pour recevoir le handle d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="5003f-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="5003f-148">*ptsExpiry* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5003f-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5003f-149">Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent.</span><span class="sxs-lookup"><span data-stu-id="5003f-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="5003f-150">La valeur retournée dans cette structure d' **horodatage** dépend de la [*délégation avec restriction*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5003f-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5003f-151">Le [*package de sécurité*](../secgloss/s-gly.md) doit retourner cette valeur en heure locale.</span><span class="sxs-lookup"><span data-stu-id="5003f-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="5003f-152">Ce paramètre est défini sur une durée maximale constante.</span><span class="sxs-lookup"><span data-stu-id="5003f-152">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="5003f-153">Il n’y a pas de délai d’expiration pour les informations d’identification ou les informations d’identification du [*contexte de sécurité*](../secgloss/s-gly.md)Digest ou lors de l’utilisation du SSP Digest.</span><span class="sxs-lookup"><span data-stu-id="5003f-153">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5003f-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5003f-154">Return value</span></span>

<span data-ttu-id="5003f-155">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5003f-155">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="5003f-156">Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="5003f-156">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="5003f-157">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5003f-157">Return code</span></span>                                                                                                 | <span data-ttu-id="5003f-158">Description</span><span class="sxs-lookup"><span data-stu-id="5003f-158">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5003f-159"><dt>**s \_ E \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-159"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="5003f-160">La mémoire disponible est insuffisante pour terminer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="5003f-160">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="5003f-161"><dt>**SEC \_ E \_ \_ erreur interne**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-161"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="5003f-162">Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5003f-162">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="5003f-163"><dt>**s \_ E \_ aucune \_ information d’identification**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-163"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="5003f-164">Aucune information d’identification n’est disponible dans la [*délégation conpressionnelle*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5003f-164">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="5003f-165"><dt>**SEC \_ E \_ non \_ propriétaire**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-165"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="5003f-166">L’appelant de la fonction n’a pas les informations d’identification nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5003f-166">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="5003f-167"><dt>**SEC \_ E \_ SECPKG \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-167"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="5003f-168">Le [*package de sécurité*](../secgloss/s-gly.md) demandé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="5003f-168">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5003f-169"><dt>**SEC \_ E \_ \_ informations d’identification inconnues**</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-169"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="5003f-170">Les informations d’identification fournies au package n’ont pas été reconnues.</span><span class="sxs-lookup"><span data-stu-id="5003f-170">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5003f-171">Notes</span><span class="sxs-lookup"><span data-stu-id="5003f-171">Remarks</span></span>

<span data-ttu-id="5003f-172">La fonction **AcquireCredentialsHandle (Digest)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="5003f-172">The **AcquireCredentialsHandle (Digest)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5003f-173">Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner.</span><span class="sxs-lookup"><span data-stu-id="5003f-173">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="5003f-174">Ce descripteur peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) et [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="5003f-174">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span>

<span data-ttu-id="5003f-175">En général, **AcquireCredentialsHandle (Digest)** ne permet pas à un processus d’obtenir un handle pour les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5003f-175">In general, **AcquireCredentialsHandle (Digest)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="5003f-176">Toutefois, un appelant avec \_ \_ le [*privilège*](../secgloss/s-gly.md) se TCB nom a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session.</span><span class="sxs-lookup"><span data-stu-id="5003f-176">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="5003f-177">En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="5003f-177">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="5003f-178">Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="5003f-178">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="5003f-179">Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5003f-179">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="5003f-180">Pour les appelants en mode noyau, les différences suivantes doivent être notées :</span><span class="sxs-lookup"><span data-stu-id="5003f-180">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="5003f-181">Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5003f-181">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="5003f-182">Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.</span><span class="sxs-lookup"><span data-stu-id="5003f-182">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="5003f-183">Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="5003f-183">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5003f-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5003f-184">Requirements</span></span>



| <span data-ttu-id="5003f-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5003f-185">Requirement</span></span> | <span data-ttu-id="5003f-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="5003f-186">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5003f-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5003f-187">Minimum supported client</span></span><br/> | <span data-ttu-id="5003f-188">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5003f-188">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5003f-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5003f-189">Minimum supported server</span></span><br/> | <span data-ttu-id="5003f-190">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5003f-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5003f-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="5003f-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="5003f-192"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-192"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="5003f-193">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5003f-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="5003f-194"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-194"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="5003f-195">DLL</span><span class="sxs-lookup"><span data-stu-id="5003f-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5003f-196"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5003f-196"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="5003f-197">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5003f-197">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5003f-198">**AcquireCredentialsHandleW** (Unicode) et **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5003f-198">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5003f-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5003f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5003f-200">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="5003f-200">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="5003f-201">**AcceptSecurityContext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="5003f-201">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="5003f-202">**InitializeSecurityContext (condensé)**</span><span class="sxs-lookup"><span data-stu-id="5003f-202">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="5003f-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="5003f-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
