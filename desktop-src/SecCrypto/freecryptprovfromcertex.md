---
description: 'Libère le descripteur d’un fournisseur de services de chiffrement (CSP) ou d’une clé Cryptography API : Next Generation (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867421"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="d2b6c-103">FreeCryptProvFromCertEx fonction)</span><span class="sxs-lookup"><span data-stu-id="d2b6c-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="d2b6c-104">La fonction **FreeCryptProvFromCertEx** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) ou d’une clé Cryptography API : Next Generation (CNG).</span><span class="sxs-lookup"><span data-stu-id="d2b6c-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="d2b6c-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="d2b6c-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d2b6c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2b6c-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="d2b6c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2b6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b6c-109">*fAcquired* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b6c-110">Valeur qui spécifie si le handle du fournisseur a été acquis à partir du [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2b6c-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2b6c-111">*hProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b6c-112">Handle vers un CSP CAPICOM ou un handle vers une clé CNG.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="d2b6c-113">*dwKeySpec*</span><span class="sxs-lookup"><span data-stu-id="d2b6c-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b6c-114">Adresse d’une variable **DWORD** qui reçoit des informations supplémentaires sur la clé.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="d2b6c-115">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-115">This can be one of the following values.</span></span>



| <span data-ttu-id="d2b6c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2b6c-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="d2b6c-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d2b6c-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="d2b6c-118"><dt>**au niveau de \_ KEYexchange**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b6c-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="d2b6c-119">La paire de clés est une paire d’échange de clés.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="d2b6c-120"><dt>**à la \_ signature**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b6c-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="d2b6c-121">La paire de clés est une paire de signatures.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="d2b6c-122"><dt>**spécification de clé de certificat \_ NCRYPT \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b6c-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="d2b6c-123">La clé est une clé CNG.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="d2b6c-124">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2b6c-125">*pwszCapiProvider* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b6c-126">Pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="d2b6c-127">*dwProviderType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b6c-128">Spécifie le type de fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-128">Specifies the CSP type.</span></span> <span data-ttu-id="d2b6c-129">Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="d2b6c-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="d2b6c-130">Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="d2b6c-131">*pwszTmpContainer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b6c-132">Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b6c-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2b6c-133">Return value</span></span>

<span data-ttu-id="d2b6c-134">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d2b6c-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b6c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2b6c-135">Requirements</span></span>



| <span data-ttu-id="d2b6c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2b6c-136">Requirement</span></span> | <span data-ttu-id="d2b6c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2b6c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b6c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b6c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b6c-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d2b6c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b6c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b6c-141">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2b6c-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d2b6c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d2b6c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2b6c-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2b6c-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
