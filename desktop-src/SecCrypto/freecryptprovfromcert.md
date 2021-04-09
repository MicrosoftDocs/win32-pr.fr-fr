---
description: Libère le descripteur d’un fournisseur de services de chiffrement (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867422"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="03760-103">FreeCryptProvFromCert fonction)</span><span class="sxs-lookup"><span data-stu-id="03760-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03760-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="03760-104">This API is deprecated.</span></span> <span data-ttu-id="03760-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="03760-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="03760-106">La fonction **FreeCryptProvFromCert** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction [**GetCryptProvFromCert**](getcryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="03760-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="03760-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="03760-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="03760-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="03760-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="03760-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03760-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="03760-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03760-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03760-111">*fAcquired* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="03760-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03760-112">Valeur qui spécifie si le handle du fournisseur a été acquis à partir du [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="03760-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="03760-113">*hProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="03760-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03760-114">Pointeur vers une structure [**HCRYPTPROV**](hcryptprov.md) pour le fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="03760-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="03760-115">*pwszCapiProvider* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="03760-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03760-116">Pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="03760-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="03760-117">*dwProviderType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="03760-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03760-118">Spécifie le type de fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="03760-118">Specifies the CSP type.</span></span> <span data-ttu-id="03760-119">Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="03760-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="03760-120">Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.</span><span class="sxs-lookup"><span data-stu-id="03760-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="03760-121">*pwszTmpContainer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="03760-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03760-122">Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="03760-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03760-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03760-123">Return value</span></span>

<span data-ttu-id="03760-124">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03760-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03760-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03760-125">Requirements</span></span>



| <span data-ttu-id="03760-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03760-126">Requirement</span></span> | <span data-ttu-id="03760-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="03760-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03760-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03760-128">Minimum supported client</span></span><br/> | <span data-ttu-id="03760-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03760-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03760-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03760-130">Minimum supported server</span></span><br/> | <span data-ttu-id="03760-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03760-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03760-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03760-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03760-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03760-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
