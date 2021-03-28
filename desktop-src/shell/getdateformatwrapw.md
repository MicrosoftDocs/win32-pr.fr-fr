---
description: Met en forme une date sous forme de chaîne de date pour les paramètres régionaux spécifiés.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202786"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="afc0d-103">GetDateFormatWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="afc0d-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="afc0d-104">\[**GetDateFormatWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afc0d-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="afc0d-105">Elle ne sera pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="afc0d-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="afc0d-106">Vous devez utiliser [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="afc0d-107">Met en forme une date sous forme de chaîne de date pour les paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="afc0d-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="afc0d-108">La fonction met en forme une date spécifiée ou la date du système local.</span><span class="sxs-lookup"><span data-stu-id="afc0d-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="afc0d-109">**GetDateFormatWrapW** est un wrapper pour la fonction **GetDateFormatW** .</span><span class="sxs-lookup"><span data-stu-id="afc0d-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="afc0d-110">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="afc0d-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="afc0d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afc0d-111">Syntax</span></span>


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="afc0d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afc0d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc0d-113">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-114">Type : **LCID**</span><span class="sxs-lookup"><span data-stu-id="afc0d-114">Type: **LCID**</span></span>

<span data-ttu-id="afc0d-115">Paramètres régionaux pour lesquels la chaîne de date doit être mise en forme.</span><span class="sxs-lookup"><span data-stu-id="afc0d-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="afc0d-116">Si *pwzFormat* a la **valeur null**, la fonction met en forme la chaîne en fonction du format de date de ces paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="afc0d-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="afc0d-117">Si *pwzFormat* n’a pas la **valeur null**, la fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format d’image (par exemple, les noms de jours et de mois des paramètres régionaux).</span><span class="sxs-lookup"><span data-stu-id="afc0d-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="afc0d-118">Ce paramètre peut être un identificateur de paramètres régionaux créé par la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , ou l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="afc0d-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="afc0d-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**paramètres régionaux \_ \_ par défaut du système**</span><span class="sxs-lookup"><span data-stu-id="afc0d-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-120">Paramètres régionaux par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="afc0d-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="afc0d-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**paramètres régionaux \_ par défaut de l’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="afc0d-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-122">Paramètres régionaux utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="afc0d-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="afc0d-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-124">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="afc0d-124">Type: **DWORD**</span></span>

<span data-ttu-id="afc0d-125">Spécifie différentes options de fonction.</span><span class="sxs-lookup"><span data-stu-id="afc0d-125">Specifies various function options.</span></span> <span data-ttu-id="afc0d-126">Si *pwzFormat* n’a pas la **valeur null**, ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="afc0d-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="afc0d-127">Si *pwzFormat* a la **valeur null**, vous pouvez spécifier une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="afc0d-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="afc0d-128">Si vous ne spécifiez pas de DATE \_ YEARMONTH, date \_ SHORTDATE ou date \_ LONGDATE, et *pwzFormat* est **null**, alors \_ la date SHORTDATE est utilisée comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="afc0d-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="afc0d-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**paramètres régionaux \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="afc0d-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-130">Si cette option est définie, la fonction met en forme la chaîne en utilisant le format de date système par défaut pour les paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="afc0d-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="afc0d-131">Si la valeur n’est pas définie, la fonction met en forme la chaîne à l’aide de n’importe quelle substitution d’utilisateur au format de date par défaut de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="afc0d-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="afc0d-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**paramètres régionaux \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="afc0d-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-133">Utilise la page de codes système ANSI pour la conversion de chaînes à la place de la page de codes des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="afc0d-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="afc0d-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE \_ SHORTDATE**</span><span class="sxs-lookup"><span data-stu-id="afc0d-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-135">Utilise le format de date abrégé.</span><span class="sxs-lookup"><span data-stu-id="afc0d-135">Uses the short date format.</span></span> <span data-ttu-id="afc0d-136">Cette valeur ne peut pas être utilisée avec DATE \_ LONGDATE ou date \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="afc0d-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="afc0d-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE \_ LONGDATE**</span><span class="sxs-lookup"><span data-stu-id="afc0d-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-138">Utilise le format de date longue.</span><span class="sxs-lookup"><span data-stu-id="afc0d-138">Uses the long date format.</span></span> <span data-ttu-id="afc0d-139">Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="afc0d-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="afc0d-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE \_ YEARMONTH**</span><span class="sxs-lookup"><span data-stu-id="afc0d-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-141">Utilise le format année/mois.</span><span class="sxs-lookup"><span data-stu-id="afc0d-141">Uses the year/month format.</span></span> <span data-ttu-id="afc0d-142">Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="afc0d-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="afc0d-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE d' \_ utilisation \_ Alt \_ Calendar**</span><span class="sxs-lookup"><span data-stu-id="afc0d-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-144">Utilise le calendrier de remplacement, le cas échéant, pour mettre en forme la chaîne de date.</span><span class="sxs-lookup"><span data-stu-id="afc0d-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="afc0d-145">Si cet indicateur est défini, la fonction utilise le format par défaut pour ce calendrier de remplacement, plutôt que d’utiliser des remplacements utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afc0d-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="afc0d-146">Les remplacements de l’utilisateur sont utilisés uniquement dans le cas où il n’existe pas de format par défaut pour le calendrier de remplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="afc0d-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="afc0d-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE \_ LTRREADING**</span><span class="sxs-lookup"><span data-stu-id="afc0d-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-148">Ajoute des marques pour la lecture de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="afc0d-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="afc0d-149">Cette valeur ne peut pas être utilisée avec la DATE \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="afc0d-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="afc0d-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="afc0d-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="afc0d-151">Ajoute des marques pour la lecture de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="afc0d-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="afc0d-152">Cette valeur ne peut pas être utilisée avec la DATE \_ LTRREADING.</span><span class="sxs-lookup"><span data-stu-id="afc0d-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="afc0d-153">*lpDate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-154">Type : \**const [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="afc0d-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="afc0d-155">Pointeur vers une structure [_ *SystemTime* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) qui contient les informations de date à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="afc0d-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="afc0d-156">Si ce pointeur est **null**, la fonction utilise la date système locale actuelle.</span><span class="sxs-lookup"><span data-stu-id="afc0d-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="afc0d-157">*pwzFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-158">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="afc0d-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="afc0d-159">Pointeur vers une image de format à utiliser pour former la chaîne de date.</span><span class="sxs-lookup"><span data-stu-id="afc0d-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="afc0d-160">Si *pwzFormat* a la **valeur null**, la fonction utilise le format de date des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="afc0d-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="afc0d-161">Pour plus d’informations, consultez [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="afc0d-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="afc0d-162">*pwzDateStr* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-163">Type : **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="afc0d-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="afc0d-164">Pointeur vers une mémoire tampon qui reçoit la chaîne de Date mise en forme.</span><span class="sxs-lookup"><span data-stu-id="afc0d-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="afc0d-165">*cchDate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc0d-166">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="afc0d-166">Type: **int**</span></span>

<span data-ttu-id="afc0d-167">Spécifie la taille, en caractères, de la mémoire tampon *pwzDateStr* .</span><span class="sxs-lookup"><span data-stu-id="afc0d-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="afc0d-168">Si *cchDate* est égal à zéro, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, et la mémoire tampon vers laquelle pointe *pwzDateStr* n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="afc0d-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc0d-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="afc0d-169">Return value</span></span>

<span data-ttu-id="afc0d-170">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="afc0d-170">Type: **int**</span></span>

<span data-ttu-id="afc0d-171">Si la fonction a abouti, la valeur de retour est le nombre de caractères écrits dans la mémoire tampon vers laquelle pointe *pwzDateStr*.</span><span class="sxs-lookup"><span data-stu-id="afc0d-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="afc0d-172">Si le paramètre *cchDate* est égal à zéro, la valeur de retour est le nombre de caractères requis pour contenir la chaîne de Date mise en forme.</span><span class="sxs-lookup"><span data-stu-id="afc0d-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="afc0d-173">Le nombre comprend le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="afc0d-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="afc0d-174">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="afc0d-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="afc0d-175">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="afc0d-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="afc0d-176">**GetLastError** peut retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="afc0d-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="afc0d-177">**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="afc0d-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="afc0d-178">**indicateurs d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="afc0d-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="afc0d-179">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="afc0d-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="afc0d-180">Notes</span><span class="sxs-lookup"><span data-stu-id="afc0d-180">Remarks</span></span>

<span data-ttu-id="afc0d-181">**GetDateFormatWrapW** offre la possibilité d’utiliser des chaînes Unicode dans des systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afc0d-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="afc0d-182">La méthode recommandée consiste à utiliser [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="afc0d-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="afc0d-183">**GetDateFormatWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 311.</span><span class="sxs-lookup"><span data-stu-id="afc0d-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc0d-184">Spécifications</span><span class="sxs-lookup"><span data-stu-id="afc0d-184">Requirements</span></span>



| <span data-ttu-id="afc0d-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afc0d-185">Requirement</span></span> | <span data-ttu-id="afc0d-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="afc0d-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc0d-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afc0d-187">Minimum supported client</span></span><br/> | <span data-ttu-id="afc0d-188">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afc0d-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afc0d-189">Minimum supported server</span></span><br/> | <span data-ttu-id="afc0d-190">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afc0d-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="afc0d-191">DLL</span><span class="sxs-lookup"><span data-stu-id="afc0d-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc0d-192"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="afc0d-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc0d-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afc0d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc0d-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="afc0d-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
