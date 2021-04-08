---
title: GetTextExtentPoint32Wrap fonction)
description: Calcule la largeur et la hauteur de la chaîne de texte spécifiée. Cette fonction encapsule un appel à GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Contrôles Windows de la fonction GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740109"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="0d125-105">GetTextExtentPoint32Wrap fonction)</span><span class="sxs-lookup"><span data-stu-id="0d125-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="0d125-106">\[**GetTextExtentPoint32Wrap** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="0d125-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="0d125-107">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0d125-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0d125-108">Nous vous recommandons d’utiliser [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directement à la place.\]</span><span class="sxs-lookup"><span data-stu-id="0d125-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="0d125-109">Calcule la largeur et la hauteur de la chaîne de texte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0d125-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="0d125-110">Cette fonction encapsule un appel à [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="0d125-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d125-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d125-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="0d125-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d125-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d125-113">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d125-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d125-114">Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d125-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d125-115">Handle vers le contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="0d125-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="0d125-116">*lpString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d125-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d125-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d125-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d125-118">Pointeur vers une mémoire tampon qui contient le texte à dessiner.</span><span class="sxs-lookup"><span data-stu-id="0d125-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="0d125-119">Il n’est pas nécessaire que la chaîne se termine par zéro, car *cbCount* spécifie la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0d125-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="0d125-120">*cbCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d125-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d125-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d125-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d125-122">Longueur, en octets, de la chaîne vers laquelle pointe *lpString*.</span><span class="sxs-lookup"><span data-stu-id="0d125-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="0d125-123">*lpSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d125-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d125-124">Type : **LPSIZE**</span><span class="sxs-lookup"><span data-stu-id="0d125-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="0d125-125">Lorsque cette méthode est retournée, contient un pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) contenant les dimensions de la chaîne, en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="0d125-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d125-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d125-126">Return value</span></span>

<span data-ttu-id="0d125-127">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d125-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d125-128">Retourne une valeur différente de zéro en cas de réussite ; Sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="0d125-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="0d125-129">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0d125-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d125-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d125-130">Remarks</span></span>

<span data-ttu-id="0d125-131">**GetTextExtentPoint32Wrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="0d125-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="0d125-132">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 420 de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="0d125-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="0d125-133">Pour des remarques supplémentaires, consultez [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="0d125-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d125-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d125-134">Requirements</span></span>



| <span data-ttu-id="0d125-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d125-135">Requirement</span></span> | <span data-ttu-id="0d125-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d125-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d125-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d125-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0d125-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d125-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="0d125-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d125-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0d125-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d125-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0d125-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0d125-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d125-142"><dt>Comctl32.dll (version 5,81 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="0d125-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

