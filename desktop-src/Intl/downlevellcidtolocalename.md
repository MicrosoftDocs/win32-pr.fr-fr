---
description: Convertit un identificateur de paramètres régionaux en un nom de paramètres régionaux.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: DownlevelLCIDToLocaleName, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520719"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="7e99f-103">DownlevelLCIDToLocaleName fonction)</span><span class="sxs-lookup"><span data-stu-id="7e99f-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="7e99f-104">Convertit un [identificateur de paramètres régionaux](locale-identifiers.md) en un [nom de paramètres régionaux](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="7e99f-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="7e99f-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e99f-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="7e99f-106">Son utilisation requiert un package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="7e99f-106">Its use requires a download package.</span></span> <span data-ttu-id="7e99f-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) pour récupérer un nom de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7e99f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e99f-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7e99f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e99f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e99f-110">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e99f-111">Identificateur de paramètres régionaux à convertir.</span><span class="sxs-lookup"><span data-stu-id="7e99f-111">The locale identifier to translate.</span></span> <span data-ttu-id="7e99f-112">Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="7e99f-113">Cette fonction ne prend pas en charge les paramètres régionaux neutres ou les valeurs d’identificateur de paramètres régionaux spécifiques suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e99f-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="7e99f-114">paramètres régionaux \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="7e99f-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="7e99f-115">paramètres régionaux \_ par défaut de l’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="7e99f-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="7e99f-116">paramètres régionaux \_ personnalisés \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="7e99f-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="7e99f-117">paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_</span><span class="sxs-lookup"><span data-stu-id="7e99f-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="7e99f-118">paramètres régionaux \_ personnalisés \_ non spécifiés</span><span class="sxs-lookup"><span data-stu-id="7e99f-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="7e99f-119">*lpName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e99f-120">Pointeur vers une mémoire tampon dans laquelle cette fonction récupère le nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="7e99f-121">La fonction récupère la **valeur null** si *cchName* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7e99f-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7e99f-122">*cchName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e99f-123">Taille, en points de code UTF-16, de la mémoire tampon du nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="7e99f-124">L’application affecte à ce paramètre la valeur 0 pour retourner la taille requise de la mémoire tampon du nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7e99f-125">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e99f-126">Indicateurs spécifiant le type de nom à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7e99f-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="7e99f-127">La valeur par défaut est le nom des paramètres régionaux de niveau inférieur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7e99f-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e99f-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e99f-128">Return value</span></span>

<span data-ttu-id="7e99f-129">Retourne le nombre de points de code UTF-16 dans le nom des paramètres régionaux, y compris le caractère null de fin, en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="7e99f-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="7e99f-130">Si la fonction est réussie et que la valeur de *cchName* est 0, la valeur de retour est la taille requise, en caractères (y compris les caractères null), pour la mémoire tampon du nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7e99f-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="7e99f-131">La fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="7e99f-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="7e99f-132">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="7e99f-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7e99f-133">ERREUR \_ de \_ mémoire tampon insuffisante.</span><span class="sxs-lookup"><span data-stu-id="7e99f-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="7e99f-134">La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7e99f-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="7e99f-135">ERREUR \_ : indicateurs non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="7e99f-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="7e99f-136">La valeur de *dwFlags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7e99f-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="7e99f-137">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="7e99f-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7e99f-138">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7e99f-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e99f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="7e99f-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7e99f-140">Cette fonction ne prend pas en charge les [paramètres régionaux personnalisés](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="7e99f-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="7e99f-141">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="7e99f-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e99f-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e99f-142">Requirements</span></span>



| <span data-ttu-id="7e99f-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e99f-143">Requirement</span></span> | <span data-ttu-id="7e99f-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e99f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e99f-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e99f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7e99f-146">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="7e99f-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e99f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7e99f-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e99f-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7e99f-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7e99f-149">Redistributable</span></span><br/>          | <span data-ttu-id="7e99f-150">API de mappage de données de niveau inférieur Microsoft NLS onWindows XP avec SP2 et laterorWindows Vista</span><span class="sxs-lookup"><span data-stu-id="7e99f-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="7e99f-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e99f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e99f-152"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e99f-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="7e99f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7e99f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e99f-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e99f-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7e99f-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e99f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e99f-156">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="7e99f-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7e99f-157">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="7e99f-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7e99f-158">Mappage des données de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="7e99f-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="7e99f-159">**LCIDToLocaleName**</span><span class="sxs-lookup"><span data-stu-id="7e99f-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
