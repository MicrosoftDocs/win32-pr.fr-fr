---
description: Récupère l’identificateur de paramètres régionaux pour le parent des paramètres régionaux fournis.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: DownlevelGetParentLocaleLCID, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320234"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="4bed9-103">DownlevelGetParentLocaleLCID fonction)</span><span class="sxs-lookup"><span data-stu-id="4bed9-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="4bed9-104">Récupère l' [identificateur de paramètres régionaux](locale-identifiers.md) pour le parent des paramètres régionaux fournis.</span><span class="sxs-lookup"><span data-stu-id="4bed9-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="4bed9-105">Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4bed9-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="4bed9-106">Son utilisation requiert le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4bed9-106">Its use requires the download package.</span></span> <span data-ttu-id="4bed9-107">Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCTYPE* défini sur [locale \_ sParent](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="4bed9-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4bed9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bed9-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="4bed9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bed9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bed9-110">*Paramètres régionaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bed9-111">Identificateur de paramètres régionaux des paramètres régionaux pour lesquels récupérer l’identificateur de paramètres régionaux parent.</span><span class="sxs-lookup"><span data-stu-id="4bed9-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="4bed9-112">Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux ou utiliser l’une des valeurs prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bed9-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="4bed9-113">paramètres régionaux \_ INvariants</span><span class="sxs-lookup"><span data-stu-id="4bed9-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="4bed9-114">paramètres régionaux \_ \_ par défaut du système</span><span class="sxs-lookup"><span data-stu-id="4bed9-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="4bed9-115">paramètres régionaux \_ par défaut de l’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="4bed9-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="4bed9-116">**Windows Vista et versions ultérieures :** Les identificateurs de paramètres régionaux personnalisés suivants sont également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4bed9-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="4bed9-117">paramètres régionaux \_ personnalisés \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="4bed9-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="4bed9-118">paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_</span><span class="sxs-lookup"><span data-stu-id="4bed9-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="4bed9-119">paramètres régionaux \_ personnalisés \_ non spécifiés</span><span class="sxs-lookup"><span data-stu-id="4bed9-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bed9-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bed9-120">Return value</span></span>

<span data-ttu-id="4bed9-121">Retourne l’identificateur de paramètres régionaux parent en cas de réussite, ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4bed9-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="4bed9-122">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="4bed9-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4bed9-123">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4bed9-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4bed9-124">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4bed9-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bed9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4bed9-125">Remarks</span></span>

<span data-ttu-id="4bed9-126">Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="4bed9-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bed9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bed9-127">Requirements</span></span>



| <span data-ttu-id="4bed9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bed9-128">Requirement</span></span> | <span data-ttu-id="4bed9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bed9-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bed9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bed9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4bed9-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4bed9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bed9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4bed9-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bed9-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4bed9-134">Redistributable</span></span><br/>          | <span data-ttu-id="4bed9-135">API de mappage de données de niveau inférieur Microsoft NLS onWindows XPor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bed9-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="4bed9-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bed9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bed9-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bed9-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="4bed9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4bed9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bed9-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bed9-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bed9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bed9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bed9-141">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="4bed9-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4bed9-142">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="4bed9-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4bed9-143">Mappage des données de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="4bed9-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="4bed9-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="4bed9-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
