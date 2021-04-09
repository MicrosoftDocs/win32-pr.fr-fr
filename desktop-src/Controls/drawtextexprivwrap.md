---
title: DrawTextExPrivWrap fonction)
description: Dessine du texte mis en forme dans le rectangle spécifié. Cette fonction encapsule un appel à DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Contrôles Windows de la fonction DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942849"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="8ae3e-105">DrawTextExPrivWrap fonction)</span><span class="sxs-lookup"><span data-stu-id="8ae3e-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="8ae3e-106">\[**DrawTextExPrivWrap** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="8ae3e-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="8ae3e-107">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8ae3e-108">Nous vous recommandons d’utiliser [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directement à la place.\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="8ae3e-109">Dessine du texte mis en forme dans le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="8ae3e-110">Cette fonction encapsule un appel à [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="8ae3e-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae3e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ae3e-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="8ae3e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ae3e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae3e-113">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-114">Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ae3e-115">Handle vers le contexte de périphérique dans lequel dessiner.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="8ae3e-116">*lpchText* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-117">Type : **[ **LPTStr**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ae3e-118">Pointeur vers une mémoire tampon qui contient le texte à dessiner.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="8ae3e-119">Si le paramètre *cchText* a la valeur-1, la chaîne doit se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="8ae3e-120">Si *dwDTFormat* comprend DT \_ MODIFYSTRING, la fonction peut ajouter jusqu’à quatre caractères supplémentaires à cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="8ae3e-121">La mémoire tampon qui contient la chaîne doit être suffisamment grande pour prendre en charge ces caractères supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="8ae3e-122">*cchText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-123">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-123">Type: **int**</span></span>

<span data-ttu-id="8ae3e-124">Longueur de la chaîne vers laquelle pointe *lpchText*.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="8ae3e-125">Si *cchText* a la valeur-1, le paramètre *lpchText* est supposé être un pointeur vers une chaîne se terminant par le caractère null et [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcule le nombre de caractères automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="8ae3e-126">*LPRC* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-127">Type : **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-127">Type: **LPRECT**</span></span>

<span data-ttu-id="8ae3e-128">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="8ae3e-129">*dwDTFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-130">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ae3e-131">Options de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-131">The formatting options.</span></span> <span data-ttu-id="8ae3e-132">Pour obtenir la liste complète des options, consultez la documentation de [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .</span><span class="sxs-lookup"><span data-stu-id="8ae3e-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="8ae3e-133">*lpDTParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae3e-134">Type : **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="8ae3e-135">Pointeur vers une structure [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) qui spécifie des options de mise en forme supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="8ae3e-136">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae3e-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ae3e-137">Return value</span></span>

<span data-ttu-id="8ae3e-138">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="8ae3e-138">Type: **int**</span></span>

<span data-ttu-id="8ae3e-139">Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="8ae3e-140">Si **DT \_ VCENTER** ou **DT \_ Bottom** est spécifié, la valeur de retour est le décalage par rapport au membre **supérieur** de *LPRC* au bas du texte dessiné.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="8ae3e-141">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="8ae3e-142">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8ae3e-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae3e-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ae3e-143">Remarks</span></span>

<span data-ttu-id="8ae3e-144">**DrawTextExPrivWrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="8ae3e-145">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 416 de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="8ae3e-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="8ae3e-146">Pour des remarques supplémentaires, consultez [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="8ae3e-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae3e-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ae3e-147">Requirements</span></span>



| <span data-ttu-id="8ae3e-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ae3e-148">Requirement</span></span> | <span data-ttu-id="8ae3e-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ae3e-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae3e-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae3e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae3e-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="8ae3e-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae3e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae3e-153">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ae3e-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ae3e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8ae3e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ae3e-155"><dt>Comctl32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3e-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

