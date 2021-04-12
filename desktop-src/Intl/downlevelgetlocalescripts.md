---
description: Fournit une liste de scripts pour les paramètres régionaux spécifiés.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: DownlevelGetLocaleScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210054"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="1c5ba-103">DownlevelGetLocaleScripts fonction)</span><span class="sxs-lookup"><span data-stu-id="1c5ba-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="1c5ba-104">Fournit une liste de scripts pour les paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="1c5ba-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="1c5ba-106">Son utilisation requiert le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-106">Its use requires the download package.</span></span> <span data-ttu-id="1c5ba-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCTYPE* défini sur [locale \_ SSCRIPTS](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="1c5ba-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1c5ba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c5ba-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="1c5ba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c5ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5ba-110">*lpLocaleName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c5ba-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5ba-111">Pointeur vers un [nom de paramètres régionaux](locale-names.md)se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c5ba-112">*lpScripts* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1c5ba-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5ba-113">Pointeur vers une mémoire tampon dans laquelle cette fonction récupère une chaîne se terminant par un caractère null qui représente une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="1c5ba-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="1c5ba-114">Chaque nom de script se compose de quatre caractères latins, et les noms sont récupérés dans l’ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="1c5ba-115">Chacune d’entre elles, y compris la dernière, est suivie d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="1c5ba-116">Ce paramètre peut également contenir la **valeur null** si *cchScripts* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="1c5ba-117">Dans ce cas, la fonction retourne la taille requise pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1c5ba-118">*cchScripts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c5ba-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5ba-119">Taille, en caractères, de la mémoire tampon de script indiquée par *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="1c5ba-120">L’application peut également affecter la valeur 0 à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="1c5ba-121">Dans ce cas, la fonction récupère la **valeur null** dans *lpScripts* et retourne la taille requise pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5ba-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c5ba-122">Return value</span></span>

<span data-ttu-id="1c5ba-123">Retourne le nombre de caractères récupérés dans la mémoire tampon de script, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="1c5ba-124">Si la fonction est réussie et que la valeur de *cchScripts* est 0, la valeur de retour est la taille requise, en caractères incluant un caractère null de fin, pour la mémoire tampon de script.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="1c5ba-125">Cette fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="1c5ba-126">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="1c5ba-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="1c5ba-127">ERREUR \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-127">ERROR\_BADDB.</span></span> <span data-ttu-id="1c5ba-128">La fonction n’a pas pu accéder aux données.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-128">The function could not access the data.</span></span> <span data-ttu-id="1c5ba-129">Cette situation ne doit normalement pas se produire, et indique généralement une installation incorrecte, un problème de disque ou similaire.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="1c5ba-130">ERREUR \_ de \_ mémoire tampon insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="1c5ba-131">La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="1c5ba-132">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="1c5ba-133">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5ba-134">Notes</span><span class="sxs-lookup"><span data-stu-id="1c5ba-134">Remarks</span></span>

<span data-ttu-id="1c5ba-135">Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="1c5ba-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="1c5ba-136">Voici quelques exemples d’entrées et de sorties pour cette fonction, en supposant une taille de mémoire tampon suffisante :</span><span class="sxs-lookup"><span data-stu-id="1c5ba-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="1c5ba-137">Paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="1c5ba-137">Locale</span></span>                  | <span data-ttu-id="1c5ba-138">*lpLocaleName*</span><span class="sxs-lookup"><span data-stu-id="1c5ba-138">*lpLocaleName*</span></span> | <span data-ttu-id="1c5ba-139">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="1c5ba-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="1c5ba-140">Anglais (États-Unis)</span><span class="sxs-lookup"><span data-stu-id="1c5ba-140">English (United States)</span></span> | <span data-ttu-id="1c5ba-141">fr-FR</span><span class="sxs-lookup"><span data-stu-id="1c5ba-141">en-US</span></span>          | <span data-ttu-id="1c5ba-142">LATN</span><span class="sxs-lookup"><span data-stu-id="1c5ba-142">Latn;</span></span>           |
| <span data-ttu-id="1c5ba-143">Hindi (Inde)</span><span class="sxs-lookup"><span data-stu-id="1c5ba-143">Hindi (India)</span></span>           | <span data-ttu-id="1c5ba-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="1c5ba-144">hi-IN</span></span>          | <span data-ttu-id="1c5ba-145">Deva</span><span class="sxs-lookup"><span data-stu-id="1c5ba-145">Deva;</span></span>           |
| <span data-ttu-id="1c5ba-146">Japonais (Japon)</span><span class="sxs-lookup"><span data-stu-id="1c5ba-146">Japanese (Japan)</span></span>        | <span data-ttu-id="1c5ba-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="1c5ba-147">ja-JP</span></span>          | <span data-ttu-id="1c5ba-148">Hani; Hira; Caractères Kana</span><span class="sxs-lookup"><span data-stu-id="1c5ba-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="1c5ba-149">La liste ne contient pas le script latin, sauf s’il s’agit d’une partie essentielle du système d’écriture utilisé pour les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="1c5ba-150">Toutefois, les caractères latins sont souvent utilisés dans le contexte des paramètres régionaux pour lesquels ils ne sont pas natifs, comme pour un nom d’entreprise étranger.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="1c5ba-151">Dans l’exemple ci-dessus pour l’hindi en Inde, le seul script récupéré est « Deva » (pour DÉVANÂGARÎ), bien que les caractères latins puissent également apparaître dans le texte hindi.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="1c5ba-152">La fonction [**DownlevelVerifyScripts**](downlevelverifyscripts.md) a un indicateur spécial pour traiter ce cas.</span><span class="sxs-lookup"><span data-stu-id="1c5ba-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="1c5ba-153">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="1c5ba-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5ba-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c5ba-154">Requirements</span></span>



| <span data-ttu-id="1c5ba-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c5ba-155">Requirement</span></span> | <span data-ttu-id="1c5ba-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c5ba-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5ba-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c5ba-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5ba-158">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c5ba-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="1c5ba-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c5ba-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5ba-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c5ba-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="1c5ba-161">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1c5ba-161">Redistributable</span></span><br/>          | <span data-ttu-id="1c5ba-162">API d’atténuation des IDN (Internationalized Domain Name) Microsoft sur Windows XP (SP2 ou version ultérieure), Windows Server 2003 (SP1 ou version ultérieure) ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c5ba-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="1c5ba-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c5ba-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c5ba-164"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c5ba-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="1c5ba-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5ba-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c5ba-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5ba-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1c5ba-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c5ba-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5ba-168">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="1c5ba-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="1c5ba-169">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="1c5ba-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="1c5ba-170">Gestion des noms de domaine internationaux (IDNs)</span><span class="sxs-lookup"><span data-stu-id="1c5ba-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="1c5ba-171">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="1c5ba-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="1c5ba-172">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="1c5ba-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="1c5ba-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="1c5ba-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
