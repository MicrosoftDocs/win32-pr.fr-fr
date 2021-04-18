---
description: Obsolète.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519924"
---
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="5718c-103">GetCalendarDateFormatEx fonction)</span><span class="sxs-lookup"><span data-stu-id="5718c-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="5718c-104">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5718c-104">Deprecated.</span></span> <span data-ttu-id="5718c-105">Récupère une chaîne de date correctement mise en forme pour les paramètres régionaux spécifiés à l’aide de la date et du calendrier spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5718c-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="5718c-106">L’utilisateur peut spécifier le format de date abrégé, le format de date longue, le format d’année mois ou un modèle de format personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5718c-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="5718c-107">Cette fonction peut récupérer des données qui changent entre des mises en production, par exemple en raison de paramètres régionaux personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5718c-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="5718c-108">Si votre application doit rendre persistantes ou transmettre des données, consultez [utilisation de données de paramètres régionaux persistants](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="5718c-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5718c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5718c-109">Syntax</span></span>


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="5718c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5718c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5718c-111">*lpszLocale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5718c-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-112">Pointeur vers un nom de paramètres régionaux, ou l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="5718c-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="5718c-113">nom de paramètres régionaux \_ \_ invariant</span><span class="sxs-lookup"><span data-stu-id="5718c-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="5718c-114">paramètres régionaux \_ \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="5718c-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="5718c-115">nom des paramètres régionaux \_ \_ \_ par défaut de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5718c-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="5718c-116">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5718c-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-117">Indicateurs spécifiant les options de format de date.</span><span class="sxs-lookup"><span data-stu-id="5718c-117">Flags specifying date format options.</span></span> <span data-ttu-id="5718c-118">Si *lpFormat* n’a pas la valeur **null**, ce paramètre doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="5718c-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="5718c-119">Si *lpFormat* a la valeur **null**, l’application peut spécifier une combinaison des valeurs suivantes et des [paramètres régionaux \_ NOUSEROVERRIDE](locale-nouseroverride.md).</span><span class="sxs-lookup"><span data-stu-id="5718c-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="5718c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5718c-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="5718c-121">Signification</span><span class="sxs-lookup"><span data-stu-id="5718c-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="5718c-122"><dt>**DATE \_ SHORTDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="5718c-123">Utilisez le format de date abrégé.</span><span class="sxs-lookup"><span data-stu-id="5718c-123">Use the short date format.</span></span> <span data-ttu-id="5718c-124">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5718c-124">This is the default.</span></span> <span data-ttu-id="5718c-125">Cette valeur ne peut pas être utilisée avec DATE \_ LONGDATE ou date \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="5718c-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="5718c-126"><dt>**DATE \_ LONGDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="5718c-127">Utilisez le format de date longue.</span><span class="sxs-lookup"><span data-stu-id="5718c-127">Use the long date format.</span></span> <span data-ttu-id="5718c-128">Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="5718c-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="5718c-129"><dt>**DATE \_ YEARMONTH**</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="5718c-130">Utilisez le format année/mois.</span><span class="sxs-lookup"><span data-stu-id="5718c-130">Use the year/month format.</span></span> <span data-ttu-id="5718c-131">Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="5718c-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="5718c-132"><dt>**DATE \_ LTRREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="5718c-133">Ajoutez des marques pour la lecture de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="5718c-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="5718c-134">Cette valeur ne peut pas être utilisée avec la DATE \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="5718c-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="5718c-135"><dt>**DATE \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="5718c-136">Ajoutez des marques pour la lecture de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="5718c-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="5718c-137">Cette valeur ne peut pas être utilisée avec la DATE \_ LTRREADING</span><span class="sxs-lookup"><span data-stu-id="5718c-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="5718c-138">*lpCalDateTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5718c-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-139">Pointeur vers une structure [**CALDATETIME**](caldatetime.md) qui contient les informations de date et de calendrier à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="5718c-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="5718c-140">*lpFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5718c-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-141">Pointeur vers une chaîne de format d’image utilisée pour former la chaîne de date.</span><span class="sxs-lookup"><span data-stu-id="5718c-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="5718c-142">Les valeurs possibles pour la chaîne format image sont définies dans les [images de format jour, mois, année et ère](day--month--year--and-era-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="5718c-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="5718c-143">La chaîne de l’image de format doit se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="5718c-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="5718c-144">La fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format image, par exemple, les noms des jours et des mois pour les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="5718c-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="5718c-145">L’application affecte la **valeur null** à ce paramètre si la fonction doit utiliser le format de date des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5718c-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="5718c-146">*lpDateStr* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5718c-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-147">Pointeur vers une mémoire tampon dans laquelle cette fonction reçoit la chaîne de Date mise en forme.</span><span class="sxs-lookup"><span data-stu-id="5718c-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="5718c-148">*cchDate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5718c-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5718c-149">Taille, en caractères, de la mémoire tampon *lpDateStr* .</span><span class="sxs-lookup"><span data-stu-id="5718c-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="5718c-150">L’application peut également affecter la valeur 0 à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5718c-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="5718c-151">Dans ce cas, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, et le paramètre *lpDateStr* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5718c-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5718c-152">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5718c-152">Return value</span></span>

<span data-ttu-id="5718c-153">Retourne le nombre de caractères écrits dans la mémoire tampon *lpDateStr* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5718c-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="5718c-154">Si le paramètre *cchDate* a la valeur 0, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="5718c-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="5718c-155">Cette fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="5718c-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="5718c-156">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="5718c-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="5718c-157">\_date \_ d’erreur \_ hors \_ limites.</span><span class="sxs-lookup"><span data-stu-id="5718c-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="5718c-158">La date spécifiée était hors limites.</span><span class="sxs-lookup"><span data-stu-id="5718c-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="5718c-159">ERREUR \_ de \_ mémoire tampon insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5718c-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="5718c-160">La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5718c-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="5718c-161">ERREUR \_ : indicateurs non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="5718c-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="5718c-162">Les valeurs fournies pour les indicateurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5718c-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="5718c-163">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="5718c-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="5718c-164">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5718c-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5718c-165">Notes</span><span class="sxs-lookup"><span data-stu-id="5718c-165">Remarks</span></span>

<span data-ttu-id="5718c-166">La première Date prise en charge par cette fonction est le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="5718c-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="5718c-167">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="5718c-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="5718c-168">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="5718c-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="5718c-169">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5718c-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="5718c-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5718c-170">Requirements</span></span>



| <span data-ttu-id="5718c-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5718c-171">Requirement</span></span> | <span data-ttu-id="5718c-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="5718c-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5718c-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5718c-173">Minimum supported client</span></span><br/> | <span data-ttu-id="5718c-174">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5718c-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5718c-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5718c-175">Minimum supported server</span></span><br/> | <span data-ttu-id="5718c-176">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5718c-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5718c-177">DLL</span><span class="sxs-lookup"><span data-stu-id="5718c-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5718c-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5718c-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5718c-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5718c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5718c-180">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="5718c-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="5718c-181">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="5718c-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="5718c-182">Images de format de jour, de mois, d’année et d’ère</span><span class="sxs-lookup"><span data-stu-id="5718c-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="5718c-183">NLS : exemple d’API basées sur un nom</span><span class="sxs-lookup"><span data-stu-id="5718c-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="5718c-184">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="5718c-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="5718c-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="5718c-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="5718c-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5718c-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="5718c-187">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="5718c-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
