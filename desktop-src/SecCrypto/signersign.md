---
description: Signe le fichier spécifié.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522087"
---
# <a name="signersign-function"></a><span data-ttu-id="26e25-103">SignerSign fonction)</span><span class="sxs-lookup"><span data-stu-id="26e25-103">SignerSign function</span></span>

<span data-ttu-id="26e25-104">La fonction **SignerSign** signe le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="26e25-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="26e25-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="26e25-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="26e25-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="26e25-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="26e25-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26e25-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="26e25-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26e25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e25-109">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e25-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-110">Pointeur vers une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui spécifie l’objet à signer.</span><span class="sxs-lookup"><span data-stu-id="26e25-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-111">*pSignerCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e25-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-112">Pointeur vers une structure de [**\_ certificat de signataire**](signer-cert.md) qui spécifie le certificat à utiliser pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="26e25-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-113">*pSignatureInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e25-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-114">Pointeur vers une structure d' [**\_ \_ informations de signature de signataire**](signer-signature-info.md) qui contient des informations sur la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="26e25-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-115">*pProviderInfo* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26e25-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-116">Pointeur vers une structure d' [**\_ \_ informations de fournisseur de signataires**](signer-provider-info.md) qui spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de [*clé privée*](../secgloss/p-gly.md) utilisés pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="26e25-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="26e25-117">Si la valeur de ce paramètre est **null**, la valeur du paramètre *pSignerCert* doit spécifier un certificat associé à un CSP.</span><span class="sxs-lookup"><span data-stu-id="26e25-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-118">*pwszHttpTimeStamp* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26e25-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-119">URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="26e25-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-120">*psRequest* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26e25-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-121">Pointeur vers un tableau de structures [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) de chiffre qui sont ajoutées à une demande de signature.</span><span class="sxs-lookup"><span data-stu-id="26e25-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="26e25-122">Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* ne contient pas de valeur valide qui n’est pas **null**.</span><span class="sxs-lookup"><span data-stu-id="26e25-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="26e25-123">*pSipData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26e25-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26e25-124">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP.</span><span class="sxs-lookup"><span data-stu-id="26e25-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="26e25-125">Le format et le contenu de ce sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="26e25-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e25-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26e25-126">Return value</span></span>

<span data-ttu-id="26e25-127">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26e25-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="26e25-128">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="26e25-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="26e25-129">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="26e25-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26e25-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26e25-130">Requirements</span></span>



| <span data-ttu-id="26e25-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26e25-131">Requirement</span></span> | <span data-ttu-id="26e25-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="26e25-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e25-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e25-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26e25-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e25-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26e25-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e25-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26e25-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e25-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26e25-137">DLL</span><span class="sxs-lookup"><span data-stu-id="26e25-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26e25-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e25-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e25-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26e25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e25-140">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="26e25-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
