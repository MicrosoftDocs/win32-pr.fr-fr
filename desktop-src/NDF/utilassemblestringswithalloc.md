---
title: UtilAssembleStringsWithAlloc, fonction (Ndattributils. h)
description: Alloue une chaîne et la met en forme à l’aide de chaînes fournies par la table de chaînes. Cette fonction utilise StringCchPrintf pour créer la chaîne mise en forme.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743884"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="abb04-105">UtilAssembleStringsWithAlloc fonction)</span><span class="sxs-lookup"><span data-stu-id="abb04-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="abb04-106">La fonction **UtilAssembleStringsWithAlloc** alloue une chaîne et la met en forme à l’aide de chaînes fournies par la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="abb04-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="abb04-107">Cette fonction utilise [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) pour créer la chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="abb04-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abb04-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="abb04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abb04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb04-110">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="abb04-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-111">Tapez : \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="abb04-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="abb04-112">Emplacement où la chaîne qui vient d’être allouée sera placée.</span><span class="sxs-lookup"><span data-stu-id="abb04-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="abb04-113">Lorsque la chaîne n’est plus nécessaire, elle doit être libérée avec [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="abb04-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="abb04-114">*BufferMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abb04-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-115">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="abb04-115">Type: **UINT**</span></span>

<span data-ttu-id="abb04-116">Nombre maximal de caractères autorisés dans la chaîne allouée par *buffer*.</span><span class="sxs-lookup"><span data-stu-id="abb04-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="abb04-117">Si la chaîne mise en forme obtenue est plus longue que le nombre de caractères spécifié, elle est tronquée et se termine par null.</span><span class="sxs-lookup"><span data-stu-id="abb04-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="abb04-118">Ce paramètre ne peut pas être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="abb04-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="abb04-119">*InputFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abb04-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-120">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="abb04-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="abb04-121">Ressource de type chaîne de la table de chaînes représentant un paramètre de format passé à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span><span class="sxs-lookup"><span data-stu-id="abb04-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="abb04-122">Il est construit à l’aide de [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="abb04-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="abb04-123">Le format de chaîne de ressource doit spécifier un paramètre de format acceptant une chaîne étendue, ou un paramètre de format qui accepte un entier long non signé et une chaîne étendue.</span><span class="sxs-lookup"><span data-stu-id="abb04-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="abb04-124">*InputString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abb04-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-125">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="abb04-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="abb04-126">Ressource de chaîne provenant de la table de chaînes qui représente un argument passé à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) à la place de la chaîne étendue dans le paramètre de format.</span><span class="sxs-lookup"><span data-stu-id="abb04-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="abb04-127">Il est construit à l’aide de [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="abb04-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="abb04-128">*AdditionalArgument* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abb04-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-129">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abb04-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="abb04-130">True si *AdditionalValue* doit être passé en tant que premier argument de mise en forme à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); Sinon, false (et seule la chaîne de ressource identifiée par *InputString* sera passée).</span><span class="sxs-lookup"><span data-stu-id="abb04-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="abb04-131">*AdditionalValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abb04-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb04-132">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="abb04-132">Type: **ULONG**</span></span>

<span data-ttu-id="abb04-133">Valeur à passer comme premier argument de mise en forme à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) si *AdditionalArgument* a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="abb04-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb04-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abb04-134">Return value</span></span>

<span data-ttu-id="abb04-135">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="abb04-135">Type: **HRESULT**</span></span>

<span data-ttu-id="abb04-136">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="abb04-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="abb04-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="abb04-137">Return code</span></span>                                                                                  | <span data-ttu-id="abb04-138">Description</span><span class="sxs-lookup"><span data-stu-id="abb04-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="abb04-139"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abb04-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="abb04-140">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="abb04-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="abb04-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="abb04-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="abb04-142">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="abb04-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="abb04-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abb04-143">Requirements</span></span>



| <span data-ttu-id="abb04-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abb04-144">Requirement</span></span> | <span data-ttu-id="abb04-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="abb04-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb04-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abb04-146">Minimum supported client</span></span><br/> | <span data-ttu-id="abb04-147">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abb04-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="abb04-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abb04-148">Minimum supported server</span></span><br/> | <span data-ttu-id="abb04-149">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abb04-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="abb04-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="abb04-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb04-151"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb04-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb04-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abb04-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb04-153">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="abb04-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="abb04-154">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="abb04-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="abb04-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="abb04-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="abb04-156">**MAKEINTRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="abb04-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="abb04-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="abb04-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

