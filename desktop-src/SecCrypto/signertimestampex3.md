---
description: Horodatage l’objet spécifié et prend en charge la définition des horodatages sur plusieurs signatures.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111974"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="edf06-103">SignerTimeStampEx3 fonction)</span><span class="sxs-lookup"><span data-stu-id="edf06-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="edf06-104">L’heure de la fonction **SignerTimeStampEx3** marque l’objet spécifié et prend en charge la définition des horodatages sur plusieurs signatures.</span><span class="sxs-lookup"><span data-stu-id="edf06-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="edf06-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="edf06-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="edf06-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="edf06-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="edf06-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edf06-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="edf06-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edf06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf06-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edf06-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-110">Indicateur qui spécifie le type d’horodatage à générer.</span><span class="sxs-lookup"><span data-stu-id="edf06-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="edf06-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="edf06-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="edf06-112">Les valeurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="edf06-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edf06-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf06-113">Value</span></span></th>
<th><span data-ttu-id="edf06-114">Signification</span><span class="sxs-lookup"><span data-stu-id="edf06-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="edf06-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="edf06-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="edf06-116">Spécifie un horodatage Authenticode.</span><span class="sxs-lookup"><span data-stu-id="edf06-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="edf06-117">Authenticode n’est plus le type d’horodatage préféré.</span><span class="sxs-lookup"><span data-stu-id="edf06-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="edf06-118">La prise en charge des horodatages Authenticode peut être supprimée à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="edf06-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="edf06-119">Nous vous recommandons d’utiliser à la place la RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="edf06-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="edf06-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="edf06-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="edf06-121">Spécifie un horodatage conforme à la norme RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="edf06-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="edf06-122">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edf06-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-123">Spécifie le numéro de séquence de la signature à laquelle l’horodateur sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="edf06-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="edf06-124">Si cette valeur est égale à zéro (0), la signature externe sera horodatage.</span><span class="sxs-lookup"><span data-stu-id="edf06-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-125">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edf06-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-126">Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.</span><span class="sxs-lookup"><span data-stu-id="edf06-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-127">*pwszHttpTimeStamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edf06-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-128">Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="edf06-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-129">*pszAlgorithmOid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edf06-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-130">Algorithme de hachage à utiliser pour exécuter des horodatages conformes à la norme RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="edf06-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="edf06-131">Ce paramètre est ignoré pour les horodatages Authenticode.</span><span class="sxs-lookup"><span data-stu-id="edf06-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-132">*psRequest* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="edf06-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="edf06-133">Optional.</span></span> <span data-ttu-id="edf06-134">Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="edf06-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="edf06-135">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="edf06-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-136">*pSipData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="edf06-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-137">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="edf06-137">Optional.</span></span> <span data-ttu-id="edf06-138">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="edf06-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="edf06-139">Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="edf06-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="edf06-140">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="edf06-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-141">*ppSignerContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="edf06-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-142">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="edf06-142">Optional.</span></span> <span data-ttu-id="edf06-143">Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé.</span><span class="sxs-lookup"><span data-stu-id="edf06-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="edf06-144">Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="edf06-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-145">*pCryptoPolicy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="edf06-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edf06-146">S’il est présent, pointeur vers une structure de [**\_ \_ \_ paragraphe de signe fort de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) qui contient les paramètres utilisés pour vérifier les signatures fortes.</span><span class="sxs-lookup"><span data-stu-id="edf06-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="edf06-147">L’horodatage doit passer cette stratégie de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="edf06-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="edf06-148">*Respecté*</span><span class="sxs-lookup"><span data-stu-id="edf06-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="edf06-149">Réservé.</span><span class="sxs-lookup"><span data-stu-id="edf06-149">Reserved.</span></span> <span data-ttu-id="edf06-150">Cette valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="edf06-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edf06-151">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edf06-151">Return value</span></span>

<span data-ttu-id="edf06-152">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="edf06-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="edf06-153">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="edf06-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="edf06-154">Les codes d’erreur possibles retournés par cette fonction incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="edf06-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="edf06-155">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="edf06-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edf06-156">Code de retour</span><span class="sxs-lookup"><span data-stu-id="edf06-156">Return code</span></span></th>
<th><span data-ttu-id="edf06-157">Description</span><span class="sxs-lookup"><span data-stu-id="edf06-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="edf06-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="edf06-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="edf06-159">Cette erreur peut être retournée pour les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="edf06-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="edf06-160">Vous devez définir <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> ou <strong>SIGNER_TIMESTAMP_RFC3161</strong> pour le paramètre <em>dwFlags</em> .</span><span class="sxs-lookup"><span data-stu-id="edf06-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="edf06-161">Le paramètre <em>conserved</em> doit avoir la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="edf06-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="edf06-162">Si vous définissez l’indicateur <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> dans le paramètre <em>dwFlags</em> , vous devez définir le paramètre <em>dwIndex</em> sur zéro.</span><span class="sxs-lookup"><span data-stu-id="edf06-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="edf06-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edf06-163">Requirements</span></span>



| <span data-ttu-id="edf06-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edf06-164">Requirement</span></span> | <span data-ttu-id="edf06-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf06-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edf06-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf06-166">Minimum supported client</span></span><br/> | <span data-ttu-id="edf06-167">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edf06-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="edf06-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf06-168">Minimum supported server</span></span><br/> | <span data-ttu-id="edf06-169">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edf06-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="edf06-170">DLL</span><span class="sxs-lookup"><span data-stu-id="edf06-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edf06-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf06-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edf06-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf06-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf06-173">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="edf06-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="edf06-174">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="edf06-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="edf06-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="edf06-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
