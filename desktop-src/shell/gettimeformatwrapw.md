---
description: Met en forme l’heure sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973195"
---
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="91f3a-103">GetTimeFormatWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="91f3a-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="91f3a-104">\[**GetTimeFormatWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91f3a-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="91f3a-105">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="91f3a-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="91f3a-106">Vous devez utiliser [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="91f3a-107">Met en forme l’heure sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="91f3a-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="91f3a-108">La fonction met en forme une heure spécifiée ou l’heure système locale.</span><span class="sxs-lookup"><span data-stu-id="91f3a-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="91f3a-109">**GetTimeFormatWrapW** est un wrapper pour la fonction **GetTimeFormatW** .</span><span class="sxs-lookup"><span data-stu-id="91f3a-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="91f3a-110">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="91f3a-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91f3a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91f3a-111">Syntax</span></span>


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a><span data-ttu-id="91f3a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91f3a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f3a-113">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-114">Type : **LCID**</span><span class="sxs-lookup"><span data-stu-id="91f3a-114">Type: **LCID**</span></span>

<span data-ttu-id="91f3a-115">Spécifie les paramètres régionaux pour lesquels la chaîne d’heure doit être mise en forme.</span><span class="sxs-lookup"><span data-stu-id="91f3a-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="91f3a-116">Si *pwzFormat* a la **valeur null**, la fonction met en forme la chaîne en fonction du format d’heure de ces paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="91f3a-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="91f3a-117">Si *pwzFormat* n’a pas la **valeur null**, la fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format d’image (par exemple, les marqueurs d’heure de la région).</span><span class="sxs-lookup"><span data-stu-id="91f3a-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="91f3a-118">Ce paramètre peut être un identificateur de paramètres régionaux créé par la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , ou l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="91f3a-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="91f3a-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**paramètres régionaux \_ \_ par défaut du système**</span><span class="sxs-lookup"><span data-stu-id="91f3a-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-120">Paramètres régionaux par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="91f3a-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="91f3a-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**paramètres régionaux \_ par défaut de l’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="91f3a-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-122">Paramètres régionaux utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="91f3a-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91f3a-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-124">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="91f3a-124">Type: **DWORD**</span></span>

<span data-ttu-id="91f3a-125">Spécifie différentes options de fonction.</span><span class="sxs-lookup"><span data-stu-id="91f3a-125">Specifies various function options.</span></span> <span data-ttu-id="91f3a-126">Vous pouvez spécifier une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="91f3a-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="91f3a-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**paramètres régionaux \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="91f3a-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-128">Si cette option est définie, la fonction met en forme la chaîne en utilisant le format d’heure par défaut du système pour les paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="91f3a-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="91f3a-129">S’il n’est pas défini, la fonction met en forme la chaîne à l’aide de n’importe quel remplacement de l’utilisateur au format d’heure par défaut de la région.</span><span class="sxs-lookup"><span data-stu-id="91f3a-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="91f3a-130">Cet indicateur ne peut être défini que si *pwzFormat* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="91f3a-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="91f3a-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**paramètres régionaux \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="91f3a-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-132">Utilise la page de codes système ANSI pour la conversion de chaînes à la place de la page de codes des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="91f3a-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="91f3a-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TEMPS \_ NOMINUTESORSECONDS**</span><span class="sxs-lookup"><span data-stu-id="91f3a-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-134">N’utilise pas de minutes ou de secondes.</span><span class="sxs-lookup"><span data-stu-id="91f3a-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="91f3a-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**intervalle de temps (en \_ secondes)**</span><span class="sxs-lookup"><span data-stu-id="91f3a-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-136">N’utilise pas de secondes.</span><span class="sxs-lookup"><span data-stu-id="91f3a-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="91f3a-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TEMPS \_ NOTIMEMARKER**</span><span class="sxs-lookup"><span data-stu-id="91f3a-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-138">N’utilise pas de marqueur d’heure.</span><span class="sxs-lookup"><span data-stu-id="91f3a-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="91f3a-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TEMPS \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="91f3a-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="91f3a-140">Utilise toujours un format horaire de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="91f3a-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91f3a-141">*lpTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-142">Type : \**const [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="91f3a-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="91f3a-143">Pointeur vers une structure [_ *SystemTime* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) qui contient les informations d’heure à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="91f3a-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="91f3a-144">Si ce pointeur est **null**, la fonction utilise l’heure système locale actuelle.</span><span class="sxs-lookup"><span data-stu-id="91f3a-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="91f3a-145">*pwzFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-146">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="91f3a-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="91f3a-147">Pointeur vers un format à utiliser pour former la chaîne d’heure.</span><span class="sxs-lookup"><span data-stu-id="91f3a-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="91f3a-148">Si *pwzFormat* a la **valeur null**, la fonction utilise le format d’heure des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="91f3a-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="91f3a-149">Pour plus d’informations, consultez [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="91f3a-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="91f3a-150">*pwzTimeStr* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-151">Type : **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="91f3a-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="91f3a-152">Pointeur vers une mémoire tampon qui reçoit la chaîne d’heure mise en forme.</span><span class="sxs-lookup"><span data-stu-id="91f3a-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="91f3a-153">*cchTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f3a-154">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="91f3a-154">Type: **int**</span></span>

<span data-ttu-id="91f3a-155">Taille, en caractères, de la mémoire tampon *pwzTimeStr* .</span><span class="sxs-lookup"><span data-stu-id="91f3a-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="91f3a-156">Si *cchTime* est égal à zéro, la fonction retourne le nombre de caractères requis pour contenir la chaîne de temps mise en forme, et la mémoire tampon vers laquelle pointe *pwzTimeStr* n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="91f3a-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f3a-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91f3a-157">Return value</span></span>

<span data-ttu-id="91f3a-158">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="91f3a-158">Type: **int**</span></span>

<span data-ttu-id="91f3a-159">Si la fonction a abouti, la valeur de retour est le nombre de caractères écrits dans la mémoire tampon vers laquelle pointe *pwzTimeStr*.</span><span class="sxs-lookup"><span data-stu-id="91f3a-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="91f3a-160">Si le paramètre *cchTime* est égal à zéro, la valeur de retour est le nombre de caractères requis pour contenir la chaîne de temps mise en forme.</span><span class="sxs-lookup"><span data-stu-id="91f3a-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="91f3a-161">Le nombre comprend le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="91f3a-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="91f3a-162">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="91f3a-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="91f3a-163">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="91f3a-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="91f3a-164">**GetLastError** peut retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="91f3a-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="91f3a-165">**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="91f3a-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="91f3a-166">**indicateurs d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="91f3a-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="91f3a-167">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="91f3a-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="91f3a-168">Notes</span><span class="sxs-lookup"><span data-stu-id="91f3a-168">Remarks</span></span>

<span data-ttu-id="91f3a-169">**GetTimeFormatWrapW** offre la possibilité d’utiliser des chaînes Unicode dans des systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91f3a-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="91f3a-170">La méthode recommandée consiste à utiliser [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="91f3a-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="91f3a-171">**GetTimeFormatWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 310.</span><span class="sxs-lookup"><span data-stu-id="91f3a-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f3a-172">Spécifications</span><span class="sxs-lookup"><span data-stu-id="91f3a-172">Requirements</span></span>



| <span data-ttu-id="91f3a-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91f3a-173">Requirement</span></span> | <span data-ttu-id="91f3a-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="91f3a-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f3a-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f3a-175">Minimum supported client</span></span><br/> | <span data-ttu-id="91f3a-176">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91f3a-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f3a-177">Minimum supported server</span></span><br/> | <span data-ttu-id="91f3a-178">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f3a-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="91f3a-179">DLL</span><span class="sxs-lookup"><span data-stu-id="91f3a-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91f3a-180"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="91f3a-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f3a-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91f3a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f3a-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="91f3a-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
