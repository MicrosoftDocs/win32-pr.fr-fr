---
description: Horodatage l’objet spécifié et retourne éventuellement un pointeur vers une structure de contexte de signataire \_ qui contient un pointeur vers un objet BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758770"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="b7aff-103">SignerTimeStampEx fonction)</span><span class="sxs-lookup"><span data-stu-id="b7aff-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="b7aff-104">L’heure de la fonction **SignerTimeStampEx** marque l’objet spécifié et retourne éventuellement un pointeur vers une structure de [**\_ contexte de signataire**](signer-context.md) qui contient un pointeur vers un [*objet BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b7aff-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="b7aff-105">Cette fonction prend en charge l’horodatage Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b7aff-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="b7aff-106">Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="b7aff-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="b7aff-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="b7aff-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="b7aff-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="b7aff-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b7aff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7aff-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="b7aff-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7aff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7aff-111">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b7aff-112">Reserved.</span></span> <span data-ttu-id="b7aff-113">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b7aff-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b7aff-114">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-115">Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.</span><span class="sxs-lookup"><span data-stu-id="b7aff-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="b7aff-116">*pwszHttpTimeStamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-117">Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="b7aff-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="b7aff-118">*psRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b7aff-119">Optional.</span></span> <span data-ttu-id="b7aff-120">Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="b7aff-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="b7aff-121">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="b7aff-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="b7aff-122">*pSipData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-123">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b7aff-123">Optional.</span></span> <span data-ttu-id="b7aff-124">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="b7aff-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="b7aff-125">Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="b7aff-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="b7aff-126">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="b7aff-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="b7aff-127">*ppSignerContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aff-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b7aff-128">Optional.</span></span> <span data-ttu-id="b7aff-129">Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé.</span><span class="sxs-lookup"><span data-stu-id="b7aff-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="b7aff-130">Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="b7aff-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7aff-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7aff-131">Return value</span></span>

<span data-ttu-id="b7aff-132">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7aff-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="b7aff-133">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7aff-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b7aff-134">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b7aff-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7aff-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7aff-135">Requirements</span></span>



| <span data-ttu-id="b7aff-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7aff-136">Requirement</span></span> | <span data-ttu-id="b7aff-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7aff-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7aff-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7aff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b7aff-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7aff-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7aff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b7aff-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7aff-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7aff-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b7aff-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7aff-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7aff-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7aff-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7aff-144">See also</span></span>

<dl> <span data-ttu-id="b7aff-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b7aff-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b7aff-146">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="b7aff-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
