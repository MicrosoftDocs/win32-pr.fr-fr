---
title: Str_GetPtr fonction)
description: Copie une chaîne d’une mémoire tampon vers une autre.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Contrôles Windows de la fonction Str_GetPtr
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740509"
---
# <a name="str_getptr-function"></a><span data-ttu-id="9d9cf-104">\_Fonction Str GetPtr</span><span class="sxs-lookup"><span data-stu-id="9d9cf-104">Str\_GetPtr function</span></span>

<span data-ttu-id="9d9cf-105">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="9d9cf-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9d9cf-107">Copie une chaîne d’une mémoire tampon vers une autre.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d9cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d9cf-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="9d9cf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d9cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9cf-110">*pszSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9cf-111">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d9cf-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d9cf-112">Pointeur vers une chaîne source.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="9d9cf-113">*pszDest* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9cf-114">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d9cf-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d9cf-115">Pointeur vers la mémoire tampon de destination.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="9d9cf-116">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9d9cf-117">*cchDest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9cf-118">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="9d9cf-118">Type: **int**</span></span>

<span data-ttu-id="9d9cf-119">Taille de *pszDest*, en caractères.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9cf-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d9cf-120">Return value</span></span>

<span data-ttu-id="9d9cf-121">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="9d9cf-121">Type: **int**</span></span>

<span data-ttu-id="9d9cf-122">Si *pszDest* a la **valeur null** ou si *cchDest* est égal à zéro, retourne la taille de la mémoire tampon, en caractères, nécessaire pour contenir une copie terminée par un caractère null de la chaîne pointée par *pszSource*.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="9d9cf-123">Si *pszDest* n’a pas la **valeur null**, retourne le nombre de caractères copiés avec succès, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="9d9cf-124">Si *pszDest* ne peut pas contenir la totalité de la chaîne pointée par *PszSource*, (*cchDest*-1) caractères sont copiés, la chaîne se termine par null et *cchDest* retournée.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d9cf-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9d9cf-125">Remarks</span></span>

<span data-ttu-id="9d9cf-126">**Chaîne \_ GetPtr** est disponible en tant que versions ANSI (**Str \_ GetPtrA**) et Unicode (**Str \_ GetPtrW**).</span><span class="sxs-lookup"><span data-stu-id="9d9cf-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="9d9cf-127">Ces fonctions ne sont pas exportées par nom ou déclarées dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="9d9cf-128">Pour les utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et la requête ordinale 233 (**Str \_ GetPtrA**) ou 235 (**str \_ GetPtrW**) à partir de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9cf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d9cf-129">Requirements</span></span>



| <span data-ttu-id="9d9cf-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d9cf-130">Requirement</span></span> | <span data-ttu-id="9d9cf-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d9cf-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9cf-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9cf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9cf-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9d9cf-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9cf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9cf-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9cf-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d9cf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9d9cf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d9cf-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d9cf-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d9cf-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9d9cf-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d9cf-139">**Chaîne \_ GetPtrW** (Unicode) et **Str \_ GetPtrA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d9cf-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

