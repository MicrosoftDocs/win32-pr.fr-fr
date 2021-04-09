---
description: Obtient un handle vers un fournisseur de services de chiffrement (CSP) basé sur un fichier de clé privée ou un nom de conteneur de clé.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869001"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="68886-103">PvkGetCryptProv fonction)</span><span class="sxs-lookup"><span data-stu-id="68886-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68886-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="68886-104">This API is deprecated.</span></span> <span data-ttu-id="68886-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="68886-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="68886-106">La fonction **PvkGetCryptProv** obtient un descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) basé sur un fichier de [*clé privée*](../secgloss/p-gly.md) ou un nom de conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="68886-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="68886-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="68886-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="68886-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="68886-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="68886-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68886-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="68886-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68886-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68886-111">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-112">Si un mot de passe est requis pour déchiffrer le fichier de clé privée, ce paramètre est un handle vers le parent de la boîte de dialogue de mot de passe. dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="68886-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="68886-113">*pwszCaption* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-114">Pointeur vers une chaîne se terminant par null pour la légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="68886-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="68886-115">*pwszCapiProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-116">Pointeur vers une chaîne se terminant par null pour le nom du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="68886-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="68886-117">*dwProviderType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-118">Valeur **DWORD** qui représente le type de fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="68886-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="68886-119">Pour plus d’informations, consultez [types de fournisseur de services de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="68886-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="68886-120">*pwszPvkFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-121">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom d’un fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="68886-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="68886-122">*pwszKeyContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68886-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-123">Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé privée.</span><span class="sxs-lookup"><span data-stu-id="68886-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="68886-124">*pdwKeySpec* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68886-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-125">Pointeur vers une valeur **DWORD** pour le type de clé du conteneur retourné avec *phCryptProv* et *ppwszTmpContainer*.</span><span class="sxs-lookup"><span data-stu-id="68886-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="68886-126">*ppwszTmpContainer* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="68886-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-127">Adresse d’un pointeur vers une chaîne se terminant par un caractère null pour le nom de conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="68886-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="68886-128">La fonction **PvkGetCryptProv** fournit et initialise le conteneur temporaire.</span><span class="sxs-lookup"><span data-stu-id="68886-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="68886-129">Lors de l’appel de **PvkGetCryptProv**, l’adresse doit pointer vers une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="68886-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="68886-130">*phCryptProv* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68886-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68886-131">Pointeur vers un handle pour le CSP.</span><span class="sxs-lookup"><span data-stu-id="68886-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68886-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68886-132">Return value</span></span>

<span data-ttu-id="68886-133">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="68886-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="68886-134">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="68886-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="68886-135">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="68886-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68886-136">Notes</span><span class="sxs-lookup"><span data-stu-id="68886-136">Remarks</span></span>

<span data-ttu-id="68886-137">La fonction **PvkGetCryptProv** tente d’abord d’accéder au handle du fournisseur à partir du nom du conteneur de clé spécifié par le paramètre *pwszKeyContainerName* .</span><span class="sxs-lookup"><span data-stu-id="68886-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="68886-138">Si vous transmettez la **valeur null** pour le paramètre *pwszKeyContainerName* , **PvkGetCryptProv** tente d’obtenir le fournisseur à partir du fichier de clé privée spécifié dans le paramètre *pwszPvkFile* .</span><span class="sxs-lookup"><span data-stu-id="68886-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="68886-139">Lorsque vous avez terminé d’utiliser le CSP, libérez le handle du fournisseur et le conteneur de clé temporaire en appelant la fonction [**PvkFreeCryptProv**](pvkfreecryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="68886-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68886-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68886-140">Requirements</span></span>



| <span data-ttu-id="68886-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68886-141">Requirement</span></span> | <span data-ttu-id="68886-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="68886-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68886-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68886-143">Minimum supported client</span></span><br/> | <span data-ttu-id="68886-144">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68886-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="68886-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68886-145">Minimum supported server</span></span><br/> | <span data-ttu-id="68886-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68886-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68886-147">DLL</span><span class="sxs-lookup"><span data-stu-id="68886-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68886-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68886-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
