---
description: Horodatage l’objet spécifié. Cette fonction prend en charge l’horodatage Authenticode. Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952701"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="4b25c-105">SignerTimeStamp fonction)</span><span class="sxs-lookup"><span data-stu-id="4b25c-105">SignerTimeStamp function</span></span>

<span data-ttu-id="4b25c-106">L’heure de la fonction **SignerTimeStamp** marque l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="4b25c-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="4b25c-107">Cette fonction prend en charge l’horodatage Authenticode.</span><span class="sxs-lookup"><span data-stu-id="4b25c-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="4b25c-108">Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="4b25c-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="4b25c-109">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="4b25c-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="4b25c-110">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="4b25c-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b25c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b25c-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="4b25c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b25c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b25c-113">*pSubjectInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25c-114">Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.</span><span class="sxs-lookup"><span data-stu-id="4b25c-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="4b25c-115">*pwszHttpTimeStamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25c-116">Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="4b25c-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="4b25c-117">*psRequest* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25c-118">Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="4b25c-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="4b25c-119">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="4b25c-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="4b25c-120">*pSipData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b25c-121">Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP.</span><span class="sxs-lookup"><span data-stu-id="4b25c-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="4b25c-122">Le format et le contenu de ce sont définis par le fournisseur SIP.</span><span class="sxs-lookup"><span data-stu-id="4b25c-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="4b25c-123">Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="4b25c-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b25c-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b25c-124">Return value</span></span>

<span data-ttu-id="4b25c-125">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b25c-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="4b25c-126">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4b25c-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4b25c-127">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4b25c-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b25c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b25c-128">Requirements</span></span>



| <span data-ttu-id="4b25c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b25c-129">Requirement</span></span> | <span data-ttu-id="4b25c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b25c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b25c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4b25c-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b25c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b25c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4b25c-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b25c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b25c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4b25c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b25c-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b25c-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
