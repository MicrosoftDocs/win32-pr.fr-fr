---
description: Utilisé par un fournisseur de services de chiffrement (CSP) pour vérifier la signature d’une DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE pointeur de fonction (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521208"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="cfb00-103">Chiffrer le \_ pointeur de fonction d’image de vérification \_</span><span class="sxs-lookup"><span data-stu-id="cfb00-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="cfb00-104">La fonction de rappel **FuncVerifyImage** est utilisée par un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour vérifier la signature d’une dll.</span><span class="sxs-lookup"><span data-stu-id="cfb00-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="cfb00-105">Toutes les dll auxiliaires dans lesquelles un CSP effectue des appels de fonction doivent être signées de la même manière (et avec la même clé) que la DLL CSP principale.</span><span class="sxs-lookup"><span data-stu-id="cfb00-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="cfb00-106">Pour garantir cette signature, les dll auxiliaires doivent être chargées de manière dynamique à l’aide de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="cfb00-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="cfb00-107">Mais avant le chargement de la DLL, la signature de la DLL doit être vérifiée.</span><span class="sxs-lookup"><span data-stu-id="cfb00-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="cfb00-108">Le fournisseur CSP effectue cette vérification en appelant la fonction **FuncVerifyImage** , comme illustré dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cfb00-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb00-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfb00-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="cfb00-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfb00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb00-111">*lpszImage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfb00-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb00-112">Adresse d’une chaîne terminée par le caractère null qui contient le chemin d’accès et le nom de fichier de la DLL pour laquelle vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="cfb00-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="cfb00-113">*pbSigData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfb00-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb00-114">Adresse d’une mémoire tampon qui contient la signature.</span><span class="sxs-lookup"><span data-stu-id="cfb00-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb00-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfb00-115">Return value</span></span>

<span data-ttu-id="cfb00-116">Retourne la **valeur true** si la fonction réussit, **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="cfb00-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="cfb00-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="cfb00-117">Examples</span></span>

<span data-ttu-id="cfb00-118">L’exemple suivant montre comment utiliser la fonction de rappel **FuncVerifyImage** pour vérifier la signature d’une dll avant qu’elle ne soit chargée par un CSP.</span><span class="sxs-lookup"><span data-stu-id="cfb00-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="cfb00-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfb00-119">Requirements</span></span>



| <span data-ttu-id="cfb00-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfb00-120">Requirement</span></span> | <span data-ttu-id="cfb00-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfb00-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb00-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfb00-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb00-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfb00-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfb00-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfb00-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb00-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfb00-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cfb00-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfb00-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb00-127"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb00-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb00-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb00-129">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="cfb00-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="cfb00-130">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="cfb00-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
