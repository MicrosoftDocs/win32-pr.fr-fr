---
description: Récupère le nom des paramètres régionaux pour le parent des paramètres régionaux fournis.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: DownlevelGetParentLocaleName, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952816"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="85ea4-103">DownlevelGetParentLocaleName fonction)</span><span class="sxs-lookup"><span data-stu-id="85ea4-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="85ea4-104">Récupère le [nom des paramètres régionaux](locale-names.md) pour le parent des paramètres régionaux fournis.</span><span class="sxs-lookup"><span data-stu-id="85ea4-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="85ea4-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="85ea4-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="85ea4-106">Son utilisation requiert le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="85ea4-106">Its use requires the download package.</span></span> <span data-ttu-id="85ea4-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCTYPE* défini sur [locale \_ sParent](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="85ea4-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85ea4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85ea4-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="85ea4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85ea4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ea4-110">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85ea4-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ea4-111">[Identificateur de paramètres régionaux](locale-identifiers.md) des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="85ea4-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="85ea4-112">Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux ou utiliser l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="85ea4-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="85ea4-113">paramètres régionaux \_ INvariants</span><span class="sxs-lookup"><span data-stu-id="85ea4-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="85ea4-114">paramètres régionaux \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="85ea4-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="85ea4-115">paramètres régionaux \_ par défaut de l’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="85ea4-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="85ea4-116">**Windows Vista et versions ultérieures :** Les identificateurs de paramètres régionaux personnalisés suivants sont également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="85ea4-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="85ea4-117">paramètres régionaux \_ personnalisés \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="85ea4-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="85ea4-118">paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_</span><span class="sxs-lookup"><span data-stu-id="85ea4-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="85ea4-119">paramètres régionaux \_ personnalisés \_ non spécifiés</span><span class="sxs-lookup"><span data-stu-id="85ea4-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="85ea4-120">*lpName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="85ea4-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ea4-121">Pointeur vers une mémoire tampon dans laquelle la fonction récupère le nom de paramètres régionaux parent, ou l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="85ea4-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="85ea4-122">Ce paramètre a la valeur **null** si *cchName* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="85ea4-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="85ea4-123">nom de paramètres régionaux \_ \_ invariant</span><span class="sxs-lookup"><span data-stu-id="85ea4-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="85ea4-124">paramètres régionaux \_ \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="85ea4-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="85ea4-125">nom des paramètres régionaux \_ \_ \_ par défaut de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="85ea4-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="85ea4-126">*cchName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85ea4-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ea4-127">Taille de la mémoire tampon indiquée par *lpName*, en points de code UTF-16.</span><span class="sxs-lookup"><span data-stu-id="85ea4-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="85ea4-128">La valeur 0 pour ce paramètre fait en sorte que la fonction ignore la mémoire tampon *lpName* et retourne la taille de la mémoire tampon, en caractères (caractères null inclus), requis pour contenir le nom des paramètres régionaux parents.</span><span class="sxs-lookup"><span data-stu-id="85ea4-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ea4-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85ea4-129">Return value</span></span>

<span data-ttu-id="85ea4-130">Retourne le nombre de points de code UTF-16 dans le nom des paramètres régionaux, y compris le caractère null de fin, en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="85ea4-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="85ea4-131">Cette fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="85ea4-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="85ea4-132">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="85ea4-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="85ea4-133">ERREUR \_ de \_ mémoire tampon insuffisante.</span><span class="sxs-lookup"><span data-stu-id="85ea4-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="85ea4-134">La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="85ea4-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="85ea4-135">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="85ea4-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="85ea4-136">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="85ea4-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ea4-137">Notes</span><span class="sxs-lookup"><span data-stu-id="85ea4-137">Remarks</span></span>

<span data-ttu-id="85ea4-138">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="85ea4-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ea4-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85ea4-139">Requirements</span></span>



| <span data-ttu-id="85ea4-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85ea4-140">Requirement</span></span> | <span data-ttu-id="85ea4-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ea4-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85ea4-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ea4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="85ea4-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ea4-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85ea4-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ea4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="85ea4-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ea4-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85ea4-146">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="85ea4-146">Redistributable</span></span><br/>          | <span data-ttu-id="85ea4-147">API de mappage de données Microsoft NLS onWindows XP avec SP2 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="85ea4-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="85ea4-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="85ea4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ea4-149"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ea4-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="85ea4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="85ea4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85ea4-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ea4-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ea4-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85ea4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ea4-153">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="85ea4-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="85ea4-154">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="85ea4-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="85ea4-155">Mappage des données de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="85ea4-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="85ea4-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="85ea4-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
