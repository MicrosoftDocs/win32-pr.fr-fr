---
description: Horodatage l’objet spécifié et retourne éventuellement un pointeur vers une structure de contexte de signataire \_ qui contient un pointeur vers un objet BLOB. Cette fonction peut être utilisée pour effectuer une infrastructure à clé publique X. 509, RFC 3161&\# 8211 ; conforme, horodatage.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522164"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="e5ca0-104">SignerTimeStampEx2 fonction)</span><span class="sxs-lookup"><span data-stu-id="e5ca0-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="e5ca0-105">L’heure de la fonction **SignerTimeStampEx2** marque l’objet spécifié et retourne éventuellement un pointeur vers une structure de [**\_ contexte de signataire**](signer-context.md) qui contient un pointeur vers un [*objet BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e5ca0-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="e5ca0-106">Cette fonction peut être utilisée pour effectuer l’infrastructure de clé publique X. 509, conforme à la norme RFC 3161, horodatage.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="e5ca0-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="e5ca0-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e5ca0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5ca0-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="e5ca0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5ca0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ca0-111">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-112">Valeur qui spécifie le type d’horodatage à générer.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="e5ca0-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="e5ca0-114">Les valeurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="e5ca0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ca0-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="e5ca0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e5ca0-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="e5ca0-117"><dt>**AUTHENTICODE de l’horodateur du signataire \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ca0-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="e5ca0-118">Spécifie un horodatage Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="e5ca0-119"><dt>**Horodatage du \_ signataire \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ca0-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="e5ca0-120">Spécifie un horodatage conforme à la norme RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e5ca0-121">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-122">Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="e5ca0-123">*pwszHttpTimeStamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-124">Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="e5ca0-125">*dwAlgId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-126">Spécifie un algorithme de hachage à utiliser pour exécuter des horodatages conformes à la norme RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="e5ca0-127">Ce paramètre est ignoré pour les horodatages Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="e5ca0-128">*psRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-129">Optional.</span></span> <span data-ttu-id="e5ca0-130">Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="e5ca0-131">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="e5ca0-132">*pSipData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-133">Optional.</span></span> <span data-ttu-id="e5ca0-134">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="e5ca0-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="e5ca0-135">Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="e5ca0-136">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="e5ca0-137">*ppSignerContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ca0-138">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-138">Optional.</span></span> <span data-ttu-id="e5ca0-139">Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="e5ca0-140">Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ca0-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ca0-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5ca0-141">Return value</span></span>

<span data-ttu-id="e5ca0-142">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="e5ca0-143">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e5ca0-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e5ca0-144">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="e5ca0-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ca0-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5ca0-145">Requirements</span></span>



| <span data-ttu-id="e5ca0-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5ca0-146">Requirement</span></span> | <span data-ttu-id="e5ca0-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ca0-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ca0-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ca0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ca0-149">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e5ca0-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ca0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ca0-151">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ca0-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5ca0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ca0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ca0-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ca0-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ca0-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5ca0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ca0-155">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="e5ca0-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="e5ca0-156">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="e5ca0-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
