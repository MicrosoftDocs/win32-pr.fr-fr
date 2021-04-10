---
description: Signe le fichier spécifié et retourne un pointeur vers les données signées.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755564"
---
# <a name="signersignex-function"></a><span data-ttu-id="61fbf-103">SignerSignEx fonction)</span><span class="sxs-lookup"><span data-stu-id="61fbf-103">SignerSignEx function</span></span>

<span data-ttu-id="61fbf-104">La fonction **SignerSignEx** signe le fichier spécifié et retourne un pointeur vers les données signées.</span><span class="sxs-lookup"><span data-stu-id="61fbf-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="61fbf-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="61fbf-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="61fbf-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="61fbf-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="61fbf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61fbf-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="61fbf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61fbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fbf-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-110">Modifie le comportement de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="61fbf-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="61fbf-111">Si le fichier à signer est un fichier exécutable portable (PE), il peut s’agir de zéro ou d’une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61fbf-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="61fbf-112">Ces identificateurs sont définis dans Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="61fbf-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="61fbf-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="61fbf-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="61fbf-114">Signification</span><span class="sxs-lookup"><span data-stu-id="61fbf-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="61fbf-115"><dt>**SPC \_ \_ \_ \_ \_ Indicateur de hachages de page PE exclure**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="61fbf-116">Excluez les hachages de page lors de la création de données SIP indirectes pour le fichier PE.</span><span class="sxs-lookup"><span data-stu-id="61fbf-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="61fbf-117">Cet indicateur est prioritaire par rapport à l’indicateur d' **\_ indicateur de \_ \_ \_ hachage \_ de page PE Inc** .</span><span class="sxs-lookup"><span data-stu-id="61fbf-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="61fbf-118">Si vous ne spécifiez pas l’indicateur de **\_ \_ \_ \_ hachages \_ de page de hachage de page PE de SPC exclure** ou si l’indicateur de **\_ \_ \_ \_ hachage \_ de page PE Inc** . est spécifié, la valeur définie avec la fonction [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) est utilisée pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="61fbf-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="61fbf-119">La valeur par défaut de ce paramètre est d’exclure les hachages de page lors de la création de données SIP indirectes pour les fichiers PE.</span><span class="sxs-lookup"><span data-stu-id="61fbf-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="61fbf-120">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61fbf-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="61fbf-121"><dt>**SPC \_ \_Indicateur de \_ \_ \_ table \_ addr d’importation PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="61fbf-122">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61fbf-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="61fbf-123"><dt>**SPC \_ \_Indicateur d' \_ \_ informations de \_ DÉbogage PE de Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="61fbf-124">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61fbf-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="61fbf-125"><dt>**SPC \_ \_Indicateur de \_ ressources \_ PE Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="61fbf-126">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61fbf-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="61fbf-127"><dt>**SPC \_ \_ \_ \_ \_ Identificateurs de hachage de page PE de Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="61fbf-128">Inclure les hachages de page lors de la création de données SIP indirectes pour le fichier PE.</span><span class="sxs-lookup"><span data-stu-id="61fbf-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="61fbf-129">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61fbf-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="61fbf-130">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-131">Pointeur vers une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui spécifie l’objet à signer.</span><span class="sxs-lookup"><span data-stu-id="61fbf-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-132">*pSignerCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-133">Pointeur vers une structure de [**\_ certificat de signataire**](signer-cert.md) qui spécifie le certificat à utiliser pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61fbf-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-134">*pSignatureInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-135">Pointeur vers une structure d' [**\_ \_ informations de signature de signataire**](signer-signature-info.md) qui contient des informations sur la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61fbf-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-136">*pProviderInfo* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-137">Pointeur vers une structure d' [**\_ \_ informations de fournisseur de signataires**](signer-provider-info.md) qui spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de clé privée utilisés pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61fbf-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="61fbf-138">Si la valeur de ce paramètre est **null**, la valeur du paramètre *pSignerCert* doit spécifier un certificat associé à un CSP.</span><span class="sxs-lookup"><span data-stu-id="61fbf-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-139">*pwszHttpTimeStamp* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-140">URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="61fbf-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-141">*psRequest* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-142">Pointeur vers un tableau de structures [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) de chiffre qui sont ajoutées à une demande de signature.</span><span class="sxs-lookup"><span data-stu-id="61fbf-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="61fbf-143">Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* ne contient pas de valeur valide qui n’est pas **null**.</span><span class="sxs-lookup"><span data-stu-id="61fbf-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-144">*pSipData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-145">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP.</span><span class="sxs-lookup"><span data-stu-id="61fbf-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="61fbf-146">Le format et le contenu de ce sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="61fbf-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="61fbf-147">*ppSignerContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61fbf-148">Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l' [*objet BLOB*](../secgloss/b-gly.md)signé.</span><span class="sxs-lookup"><span data-stu-id="61fbf-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="61fbf-149">Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez la structure du **\_ contexte du signataire** en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="61fbf-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fbf-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61fbf-150">Return value</span></span>

<span data-ttu-id="61fbf-151">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="61fbf-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="61fbf-152">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="61fbf-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="61fbf-153">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="61fbf-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61fbf-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61fbf-154">Requirements</span></span>



| <span data-ttu-id="61fbf-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61fbf-155">Requirement</span></span> | <span data-ttu-id="61fbf-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="61fbf-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61fbf-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fbf-157">Minimum supported client</span></span><br/> | <span data-ttu-id="61fbf-158">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="61fbf-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fbf-159">Minimum supported server</span></span><br/> | <span data-ttu-id="61fbf-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61fbf-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61fbf-161">DLL</span><span class="sxs-lookup"><span data-stu-id="61fbf-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61fbf-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61fbf-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fbf-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61fbf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fbf-164">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="61fbf-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="61fbf-165">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="61fbf-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
