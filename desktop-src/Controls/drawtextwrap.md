---
title: DrawTextWrap fonction)
description: Dessine du texte mis en forme dans le rectangle spécifié. Il met en forme le texte en fonction de la méthode spécifiée (en développant les onglets, en justifiant les caractères, les sauts de ligne, etc.). Cette fonction encapsule un appel à DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Contrôles Windows de la fonction DrawTextWrap
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941719"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="413f8-106">DrawTextWrap fonction)</span><span class="sxs-lookup"><span data-stu-id="413f8-106">DrawTextWrap function</span></span>

<span data-ttu-id="413f8-107">\[**DrawTextWrap** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="413f8-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="413f8-108">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="413f8-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="413f8-109">Il est recommandé d’utiliser [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directement à la place.\]</span><span class="sxs-lookup"><span data-stu-id="413f8-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="413f8-110">Dessine du texte mis en forme dans le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="413f8-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="413f8-111">Il met en forme le texte en fonction de la méthode spécifiée (en développant les onglets, en justifiant les caractères, les sauts de ligne, etc.).</span><span class="sxs-lookup"><span data-stu-id="413f8-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="413f8-112">Cette fonction encapsule un appel à [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="413f8-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="413f8-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="413f8-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="413f8-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="413f8-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413f8-115">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="413f8-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-116">Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="413f8-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="413f8-117">Handle vers le contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="413f8-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="413f8-118">*lpString* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="413f8-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-119">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="413f8-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="413f8-120">Pointeur vers une mémoire tampon qui contient le texte à dessiner.</span><span class="sxs-lookup"><span data-stu-id="413f8-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="413f8-121">Si le paramètre *nCount* a la valeur-1, la chaîne doit se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="413f8-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="413f8-122">Si *uFormat* comprend DT \_ MODIFYSTRING, la fonction peut ajouter jusqu’à quatre caractères supplémentaires à cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="413f8-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="413f8-123">La mémoire tampon qui contient la chaîne doit être suffisamment grande pour prendre en charge ces caractères supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="413f8-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="413f8-124">*nCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="413f8-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-125">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="413f8-125">Type: **int**</span></span>

<span data-ttu-id="413f8-126">Longueur de la chaîne vers laquelle pointe *lpString*.</span><span class="sxs-lookup"><span data-stu-id="413f8-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="413f8-127">Si *nCount* a la valeur-1, le paramètre *lpString* est supposé être un pointeur vers une chaîne terminée par le caractère null et [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcule automatiquement le nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="413f8-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="413f8-128">*lpRect* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="413f8-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-129">Type : **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="413f8-129">Type: **LPRECT**</span></span>

<span data-ttu-id="413f8-130">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.</span><span class="sxs-lookup"><span data-stu-id="413f8-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="413f8-131">*uFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="413f8-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-132">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="413f8-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="413f8-133">Options de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="413f8-133">The formatting options.</span></span> <span data-ttu-id="413f8-134">Pour obtenir la liste complète des options, consultez la documentation de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="413f8-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="413f8-135">*lpDTParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="413f8-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413f8-136">Type : **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="413f8-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="413f8-137">Pointeur vers une structure [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) qui spécifie des options de mise en forme supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="413f8-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="413f8-138">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="413f8-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413f8-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="413f8-139">Return value</span></span>

<span data-ttu-id="413f8-140">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="413f8-140">Type: **int**</span></span>

<span data-ttu-id="413f8-141">Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="413f8-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="413f8-142">Si **DT \_ VCENTER** ou **DT \_ Bottom** est spécifié, la valeur de retour est le décalage par rapport au membre **supérieur** de *LPRC* au bas du texte dessiné si la fonction échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="413f8-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="413f8-143">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="413f8-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="413f8-144">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="413f8-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="413f8-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="413f8-145">Remarks</span></span>

<span data-ttu-id="413f8-146">**DrawTextWrap** n’est pas exporté par nom ou déclaré dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="413f8-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="413f8-147">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 415 de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="413f8-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="413f8-148">Pour des remarques supplémentaires, consultez [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="413f8-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="413f8-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="413f8-149">Requirements</span></span>



| <span data-ttu-id="413f8-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="413f8-150">Requirement</span></span> | <span data-ttu-id="413f8-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="413f8-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="413f8-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="413f8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="413f8-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="413f8-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="413f8-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="413f8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="413f8-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="413f8-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="413f8-156">DLL</span><span class="sxs-lookup"><span data-stu-id="413f8-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="413f8-157"><dt>Comctl32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="413f8-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

