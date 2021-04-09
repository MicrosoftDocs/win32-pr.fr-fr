---
description: Détermine si les paramètres régionaux spécifiés par le nom sont installés ou pris en charge sur le système d’exploitation.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: RtlIsValidLocaleName, fonction (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862453"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="b2bfe-103">RtlIsValidLocaleName fonction)</span><span class="sxs-lookup"><span data-stu-id="b2bfe-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="b2bfe-104">Détermine si les paramètres régionaux spécifiés par le nom sont installés ou pris en charge sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="b2bfe-105">Cette fonction peut être utilisée uniquement dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="b2bfe-106">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b2bfe-107">Les applications doivent utiliser [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b2bfe-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2bfe-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b2bfe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2bfe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2bfe-110">*LocaleName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bfe-111">[Nom des paramètres régionaux](locale-names.md) à valider.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="b2bfe-112">Ce paramètre peut spécifier le nom des [paramètres régionaux personnalisés](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2bfe-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bfe-114">Indicateurs indiquant si les paramètres régionaux neutres sont considérés comme valides.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="b2bfe-115">Actuellement, la seule option définie pour les [paramètres régionaux \_ autorise le \_ neutre](locale-allow-neutral.md).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="b2bfe-116">La valeur par défaut est qu’ils ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2bfe-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2bfe-117">Return value</span></span>

<span data-ttu-id="b2bfe-118">Retourne une valeur différente de zéro en cas de réussite, ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2bfe-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b2bfe-119">Remarks</span></span>

<span data-ttu-id="b2bfe-120">Cette fonction est similaire à [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="b2bfe-121">La seule différence réside dans le fait que si les paramètres régionaux \_ autorisent la \_ neutralité est défini, **RtlIsValidLocaleName** retourne la **valeur true** pour un nom qui correspond à des paramètres régionaux neutres (par exemple, « en »), tandis que [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) retourne **true** uniquement pour des paramètres régionaux spécifiques (tels que « en-US »).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="b2bfe-122">Les paramètres régionaux neutres sont utilisés dans le cadre de la stratégie de chargement des ressources dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="b2bfe-123">Seule une petite classe d’applications hautement spécialisées utilise **RtlIsValidLocaleName** et Set locale \_ autorisent la \_ neutralité, car les paramètres régionaux neutres sont très peu utilisés.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="b2bfe-124">Aucune des fonctions décrites dans [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md) n’accepte les paramètres régionaux neutres en tant qu’entrées.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bfe-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2bfe-125">Requirements</span></span>



| <span data-ttu-id="b2bfe-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2bfe-126">Requirement</span></span> | <span data-ttu-id="b2bfe-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2bfe-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2bfe-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2bfe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b2bfe-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2bfe-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2bfe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b2bfe-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2bfe-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2bfe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2bfe-133"><dt>Ntrtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2bfe-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2bfe-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2bfe-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2bfe-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2bfe-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2bfe-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b2bfe-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2bfe-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2bfe-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2bfe-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2bfe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bfe-139">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="b2bfe-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b2bfe-140">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="b2bfe-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="b2bfe-141">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="b2bfe-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




