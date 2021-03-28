---
description: Compare deux chaînes de caractères Unicode à l’aide des paramètres régionaux spécifiés.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972063"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="b49de-103">CompareStringWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="b49de-103">CompareStringWrapW function</span></span>

<span data-ttu-id="b49de-104">\[**CompareStringWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b49de-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="b49de-105">Elle ne sera pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b49de-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="b49de-106">Vous devez utiliser [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="b49de-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="b49de-107">Compare deux chaînes de caractères Unicode à l’aide des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b49de-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="b49de-108">**CompareStringWrapW** est un wrapper pour la fonction **CompareStringW** .</span><span class="sxs-lookup"><span data-stu-id="b49de-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="b49de-109">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .</span><span class="sxs-lookup"><span data-stu-id="b49de-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b49de-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b49de-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="b49de-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b49de-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49de-112">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-113">Type : **LCID**</span><span class="sxs-lookup"><span data-stu-id="b49de-113">Type: **LCID**</span></span>

<span data-ttu-id="b49de-114">Identificateur de paramètres régionaux utilisé pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="b49de-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="b49de-115">Ce paramètre peut être l’un des identificateurs de paramètres régionaux prédéfinis suivants ou un identificateur de paramètres régionaux créé par la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="b49de-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="b49de-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**paramètres régionaux \_ \_ par défaut du système**</span><span class="sxs-lookup"><span data-stu-id="b49de-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-117">Paramètres régionaux par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="b49de-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="b49de-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**paramètres régionaux \_ par défaut de l’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="b49de-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-119">Paramètres régionaux par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="b49de-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b49de-120">*dwCmpFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-121">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b49de-121">Type: **DWORD**</span></span>

<span data-ttu-id="b49de-122">Indicateurs qui indiquent comment la fonction compare les deux chaînes.</span><span class="sxs-lookup"><span data-stu-id="b49de-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="b49de-123">Par défaut, ces indicateurs ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="b49de-123">By default, these flags are not set.</span></span> <span data-ttu-id="b49de-124">Affectez la valeur zéro pour accéder au comportement par défaut ou à n’importe quelle combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b49de-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="b49de-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**\_IGNORECASE normal**</span><span class="sxs-lookup"><span data-stu-id="b49de-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-126">Ignorer la casse.</span><span class="sxs-lookup"><span data-stu-id="b49de-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="b49de-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE normale**</span><span class="sxs-lookup"><span data-stu-id="b49de-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-128">Ne faites pas la distinction entre les caractères Hiragana et Katakana.</span><span class="sxs-lookup"><span data-stu-id="b49de-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="b49de-129">Les caractères Hiragana et Katakana correspondants sont considérés comme égaux.</span><span class="sxs-lookup"><span data-stu-id="b49de-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="b49de-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE normale**</span><span class="sxs-lookup"><span data-stu-id="b49de-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-131">Ignorer les caractères sans espace.</span><span class="sxs-lookup"><span data-stu-id="b49de-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="b49de-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS normale**</span><span class="sxs-lookup"><span data-stu-id="b49de-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-133">Ignorer les symboles.</span><span class="sxs-lookup"><span data-stu-id="b49de-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="b49de-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH normale**</span><span class="sxs-lookup"><span data-stu-id="b49de-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-135">Ne faites pas la distinction entre un caractère codé sur un octet et le même caractère qu’un caractère codé sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="b49de-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="b49de-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**TRIER \_ STRINGSORT**</span><span class="sxs-lookup"><span data-stu-id="b49de-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="b49de-137">Traitez la ponctuation de la même façon que les symboles.</span><span class="sxs-lookup"><span data-stu-id="b49de-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b49de-138">*lpString1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-139">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b49de-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b49de-140">Pointeur vers la première chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="b49de-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="b49de-141">*cchCount1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-142">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="b49de-142">Type: **int**</span></span>

<span data-ttu-id="b49de-143">Nombre de caractères dans la chaîne vers laquelle pointe le paramètre *lpString1* .</span><span class="sxs-lookup"><span data-stu-id="b49de-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="b49de-144">Le nombre n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b49de-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="b49de-145">Si ce paramètre est une valeur négative, il est supposé que la chaîne se termine par un caractère null et que la longueur est calculée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b49de-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="b49de-146">*lpString2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-147">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b49de-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b49de-148">Pointeur vers la deuxième chaîne Unicode à comparer.</span><span class="sxs-lookup"><span data-stu-id="b49de-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="b49de-149">*cchCount2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49de-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49de-150">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="b49de-150">Type: **int**</span></span>

<span data-ttu-id="b49de-151">Nombre de caractères dans la chaîne vers laquelle pointe le paramètre *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="b49de-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="b49de-152">Le nombre n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b49de-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="b49de-153">Si ce paramètre est une valeur négative, il est supposé que la chaîne se termine par un caractère null et que la longueur est calculée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b49de-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49de-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b49de-154">Return value</span></span>

<span data-ttu-id="b49de-155">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="b49de-155">Type: **int**</span></span>

<span data-ttu-id="b49de-156">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b49de-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="b49de-157">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b49de-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="b49de-158">**GetLastError** peut retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="b49de-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="b49de-159">indicateurs d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="b49de-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="b49de-160">paramètre d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="b49de-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="b49de-161">Si la fonction est réussie, la valeur de retour est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b49de-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="b49de-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b49de-162">Requirement</span></span> | <span data-ttu-id="b49de-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49de-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49de-164">CSTR \_ inférieur \_ à</span><span class="sxs-lookup"><span data-stu-id="b49de-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="b49de-165">La chaîne vers laquelle pointe le paramètre *lpString1* est inférieure à la valeur lexicale par rapport à la chaîne vers laquelle pointe le paramètre *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="b49de-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="b49de-166">CSTR \_ égal</span><span class="sxs-lookup"><span data-stu-id="b49de-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="b49de-167">La chaîne vers laquelle pointe *lpString1* est égale à la valeur lexicale à la chaîne désignée par *lpString2*.</span><span class="sxs-lookup"><span data-stu-id="b49de-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="b49de-168">CSTR \_ supérieur \_ à</span><span class="sxs-lookup"><span data-stu-id="b49de-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="b49de-169">La chaîne pointée par *lpString1* est plus grande dans la valeur lexicale que la chaîne vers laquelle pointe *lpString2*</span><span class="sxs-lookup"><span data-stu-id="b49de-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="b49de-170">Notes</span><span class="sxs-lookup"><span data-stu-id="b49de-170">Remarks</span></span>

<span data-ttu-id="b49de-171">**Avertissement de sécurité :** L’utilisation incorrecte de cette fonction peut compromettre la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="b49de-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="b49de-172">Les chaînes qui ne sont pas comparées correctement peuvent produire une entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="b49de-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="b49de-173">Testez les chaînes pour vous assurer qu’elles sont valides avant de les utiliser et fournissez des gestionnaires d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b49de-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="b49de-174">Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="b49de-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="b49de-175">La méthode recommandée consiste à utiliser [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="b49de-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="b49de-176">**CompareStringWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 45.</span><span class="sxs-lookup"><span data-stu-id="b49de-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49de-177">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b49de-177">Requirements</span></span>



| <span data-ttu-id="b49de-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b49de-178">Requirement</span></span> | <span data-ttu-id="b49de-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49de-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49de-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49de-180">Minimum supported client</span></span><br/> | <span data-ttu-id="b49de-181">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49de-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b49de-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49de-182">Minimum supported server</span></span><br/> | <span data-ttu-id="b49de-183">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49de-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b49de-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="b49de-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49de-185"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="b49de-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="b49de-186">DLL</span><span class="sxs-lookup"><span data-stu-id="b49de-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b49de-187"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b49de-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49de-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49de-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49de-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="b49de-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
