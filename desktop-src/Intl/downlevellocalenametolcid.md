---
description: Convertit un nom de paramètres régionaux en un identificateur de paramètres régionaux qui peut être utilisé pour obtenir des informations à partir du système d’exploitation.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: DownlevelLocaleNameToLCID, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520129"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="7ad99-103">DownlevelLocaleNameToLCID fonction)</span><span class="sxs-lookup"><span data-stu-id="7ad99-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="7ad99-104">Convertit un [nom de paramètres régionaux](locale-names.md) en un [identificateur de paramètres régionaux](locale-identifiers.md) qui peut être utilisé pour obtenir des informations à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7ad99-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="7ad99-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7ad99-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="7ad99-106">Son utilisation requiert un package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="7ad99-106">Its use requires a download package.</span></span> <span data-ttu-id="7ad99-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) pour récupérer un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7ad99-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7ad99-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ad99-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7ad99-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ad99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad99-110">*lpName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad99-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad99-111">Pointeur vers une chaîne se terminant par un caractère null qui représente un [nom de paramètres régionaux](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="7ad99-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad99-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad99-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad99-113">Indicateurs spécifiant le type de nom.</span><span class="sxs-lookup"><span data-stu-id="7ad99-113">Flags specifying the type of name.</span></span> <span data-ttu-id="7ad99-114">La valeur par défaut est le nom des paramètres régionaux de niveau inférieur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7ad99-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad99-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ad99-115">Return value</span></span>

<span data-ttu-id="7ad99-116">Retourne l’identificateur de paramètres régionaux qui correspond au nom des paramètres régionaux en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="7ad99-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="7ad99-117">La fonction retourne 0 si elle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="7ad99-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="7ad99-118">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="7ad99-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7ad99-119">ERREUR \_ : indicateurs non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="7ad99-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="7ad99-120">Les valeurs fournies pour les indicateurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7ad99-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="7ad99-121">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="7ad99-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7ad99-122">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7ad99-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad99-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7ad99-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ad99-124">Cette fonction ne prend pas en charge les paramètres régionaux neutres.</span><span class="sxs-lookup"><span data-stu-id="7ad99-124">This function does not support neutral locales.</span></span> <span data-ttu-id="7ad99-125">La fonction [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) équivalente prend en charge les [paramètres régionaux personnalisés](custom-locales.md), mais uniquement pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7ad99-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="7ad99-126">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="7ad99-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad99-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ad99-127">Requirements</span></span>



| <span data-ttu-id="7ad99-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ad99-128">Requirement</span></span> | <span data-ttu-id="7ad99-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ad99-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad99-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad99-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad99-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ad99-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="7ad99-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad99-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad99-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ad99-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ad99-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7ad99-134">Redistributable</span></span><br/>          | <span data-ttu-id="7ad99-135">API de mappage de données de niveau inférieur Microsoft NLS onWindows XP avec SP2 et laterorWindows Vista</span><span class="sxs-lookup"><span data-stu-id="7ad99-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="7ad99-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ad99-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ad99-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad99-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="7ad99-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7ad99-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ad99-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ad99-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7ad99-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ad99-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad99-141">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="7ad99-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7ad99-142">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="7ad99-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7ad99-143">Mappage des données de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="7ad99-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="7ad99-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="7ad99-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
