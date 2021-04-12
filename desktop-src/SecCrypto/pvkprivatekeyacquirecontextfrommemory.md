---
description: Crée un conteneur temporaire dans le fournisseur de services de chiffrement (CSP) et charge une clé privée à partir de la mémoire dans le conteneur.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320370"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="bdadc-103">PvkPrivateKeyAcquireContextFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="bdadc-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bdadc-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bdadc-104">This API is deprecated.</span></span> <span data-ttu-id="bdadc-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bdadc-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="bdadc-106">La fonction **PvkPrivateKeyAcquireContextFromMemory** crée un conteneur temporaire dans le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et charge une [*clé privée*](../secgloss/p-gly.md) à partir de la mémoire dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="bdadc-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="bdadc-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="bdadc-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="bdadc-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="bdadc-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bdadc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdadc-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="bdadc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdadc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdadc-111">*pwszProvName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du fournisseur de services de chiffrement dont le type est demandé dans *dwProvType*.</span><span class="sxs-lookup"><span data-stu-id="bdadc-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-113">*dwProvType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-114">Valeur **DWORD** pour le type CSP.</span><span class="sxs-lookup"><span data-stu-id="bdadc-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="bdadc-115">Pour plus d’informations sur les types CSP, consultez [types de fournisseur de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="bdadc-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-116">*pbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-117">Pointeur vers une mémoire tampon destinée à recevoir les données de contexte.</span><span class="sxs-lookup"><span data-stu-id="bdadc-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="bdadc-118">L’appelant doit fournir cette ressource.</span><span class="sxs-lookup"><span data-stu-id="bdadc-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-119">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-120">Valeur **DWORD** qui spécifie la taille, en octets, de la mémoire tampon *pbData* .</span><span class="sxs-lookup"><span data-stu-id="bdadc-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="bdadc-121">L’appelant doit fournir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="bdadc-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-122">*hwndOwner* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-123">Si un mot de passe est requis pour déchiffrer les données de contexte pointées par le paramètre *pbData* , ce paramètre est un handle vers le parent de la boîte de dialogue ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="bdadc-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-124">*pwszKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-125">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de la clé à récupérer.</span><span class="sxs-lookup"><span data-stu-id="bdadc-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-126">*pdwKeySpec* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-127">Pointeur vers une valeur **DWORD** qui spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="bdadc-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="bdadc-128">Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.</span><span class="sxs-lookup"><span data-stu-id="bdadc-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-129">*phCryptProv* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-130">Pointeur vers un handle pour le CSP.</span><span class="sxs-lookup"><span data-stu-id="bdadc-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="bdadc-131">*ppwszTmpContainer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadc-132">Adresse d’un pointeur vers une chaîne se terminant par null pour le nom de conteneur temporaire.</span><span class="sxs-lookup"><span data-stu-id="bdadc-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="bdadc-133">La fonction **PvkPrivateKeyAcquireContextFromMemory** fournit la mémoire tampon pour cette chaîne et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="bdadc-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="bdadc-134">Lors de l’appel de **PvkPrivateKeyAcquireContextFromMemory**, l’adresse doit pointer vers une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="bdadc-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdadc-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdadc-135">Return value</span></span>

<span data-ttu-id="bdadc-136">En cas de réussite, cette fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="bdadc-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="bdadc-137">La fonction **PvkPrivateKeyAcquireContextFromMemory** retourne la **valeur false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="bdadc-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdadc-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdadc-138">Requirements</span></span>



| <span data-ttu-id="bdadc-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdadc-139">Requirement</span></span> | <span data-ttu-id="bdadc-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdadc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdadc-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdadc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bdadc-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bdadc-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdadc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bdadc-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdadc-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bdadc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bdadc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdadc-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdadc-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
