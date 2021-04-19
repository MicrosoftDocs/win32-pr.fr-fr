---
description: Compare deux listes énumérées de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: DownlevelVerifyScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520130"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="d5b75-103">DownlevelVerifyScripts fonction)</span><span class="sxs-lookup"><span data-stu-id="d5b75-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="d5b75-104">Compare deux listes énumérées de scripts.</span><span class="sxs-lookup"><span data-stu-id="d5b75-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="d5b75-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d5b75-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="d5b75-106">Son utilisation requiert le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d5b75-106">Its use requires the download package.</span></span> <span data-ttu-id="d5b75-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span><span class="sxs-lookup"><span data-stu-id="d5b75-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d5b75-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5b75-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="d5b75-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5b75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b75-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b75-111">Indicateurs spécifiant les options de vérification de script.</span><span class="sxs-lookup"><span data-stu-id="d5b75-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="d5b75-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5b75-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="d5b75-113">Signification</span><span class="sxs-lookup"><span data-stu-id="d5b75-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="d5b75-114"><dt>**VS \_ \_ latin**</dt></span><span class="sxs-lookup"><span data-stu-id="d5b75-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="d5b75-115">Autorisez « LATN » (script latin) dans la liste de tests, même s’il ne figure pas dans la liste des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d5b75-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d5b75-116">*lpLocaleScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b75-117">Pointeur vers la liste des paramètres régionaux, liste énumérée des scripts pour des paramètres régionaux donnés.</span><span class="sxs-lookup"><span data-stu-id="d5b75-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="d5b75-118">Cette liste est généralement remplie en appelant [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span><span class="sxs-lookup"><span data-stu-id="d5b75-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5b75-119">*cchLocaleScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b75-120">Taille, en caractères, de la chaîne indiquée par *lpLocaleScripts*.</span><span class="sxs-lookup"><span data-stu-id="d5b75-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="d5b75-121">L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="d5b75-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="d5b75-122">Si ce paramètre a la valeur 0, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="d5b75-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="d5b75-123">*lpTestScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b75-124">Pointeur vers la liste de tests, une deuxième liste énumérée de scripts.</span><span class="sxs-lookup"><span data-stu-id="d5b75-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="d5b75-125">Cette liste est généralement remplie en appelant [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span><span class="sxs-lookup"><span data-stu-id="d5b75-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5b75-126">*cchTestScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b75-127">Taille, en caractères, de la chaîne indiquée par *lpTestScripts*.</span><span class="sxs-lookup"><span data-stu-id="d5b75-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="d5b75-128">L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="d5b75-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="d5b75-129">Si ce paramètre a la valeur 0, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="d5b75-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b75-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5b75-130">Return value</span></span>

<span data-ttu-id="d5b75-131">Retourne la **valeur true** si la liste de tests n’est pas vide et si tous les éléments de la liste sont également inclus dans la liste des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d5b75-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="d5b75-132">Dans le cas contraire, la fonction retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="d5b75-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="d5b75-133">Une valeur de retour **false** peut indiquer que la liste de tests contient un élément qui n’est pas dans la liste des paramètres régionaux ou qu’elle peut indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d5b75-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="d5b75-134">Pour faire la distinction entre ces deux cas, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d5b75-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="d5b75-135">Si **DownlevelVerifyScripts** a déterminé qu’il existe un élément dans la liste de tests qui ne figure pas dans la liste des paramètres régionaux, **GetLastError** retourne la réussite de l’erreur \_ .</span><span class="sxs-lookup"><span data-stu-id="d5b75-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="d5b75-136">Dans le cas contraire, **GetLastError** peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="d5b75-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="d5b75-137">ERREUR \_ : indicateurs non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="d5b75-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="d5b75-138">Les valeurs fournies pour les indicateurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d5b75-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="d5b75-139">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d5b75-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="d5b75-140">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d5b75-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b75-141">Notes</span><span class="sxs-lookup"><span data-stu-id="d5b75-141">Remarks</span></span>

<span data-ttu-id="d5b75-142">Cette fonction compare des chaînes, telles que « Latn ». Cyrl ;», qui se compose d’une série de noms de script de 4 caractères, chaque nom de script suivi d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="d5b75-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="d5b75-143">Il a également un cas particulier de tenir compte du fait que le script latin est souvent utilisé dans les langages et les paramètres régionaux pour lesquels il n’est pas natif.</span><span class="sxs-lookup"><span data-stu-id="d5b75-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="d5b75-144">Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="d5b75-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="d5b75-145">Voici des exemples de retour de cette fonction et d’un appel ultérieur à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) dans différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="d5b75-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="d5b75-146">Les deux derniers exemples illustrent, respectivement, un cas dans lequel la liste de tests n’a pas de point-virgule de fin (chaîne incorrecte) et un cas dans lequel la liste de tests est vide.</span><span class="sxs-lookup"><span data-stu-id="d5b75-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="d5b75-147">Chaîne « locale »</span><span class="sxs-lookup"><span data-stu-id="d5b75-147">"Locale" string</span></span> | <span data-ttu-id="d5b75-148">Chaîne « test »</span><span class="sxs-lookup"><span data-stu-id="d5b75-148">"Test" string</span></span> | <span data-ttu-id="d5b75-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d5b75-149">*dwFlags*</span></span>        | <span data-ttu-id="d5b75-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5b75-150">Return value</span></span> | <span data-ttu-id="d5b75-151">Retour de GetLastError</span><span class="sxs-lookup"><span data-stu-id="d5b75-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="d5b75-152">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="d5b75-153">Hani;</span><span class="sxs-lookup"><span data-stu-id="d5b75-153">Hani;</span></span>         | <span data-ttu-id="d5b75-154">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-154">N/A</span></span>              | <span data-ttu-id="d5b75-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-155">**TRUE**</span></span>     | <span data-ttu-id="d5b75-156">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-156">N/A</span></span>                       |
| <span data-ttu-id="d5b75-157">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="d5b75-158">Hani; LATN</span><span class="sxs-lookup"><span data-stu-id="d5b75-158">Hani;Latn;</span></span>    | <span data-ttu-id="d5b75-159">0</span><span class="sxs-lookup"><span data-stu-id="d5b75-159">0</span></span>                | <span data-ttu-id="d5b75-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-160">**FALSE**</span></span>    | <span data-ttu-id="d5b75-161">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="d5b75-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="d5b75-162">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="d5b75-163">Hani; LATN</span><span class="sxs-lookup"><span data-stu-id="d5b75-163">Hani;Latn;</span></span>    | <span data-ttu-id="d5b75-164">VS \_ \_ latin</span><span class="sxs-lookup"><span data-stu-id="d5b75-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="d5b75-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-165">**TRUE**</span></span>     | <span data-ttu-id="d5b75-166">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-166">N/A</span></span>                       |
| <span data-ttu-id="d5b75-167">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="d5b75-168">Cyrl</span><span class="sxs-lookup"><span data-stu-id="d5b75-168">Cyrl;</span></span>         | <span data-ttu-id="d5b75-169">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-169">N/A</span></span>              | <span data-ttu-id="d5b75-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-170">**FALSE**</span></span>    | <span data-ttu-id="d5b75-171">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="d5b75-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="d5b75-172">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="d5b75-173">Cyrl</span><span class="sxs-lookup"><span data-stu-id="d5b75-173">Cyrl;</span></span>         | <span data-ttu-id="d5b75-174">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-174">N/A</span></span>              | <span data-ttu-id="d5b75-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-175">**FALSE**</span></span>    | <span data-ttu-id="d5b75-176">paramètre d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="d5b75-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="d5b75-177">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="d5b75-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="d5b75-178">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b75-178">N/A</span></span>              | <span data-ttu-id="d5b75-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d5b75-179">**FALSE**</span></span>    | <span data-ttu-id="d5b75-180">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="d5b75-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="d5b75-181">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="d5b75-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b75-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5b75-182">Requirements</span></span>



| <span data-ttu-id="d5b75-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5b75-183">Requirement</span></span> | <span data-ttu-id="d5b75-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5b75-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b75-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5b75-185">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b75-186">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="d5b75-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5b75-187">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b75-188">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5b75-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="d5b75-189">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d5b75-189">Redistributable</span></span><br/>          | <span data-ttu-id="d5b75-190">API d’atténuation des IDN (Internationalized Domain Name) Microsoft onWindows XP avec SP2, Windows Server 2003 avec SP1, intégral Vista</span><span class="sxs-lookup"><span data-stu-id="d5b75-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="d5b75-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5b75-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b75-192"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b75-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="d5b75-193">DLL</span><span class="sxs-lookup"><span data-stu-id="d5b75-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5b75-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5b75-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="d5b75-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5b75-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b75-196">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="d5b75-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="d5b75-197">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="d5b75-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="d5b75-198">Gestion des noms de domaine internationaux (IDNs)</span><span class="sxs-lookup"><span data-stu-id="d5b75-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="d5b75-199">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="d5b75-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="d5b75-200">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="d5b75-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="d5b75-201">**VerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="d5b75-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
