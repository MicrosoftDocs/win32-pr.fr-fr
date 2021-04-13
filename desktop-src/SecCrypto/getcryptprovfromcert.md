---
description: Obtient un handle vers un fournisseur de services de chiffrement (CSP) et une spécification de clé pour un contexte de certificat.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321026"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="f967f-103">GetCryptProvFromCert fonction)</span><span class="sxs-lookup"><span data-stu-id="f967f-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f967f-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f967f-104">This API is deprecated.</span></span> <span data-ttu-id="f967f-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f967f-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="f967f-106">La fonction **GetCryptProvFromCert** obtient un descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et une spécification de clé pour un contexte de [*certificat*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f967f-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="f967f-107">Utilisez cette fonction pour accéder à la [*clé privée*](../secgloss/p-gly.md) de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="f967f-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="f967f-108">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="f967f-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="f967f-109">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="f967f-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f967f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f967f-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="f967f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f967f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f967f-112">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f967f-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-113">Handle de la fenêtre à utiliser comme propriétaire de toutes les boîtes de dialogue affichées.</span><span class="sxs-lookup"><span data-stu-id="f967f-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="f967f-114">Ce membre n’est pas actuellement utilisé et est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f967f-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="f967f-115">Il est possible de passer la **valeur null** pour ce paramètre en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="f967f-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-116">*pCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f967f-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-117">Pointeur vers une structure [**de \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="f967f-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-118">*phCryptProv* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f967f-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-119">Pointeur vers une structure [**HCRYPTPROV**](hcryptprov.md) qui est un handle pour le fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f967f-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-120">*pdwKeySpec* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f967f-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-121">Spécification de la clé privée à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f967f-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="f967f-122">Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.</span><span class="sxs-lookup"><span data-stu-id="f967f-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-123">*pfDidCryptAcquire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f967f-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-124">Valeur qui spécifie si la fonction A acquis le handle de fournisseur en fonction du certificat.</span><span class="sxs-lookup"><span data-stu-id="f967f-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-125">*ppwszTmpContainer* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f967f-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-126">Adresse d’un pointeur vers une chaîne se terminant par un caractère null pour le nom de conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="f967f-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="f967f-127">La fonction **GetCryptProvFromCert** fournit et initialise le conteneur temporaire.</span><span class="sxs-lookup"><span data-stu-id="f967f-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="f967f-128">Lors de l’appel de **GetCryptProvFromCert**, l’adresse doit pointer vers une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f967f-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-129">*ppwszProviderName* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f967f-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-130">Adresse d’un pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f967f-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="f967f-131">La fonction **GetCryptProvFromCert** retourne le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f967f-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="f967f-132">Lors de l’appel de **GetCryptProvFromCert**, l’adresse doit pointer vers une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f967f-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="f967f-133">*pdwProviderType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f967f-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f967f-134">Spécifie le type de fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f967f-134">Specifies the CSP type.</span></span> <span data-ttu-id="f967f-135">Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="f967f-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="f967f-136">Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.</span><span class="sxs-lookup"><span data-stu-id="f967f-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f967f-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f967f-137">Return value</span></span>

<span data-ttu-id="f967f-138">En cas de réussite, cette fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="f967f-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="f967f-139">La fonction **GetCryptProvFromCert** retourne la **valeur false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f967f-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="f967f-140">Notes</span><span class="sxs-lookup"><span data-stu-id="f967f-140">Remarks</span></span>

<span data-ttu-id="f967f-141">L’outil [Makecert](makecert.md) appelle **GetCryptProvFromCert** quand vous l’appelez à l’aide de l’option **de ligne de commande-is** .</span><span class="sxs-lookup"><span data-stu-id="f967f-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="f967f-142">Si le paramètre *pfDidCryptAcquire* a la valeur **true**, la fonction définit les paramètres *phCryptProv*, *pdwKeySpec* et *pdwProviderType* sur les valeurs du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f967f-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="f967f-143">Lorsque vous avez terminé d’utiliser le fournisseur de services de chiffrement, libérez-le en appelant la fonction [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="f967f-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f967f-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f967f-144">Requirements</span></span>



| <span data-ttu-id="f967f-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f967f-145">Requirement</span></span> | <span data-ttu-id="f967f-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="f967f-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f967f-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f967f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f967f-148">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f967f-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f967f-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f967f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f967f-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f967f-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f967f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f967f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f967f-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f967f-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
