---
description: Fournit la liste des scripts utilisés dans la chaîne Unicode spécifiée.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: DownlevelGetStringScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534718"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="4bba8-103">DownlevelGetStringScripts fonction)</span><span class="sxs-lookup"><span data-stu-id="4bba8-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="4bba8-104">Fournit la liste des scripts utilisés dans la chaîne Unicode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4bba8-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="4bba8-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4bba8-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="4bba8-106">Son utilisation requiert le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4bba8-106">Its use requires the download package.</span></span> <span data-ttu-id="4bba8-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span><span class="sxs-lookup"><span data-stu-id="4bba8-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4bba8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bba8-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="4bba8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bba8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bba8-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-111">Indicateurs spécifiant des options pour la récupération de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="4bba8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bba8-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="4bba8-113">Signification</span><span class="sxs-lookup"><span data-stu-id="4bba8-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="4bba8-114"><dt>**GSS \_ autoriser l' \_ héritage \_ commun**</dt></span><span class="sxs-lookup"><span data-stu-id="4bba8-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="4bba8-115">Récupérez les informations de script « Qaii » (hérité) et « ZYYY » (communes).</span><span class="sxs-lookup"><span data-stu-id="4bba8-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="4bba8-116">Cette valeur n’affecte pas le traitement des caractères non assignés.</span><span class="sxs-lookup"><span data-stu-id="4bba8-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="4bba8-117">Ces caractères dans la chaîne d’entrée provoquent toujours l’affichage d’un « zzzz » (script non assigné) dans la chaîne de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="4bba8-118">Par défaut, cette fonction ignore les caractères hérités ou communs dans la chaîne Unicode d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4bba8-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="4bba8-119">Si GSS \_ allow \_ \_ Common Common n’est pas défini, « Qaii » et « ZYYY » ne s’affichent pas dans la chaîne de script, même si la chaîne d’entrée contient des caractères de ce type.</span><span class="sxs-lookup"><span data-stu-id="4bba8-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="4bba8-120">Si GSS \_ autorise \_ \_ l’héritage commun est défini et si la chaîne d’entrée contient des caractères hérités et/ou communs, « Qaii » et/ou « ZYYY » apparaissent dans la chaîne de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="4bba8-121">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4bba8-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="4bba8-122">*lpString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-123">Pointeur vers la chaîne Unicode à analyser.</span><span class="sxs-lookup"><span data-stu-id="4bba8-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="4bba8-124">*cchString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-125">Taille, en caractères, de la chaîne Unicode indiquée par *lpString*.</span><span class="sxs-lookup"><span data-stu-id="4bba8-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="4bba8-126">L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4bba8-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="4bba8-127">Si l’application définit ce paramètre sur 0, la fonction récupère une chaîne Unicode null (L " \\ 0") dans *lpScripts* et retourne 1.</span><span class="sxs-lookup"><span data-stu-id="4bba8-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="4bba8-128">*lpScripts* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-129">Pointeur vers une mémoire tampon dans laquelle cette fonction récupère une chaîne se terminant par un caractère null qui représente une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="4bba8-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="4bba8-130">Chaque nom de script se compose de quatre caractères latins, et les noms sont récupérés dans l’ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="4bba8-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="4bba8-131">Chaque nom, y compris le dernier, est suivi d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="4bba8-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="4bba8-132">Ce paramètre peut également contenir la **valeur null** si *cchScripts* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="4bba8-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="4bba8-133">Dans ce cas, la fonction retourne la taille requise pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4bba8-134">*cchScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bba8-135">Taille, en caractères, de la mémoire tampon de script indiquée par *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="4bba8-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="4bba8-136">L’application peut également affecter la valeur 0 à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4bba8-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="4bba8-137">Dans ce cas, la fonction récupère la **valeur null** dans *lpScripts* et retourne la taille requise pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bba8-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bba8-138">Return value</span></span>

<span data-ttu-id="4bba8-139">Retourne le nombre de caractères récupérés dans la mémoire tampon de sortie, y compris un caractère null de fin, en cas de réussite et *cchScripts* est défini sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="4bba8-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="4bba8-140">La fonction retourne 1 pour indiquer qu’aucun script n’a été trouvé, par exemple, quand la chaîne d’entrée contient uniquement des caractères communs ou HÉRITÉs et que GSS \_ allow \_ \_ Common Common n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4bba8-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="4bba8-141">Étant donné que chaque script trouvé ajoute cinq caractères (quatre caractères + délimiteur), une opération mathématique simple fournit le nombre de scripts sous la forme ( \_ Code de retour-1)/5.</span><span class="sxs-lookup"><span data-stu-id="4bba8-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="4bba8-142">Si la fonction est réussie et que la valeur de *cchScripts* est 0, la valeur de retour est la taille requise, en caractères incluant un caractère null de fin, pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="4bba8-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="4bba8-143">Le nombre de scripts est décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4bba8-143">The script count is as described above.</span></span>

<span data-ttu-id="4bba8-144">La fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="4bba8-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="4bba8-145">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="4bba8-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4bba8-146">ERREUR \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="4bba8-146">ERROR\_BADDB.</span></span> <span data-ttu-id="4bba8-147">La fonction n’a pas pu accéder aux données.</span><span class="sxs-lookup"><span data-stu-id="4bba8-147">The function could not access the data.</span></span> <span data-ttu-id="4bba8-148">Cette situation ne doit normalement pas se produire, et indique généralement une installation incorrecte, un problème de disque ou similaire.</span><span class="sxs-lookup"><span data-stu-id="4bba8-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="4bba8-149">ERREUR \_ de \_ mémoire tampon insuffisante.</span><span class="sxs-lookup"><span data-stu-id="4bba8-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="4bba8-150">La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4bba8-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="4bba8-151">ERREUR \_ : indicateurs non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="4bba8-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="4bba8-152">Les valeurs fournies pour les indicateurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4bba8-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="4bba8-153">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4bba8-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4bba8-154">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4bba8-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bba8-155">Notes</span><span class="sxs-lookup"><span data-stu-id="4bba8-155">Remarks</span></span>

<span data-ttu-id="4bba8-156">Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="4bba8-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="4bba8-157">La détermination du script est basée sur les valeurs de script publiées par le consortium Unicode dans <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , sauf que les caractères non assignés ont la valeur « zzzz » (non assigné) au lieu de « ZYYY » (commun).</span><span class="sxs-lookup"><span data-stu-id="4bba8-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="4bba8-158">Voici quelques exemples du comportement de cette fonction :</span><span class="sxs-lookup"><span data-stu-id="4bba8-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="4bba8-159">Chaîne d’entrée</span><span class="sxs-lookup"><span data-stu-id="4bba8-159">Input string</span></span>

<span data-ttu-id="4bba8-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4bba8-160">*dwFlags*</span></span>

<span data-ttu-id="4bba8-161">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="4bba8-161">*lpScripts*</span></span>

<span data-ttu-id="4bba8-162">Scripts</span><span class="sxs-lookup"><span data-stu-id="4bba8-162">Scripts</span></span>

<span data-ttu-id="4bba8-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4bba8-163">Microsoft.com</span></span>

<span data-ttu-id="4bba8-164">0</span><span class="sxs-lookup"><span data-stu-id="4bba8-164">0</span></span>

<span data-ttu-id="4bba8-165">LATN</span><span class="sxs-lookup"><span data-stu-id="4bba8-165">Latn;</span></span>

<span data-ttu-id="4bba8-166">Latin</span><span class="sxs-lookup"><span data-stu-id="4bba8-166">Latin</span></span>

<span data-ttu-id="4bba8-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4bba8-167">Microsoft.com</span></span>

<span data-ttu-id="4bba8-168">GSS \_ autoriser l' \_ héritage \_ commun</span><span class="sxs-lookup"><span data-stu-id="4bba8-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="4bba8-169">LATN Zyyy;</span><span class="sxs-lookup"><span data-stu-id="4bba8-169">Latn;Zyyy;</span></span>

<span data-ttu-id="4bba8-170">Latin + courant</span><span class="sxs-lookup"><span data-stu-id="4bba8-170">Latin + Common</span></span>

<span data-ttu-id="4bba8-171">$ {ROWSPAN2} $Ni ÑO $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="4bba8-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="4bba8-173">$ {ROWSPAN2} $GSS \_ autoriser l' \_ héritage \_ $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-174">$ {ROWSPAN2} $Latn ; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-175">$ {ROWSPAN2} $Latin $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-176">Utilise la lettre minuscule latine N avec TILDE</span><span class="sxs-lookup"><span data-stu-id="4bba8-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="4bba8-177">$ {ROWSPAN2} $Ni ÑO $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="4bba8-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="4bba8-179">$ {ROWSPAN2} $GSS \_ autoriser l' \_ héritage \_ $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-180">$Latn $ {ROWSPAN2}; Qaii ; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-181">$ {ROWSPAN2} $Latin + + hérité $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-182">Utilise la combinaison TILDE</span><span class="sxs-lookup"><span data-stu-id="4bba8-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="4bba8-183">$ {ROWSPAN2} $Sp ооf $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="4bba8-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="4bba8-185">$ {ROWSPAN2} $0 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-186">$Latn $ {ROWSPAN2}; Cyrl ; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-187">$ {ROWSPAN2} $Latin + cyrillique $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4bba8-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="4bba8-188">Utilise la lettre minuscule cyrillique O</span><span class="sxs-lookup"><span data-stu-id="4bba8-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="4bba8-189"></span><span class="sxs-lookup"><span data-stu-id="4bba8-189"></span></span>

<span data-ttu-id="4bba8-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="4bba8-190">U+f000</span></span>

<span data-ttu-id="4bba8-191">0</span><span class="sxs-lookup"><span data-stu-id="4bba8-191">0</span></span>

<span data-ttu-id="4bba8-192">Zzzz</span><span class="sxs-lookup"><span data-stu-id="4bba8-192">Zzzz;</span></span>

<span data-ttu-id="4bba8-193">Non affecté</span><span class="sxs-lookup"><span data-stu-id="4bba8-193">Unassigned</span></span>

<span data-ttu-id="4bba8-194"></span><span class="sxs-lookup"><span data-stu-id="4bba8-194"></span></span>

<span data-ttu-id="4bba8-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="4bba8-195">U+f000</span></span>

<span data-ttu-id="4bba8-196">GSS \_ autoriser l' \_ héritage \_ commun</span><span class="sxs-lookup"><span data-stu-id="4bba8-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="4bba8-197">Zzzz</span><span class="sxs-lookup"><span data-stu-id="4bba8-197">Zzzz;</span></span>

<span data-ttu-id="4bba8-198">Non affecté</span><span class="sxs-lookup"><span data-stu-id="4bba8-198">Unassigned</span></span>



 

<span data-ttu-id="4bba8-199">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="4bba8-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bba8-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bba8-200">Requirements</span></span>



| <span data-ttu-id="4bba8-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bba8-201">Requirement</span></span> | <span data-ttu-id="4bba8-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bba8-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bba8-203">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bba8-203">Minimum supported client</span></span><br/> | <span data-ttu-id="4bba8-204">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="4bba8-205">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bba8-205">Minimum supported server</span></span><br/> | <span data-ttu-id="4bba8-206">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bba8-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="4bba8-207">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4bba8-207">Redistributable</span></span><br/>          | <span data-ttu-id="4bba8-208">API d’atténuation des IDN (Internationalized Domain Name) Microsoft sur Windows XP (SP2 ou version ultérieure), Windows Server 2003 (SP1 ou version ultérieure) ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bba8-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="4bba8-209">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bba8-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bba8-210"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bba8-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="4bba8-211">DLL</span><span class="sxs-lookup"><span data-stu-id="4bba8-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bba8-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bba8-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="4bba8-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bba8-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bba8-214">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="4bba8-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4bba8-215">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="4bba8-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4bba8-216">Gestion des noms de domaine internationaux (IDNs)</span><span class="sxs-lookup"><span data-stu-id="4bba8-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="4bba8-217">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="4bba8-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="4bba8-218">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="4bba8-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="4bba8-219">**GetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="4bba8-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
