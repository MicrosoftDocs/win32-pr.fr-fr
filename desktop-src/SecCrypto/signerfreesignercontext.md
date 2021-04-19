---
description: Libère une structure de contexte de signataire \_ allouée par un appel précédent à la fonction SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526155"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="a7eeb-103">SignerFreeSignerContext fonction)</span><span class="sxs-lookup"><span data-stu-id="a7eeb-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="a7eeb-104">La fonction **SignerFreeSignerContext** libère une structure de [**\_ contexte de signataire**](signer-context.md) allouée par un appel précédent à la fonction [**SignerSignEx**](signersignex.md) .</span><span class="sxs-lookup"><span data-stu-id="a7eeb-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="a7eeb-105">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="a7eeb-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="a7eeb-106">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="a7eeb-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a7eeb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7eeb-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="a7eeb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7eeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7eeb-109">*pSignerContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7eeb-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7eeb-110">Pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) à libérer.</span><span class="sxs-lookup"><span data-stu-id="a7eeb-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7eeb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7eeb-111">Return value</span></span>

<span data-ttu-id="a7eeb-112">Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7eeb-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="a7eeb-113">Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a7eeb-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="a7eeb-114">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="a7eeb-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7eeb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7eeb-115">Requirements</span></span>



| <span data-ttu-id="a7eeb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7eeb-116">Requirement</span></span> | <span data-ttu-id="a7eeb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7eeb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7eeb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7eeb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7eeb-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7eeb-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7eeb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7eeb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7eeb-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7eeb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7eeb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a7eeb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7eeb-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7eeb-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7eeb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7eeb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7eeb-125">**contexte du signataire \_**</span><span class="sxs-lookup"><span data-stu-id="a7eeb-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="a7eeb-126">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="a7eeb-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
