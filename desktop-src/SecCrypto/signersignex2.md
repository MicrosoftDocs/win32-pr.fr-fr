---
description: Signe et heure marque le fichier spécifié, en autorisant plusieurs signatures imbriquées.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209866"
---
# <a name="signersignex2-function"></a><span data-ttu-id="b3c20-103">SignerSignEx2 fonction)</span><span class="sxs-lookup"><span data-stu-id="b3c20-103">SignerSignEx2 function</span></span>

<span data-ttu-id="b3c20-104">La fonction **SignerSignEx2** signe et met en cache l’heure du fichier spécifié, en autorisant plusieurs signatures imbriquées.</span><span class="sxs-lookup"><span data-stu-id="b3c20-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="b3c20-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="b3c20-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="b3c20-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="b3c20-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b3c20-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c20-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b3c20-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c20-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-110">Modifie le comportement de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b3c20-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="b3c20-111">Si le fichier à signer est un fichier exécutable portable (PE), il peut s’agir de zéro ou d’une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b3c20-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="b3c20-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c20-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="b3c20-113">Signification</span><span class="sxs-lookup"><span data-stu-id="b3c20-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="b3c20-114"><dt>**SPC \_ \_ \_ \_ \_ Indicateur de hachages de page PE exclure**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="b3c20-115">Excluez les hachages de page lors de la création de données SIP indirectes pour le fichier PE.</span><span class="sxs-lookup"><span data-stu-id="b3c20-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="b3c20-116">Cet indicateur est prioritaire par rapport à l’indicateur d' **\_ indicateur de \_ \_ \_ hachage \_ de page PE Inc** .</span><span class="sxs-lookup"><span data-stu-id="b3c20-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="b3c20-117">Si vous ne spécifiez pas l’indicateur de **\_ \_ \_ \_ hachages \_ de page de hachage de page PE de SPC exclure** ou si l’indicateur de **\_ \_ \_ \_ hachage \_ de page PE Inc** . est spécifié, la valeur définie avec la fonction [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) est utilisée pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b3c20-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="b3c20-118">La valeur par défaut de ce paramètre est d’exclure les hachages de page lors de la création de données SIP indirectes pour les fichiers PE.</span><span class="sxs-lookup"><span data-stu-id="b3c20-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="b3c20-119">Cette valeur est définie dans le fichier d’en-tête Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="b3c20-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="b3c20-120">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b3c20-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="b3c20-121"><dt>**SPC \_ \_Indicateur de \_ \_ \_ table \_ addr d’importation PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="b3c20-122">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b3c20-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="b3c20-123"><dt>**SPC \_ \_Indicateur d' \_ \_ informations de \_ DÉbogage PE de Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="b3c20-124">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b3c20-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="b3c20-125"><dt>**SPC \_ \_Indicateur de \_ ressources \_ PE Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="b3c20-126">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b3c20-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="b3c20-127"><dt>**SPC \_ \_ \_ \_ \_ Identificateurs de hachage de page PE de Inc**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="b3c20-128">Inclure les hachages de page lors de la création de données SIP indirectes pour le fichier PE.</span><span class="sxs-lookup"><span data-stu-id="b3c20-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="b3c20-129">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b3c20-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="b3c20-130">Cette valeur est définie dans le fichier d’en-tête Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="b3c20-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="b3c20-131"><dt>**SIG \_ Ajouter**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="b3c20-132">La signature sera imbriquée.</span><span class="sxs-lookup"><span data-stu-id="b3c20-132">The signature will be nested.</span></span> <span data-ttu-id="b3c20-133">Si vous définissez cet indicateur avant l’ajout d’une signature, la signature générée sera ajoutée en tant que signature externe.</span><span class="sxs-lookup"><span data-stu-id="b3c20-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="b3c20-134">Si vous ne définissez pas cet indicateur, la signature générée remplace la signature externe, en supprimant toutes les signatures internes.</span><span class="sxs-lookup"><span data-stu-id="b3c20-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="b3c20-135">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-136">Pointeur vers une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui spécifie l’objet à signer.</span><span class="sxs-lookup"><span data-stu-id="b3c20-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-137">*pSignerCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-138">Pointeur vers une structure de [**\_ certificat de signataire**](signer-cert.md) qui spécifie le certificat à utiliser pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b3c20-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-139">*pSignatureInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-140">Pointeur vers une structure d' [**\_ \_ informations de signature de signataire**](signer-signature-info.md) qui contient des informations sur la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b3c20-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-141">*pProviderInfo* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-142">Pointeur vers une structure d' [**\_ \_ informations de fournisseur de signataires**](signer-provider-info.md) qui spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de clé privée utilisés pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b3c20-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="b3c20-143">Si la valeur de ce paramètre est **null**, le paramètre *pSignerCert* doit spécifier un certificat associé à un CSP.</span><span class="sxs-lookup"><span data-stu-id="b3c20-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-144">*dwTimestampFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-145">Indicateurs qui seront passés à [**SignerTimeStampEx3**](signertimestampex3.md) si le paramètre *pwszHttpTimeStamp* n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b3c20-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="b3c20-146">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b3c20-146">This can be one of the following values.</span></span>



| <span data-ttu-id="b3c20-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c20-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="b3c20-148">Signification</span><span class="sxs-lookup"><span data-stu-id="b3c20-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="b3c20-149"><dt>**AUTHENTICODE de l’horodateur du signataire \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="b3c20-150">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b3c20-150">Default value.</span></span> <span data-ttu-id="b3c20-151">Spécifie un horodateur Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b3c20-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="b3c20-152"><dt>**Horodatage du \_ signataire \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="b3c20-153">Spécifie un horodateur RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="b3c20-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="b3c20-154">Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b3c20-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-155">*pszTimestampAlgorithmOid* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-156">Identificateur d’objet de l’algorithme à utiliser pour créer un horodateur RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="b3c20-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="b3c20-157">Ce paramètre est ignoré pour les horodatages Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b3c20-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-158">*pwszHttpTimeStamp* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-159">URL du serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="b3c20-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-160">*psRequest* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-161">Pointeur vers un tableau de structures d' [**\_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) de chiffre qui sont ajoutées à une demande de signature.</span><span class="sxs-lookup"><span data-stu-id="b3c20-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="b3c20-162">Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* ne contient pas de valeur valide ou a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="b3c20-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-163">*pSipData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-164">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP.</span><span class="sxs-lookup"><span data-stu-id="b3c20-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="b3c20-165">Le format et le contenu de ce sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="b3c20-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-166">*ppSignerContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-167">Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l' [*objet BLOB*](../secgloss/b-gly.md)signé.</span><span class="sxs-lookup"><span data-stu-id="b3c20-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="b3c20-168">Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez la structure du **\_ contexte du signataire** en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c20-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-169">*pCryptoPolicy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c20-170">S’il est présent, pointeur vers une structure de [**\_ \_ \_ paragraphe de signe fort de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) qui contient les paramètres utilisés pour vérifier les signatures fortes.</span><span class="sxs-lookup"><span data-stu-id="b3c20-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="b3c20-171">Si un certificat ou sa chaîne ne réussissent pas, le fichier n’est pas modifié de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="b3c20-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="b3c20-172">Si une URL est transmise pour spécifier une autorité d’horodatage (TSA), cette stratégie est également appliquée à l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="b3c20-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="b3c20-173">*Respecté*</span><span class="sxs-lookup"><span data-stu-id="b3c20-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c20-174">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b3c20-174">Reserved.</span></span> <span data-ttu-id="b3c20-175">Cette valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="b3c20-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c20-176">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3c20-176">Return value</span></span>

<span data-ttu-id="b3c20-177">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3c20-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="b3c20-178">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3c20-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b3c20-179">Les codes d’erreur possibles retournés par cette fonction incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="b3c20-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="b3c20-180">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b3c20-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="b3c20-181">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b3c20-181">Return code</span></span>                                                                                  | <span data-ttu-id="b3c20-182">Description</span><span class="sxs-lookup"><span data-stu-id="b3c20-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3c20-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b3c20-184">Si vous définissez le paramètre *dwTimestampFlags* sur **signer \_ timestamp \_ AUTHENTICODE**, vous ne pouvez pas définir le paramètre *dwFlags* sur **SIG \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="b3c20-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b3c20-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c20-185">Requirements</span></span>



| <span data-ttu-id="b3c20-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c20-186">Requirement</span></span> | <span data-ttu-id="b3c20-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c20-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c20-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c20-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c20-189">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b3c20-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c20-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c20-191">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c20-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3c20-192">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c20-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c20-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c20-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c20-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c20-195">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="b3c20-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="b3c20-196">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="b3c20-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="b3c20-197">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="b3c20-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
