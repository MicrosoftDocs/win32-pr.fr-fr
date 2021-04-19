---
description: Libère le descripteur d’un fournisseur de services de chiffrement (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530224"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="fa32a-103">PvkFreeCryptProv fonction)</span><span class="sxs-lookup"><span data-stu-id="fa32a-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa32a-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fa32a-104">This API is deprecated.</span></span> <span data-ttu-id="fa32a-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fa32a-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="fa32a-106">La fonction **PvkFreeCryptProv** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction [**PvkGetCryptProv**](pvkgetcryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="fa32a-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="fa32a-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="fa32a-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="fa32a-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="fa32a-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fa32a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa32a-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="fa32a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa32a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa32a-111">*hProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa32a-112">Handle du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fa32a-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="fa32a-113">*pwszCapiProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa32a-114">Pointeur vers une chaîne se terminant par null pour le nom du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fa32a-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="fa32a-115">*dwProviderType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa32a-116">Valeur **DWORD** qui représente le type de fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fa32a-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="fa32a-117">Pour plus d’informations, consultez [types de fournisseur de services de chiffrement](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="fa32a-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa32a-118">*pwszTmpContainer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa32a-119">Pointeur vers une chaîne se terminant par null pour le nom de conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="fa32a-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa32a-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa32a-120">Return value</span></span>

<span data-ttu-id="fa32a-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fa32a-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa32a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa32a-122">Requirements</span></span>



| <span data-ttu-id="fa32a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa32a-123">Requirement</span></span> | <span data-ttu-id="fa32a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa32a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa32a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa32a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa32a-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fa32a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa32a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa32a-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa32a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa32a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fa32a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa32a-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa32a-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
