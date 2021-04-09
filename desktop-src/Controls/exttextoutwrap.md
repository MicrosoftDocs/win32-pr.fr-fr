---
title: ExtTextOutWrap fonction)
description: Dessine le texte à l’aide de la police, de la couleur d’arrière-plan et de la couleur de texte actuellement sélectionnées. Vous pouvez éventuellement fournir des dimensions à utiliser pour le découpage, l’opacité ou les deux. Cette fonction encapsule un appel à ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Contrôles Windows de la fonction ExtTextOutWrap
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102977"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="1c3f6-106">ExtTextOutWrap fonction)</span><span class="sxs-lookup"><span data-stu-id="1c3f6-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="1c3f6-107">\[**ExtTextOutWrap** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="1c3f6-108">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1c3f6-109">Nous vous recommandons d’utiliser [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directement à la place.\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="1c3f6-110">Dessine le texte à l’aide de la police, de la couleur d’arrière-plan et de la couleur de texte actuellement sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="1c3f6-111">Vous pouvez éventuellement fournir des dimensions à utiliser pour le découpage, l’opacité ou les deux.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="1c3f6-112">Cette fonction encapsule un appel à [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c3f6-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c3f6-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="1c3f6-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c3f6-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c3f6-115">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-116">Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c3f6-117">Handle vers le contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-118">*X* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-119">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-119">Type: **int**</span></span>

<span data-ttu-id="1c3f6-120">Coordonnée x, en coordonnées logiques, du point de référence utilisé pour positionner la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-121">*Y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-122">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-122">Type: **int**</span></span>

<span data-ttu-id="1c3f6-123">Coordonnée y, en coordonnées logiques, du point de référence utilisé pour positionner la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-124">*uOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-125">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c3f6-126">Valeurs qui spécifient comment utiliser le rectangle défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="1c3f6-127">Pour obtenir la liste complète des options, consultez [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .</span><span class="sxs-lookup"><span data-stu-id="1c3f6-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-128">*LPRC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-129">Type : \**const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="1c3f6-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="1c3f6-130">Pointeur vers une structure [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) facultative qui spécifie les dimensions, en coordonnées logiques, d’un rectangle utilisé pour le découpage, l’opacité ou les deux.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-131">*lpString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-132">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c3f6-133">Pointeur vers une mémoire tampon qui contient le texte à dessiner.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="1c3f6-134">Il n’est pas nécessaire que la chaîne se termine par zéro, car *cbCount* spécifie la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-135">*cbCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-136">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c3f6-137">Longueur de la chaîne, en octets, vers laquelle pointe *lpString*.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="1c3f6-138">*lpDx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3f6-139">Type : \**const [**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="1c3f6-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="1c3f6-140">Pointeur vers un tableau facultatif de valeurs qui indiquent la distance entre les origines des cellules de caractères adjacentes.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="1c3f6-141">Par exemple, \[ \] les unités logiques _lpDx \* x séparent les origines de la cellule de caractère x et de la cellule de caractère (x + 1).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c3f6-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c3f6-142">Return value</span></span>

<span data-ttu-id="1c3f6-143">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1c3f6-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1c3f6-144">Retourne une valeur différente de zéro si la chaîne est dessinée correctement.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="1c3f6-145">Toutefois, si la version ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) est appelée avec l' \_ index de glyphes ETO \_ , la fonction retourne la **valeur true** même si la fonction ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="1c3f6-146">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="1c3f6-147">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c3f6-148">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c3f6-148">Remarks</span></span>

<span data-ttu-id="1c3f6-149">**ExtTextOutWrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="1c3f6-150">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 417 de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="1c3f6-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="1c3f6-151">Pour des remarques supplémentaires, consultez [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="1c3f6-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c3f6-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c3f6-152">Requirements</span></span>



| <span data-ttu-id="1c3f6-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c3f6-153">Requirement</span></span> | <span data-ttu-id="1c3f6-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c3f6-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c3f6-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c3f6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="1c3f6-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="1c3f6-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c3f6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="1c3f6-158">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c3f6-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c3f6-159">DLL</span><span class="sxs-lookup"><span data-stu-id="1c3f6-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c3f6-160"><dt>Comctl32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1c3f6-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

