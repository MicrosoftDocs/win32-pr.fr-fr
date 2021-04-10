---
description: Utilise des appels séquentiels pour récupérer toutes les chaînes dans les plages spécifiées.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: GetStringsFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950955"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="02929-103">GetStringsFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="02929-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="02929-104">La fonction **GetStringsFromBlob** utilise des appels séquentiels pour récupérer toutes les chaînes dans les plages spécifiées.</span><span class="sxs-lookup"><span data-stu-id="02929-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="02929-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02929-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="02929-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02929-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02929-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02929-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="02929-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="02929-109">*pRequestedOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02929-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-110">Pointeur vers la section propriétaire à partir de laquelle obtenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="02929-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="02929-111">*pRequestedCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02929-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-112">Pointeur vers la section de catégorie à partir de laquelle obtenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="02929-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="02929-113">*pRequestedTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02929-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-114">Pointeur vers la balise pour la chaîne demandée.</span><span class="sxs-lookup"><span data-stu-id="02929-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="02929-115">*ppReturnedOwnerName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02929-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-116">Pointeur vers la variable qui pointe vers l’emplacement où le nom du **propriétaire** sera retourné.</span><span class="sxs-lookup"><span data-stu-id="02929-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="02929-117">*ppReturnedCategoryName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02929-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-118">Pointeur vers la variable qui pointe vers l’emplacement où le nom de la **catégorie** sera retourné.</span><span class="sxs-lookup"><span data-stu-id="02929-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="02929-119">*ppReturnedTagName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02929-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-120">Pointeur vers la variable qui pointe vers l’emplacement où le nom de la **balise** sera retourné.</span><span class="sxs-lookup"><span data-stu-id="02929-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="02929-121">*ppReturnedString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02929-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-122">Pointeur vers la variable qui pointe vers l’emplacement où le nom de la chaîne sera retourné.</span><span class="sxs-lookup"><span data-stu-id="02929-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="02929-123">*pRestartKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02929-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02929-124">Pointeur vers la variable où la clé de redémarrage sera spécifiée et retournée.</span><span class="sxs-lookup"><span data-stu-id="02929-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02929-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02929-125">Return value</span></span>

<span data-ttu-id="02929-126">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="02929-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="02929-127">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique le problème.</span><span class="sxs-lookup"><span data-stu-id="02929-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="02929-128">Si une combinaison spécifiée d’informations de **propriétaire**, de **catégorie** et de **balise** n’existe pas, la valeur de retour est **NMERR l’entrée d' \_ objet BLOB \_ \_ n' \_ \_ existe pas**.</span><span class="sxs-lookup"><span data-stu-id="02929-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="02929-129">Lorsque l’objet BLOB est parcouru entièrement dans les limites initialement spécifiées, la fonction retourne **l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**, et le paramètre *pRestartKey* pointe sur zéro.</span><span class="sxs-lookup"><span data-stu-id="02929-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="02929-130">Notes</span><span class="sxs-lookup"><span data-stu-id="02929-130">Remarks</span></span>

<span data-ttu-id="02929-131">Lors de l’appel initial à la fonction **GetStringsFromBlob** , le paramètre *pRestartKey* pointe vers une variable qui contient la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="02929-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="02929-132">Les paramètres préutilisés ne peuvent être utilisés que *si la clé* de redémarrage est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="02929-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="02929-133">Dans les appels suivants, lorsque *pRestartKey* a une valeur *différente de zéro, les paramètres* prépriss sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="02929-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="02929-134">Lors de l’appel initial, tous les peuvent pointer vers la **valeur null**, qui définit la requête de sorte qu’elle retourne chaque entrée de l’objet BLOB, une par appel suivant.</span><span class="sxs-lookup"><span data-stu-id="02929-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="02929-135">La spécification d’un propriétaire limite les chaînes retournées uniquement à ce propriétaire.</span><span class="sxs-lookup"><span data-stu-id="02929-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="02929-136">Une limitation similaire est vraie pour les catégories et les balises, avec un inconvénient supplémentaire : si une catégorie est spécifiée, un propriétaire doit également être spécifié et, si une balise est spécifiée, une catégorie (et donc un propriétaire) doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="02929-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="02929-137">Lorsque l’appel initial à **GetStringsFromBlob** retourne, *pRestartKey* pointe vers une nouvelle valeur, qui doit être spécifiée lors de l’appel suivant à la fonction pour obtenir la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="02929-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="02929-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02929-138">Requirements</span></span>



| <span data-ttu-id="02929-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02929-139">Requirement</span></span> | <span data-ttu-id="02929-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="02929-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02929-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02929-141">Minimum supported client</span></span><br/> | <span data-ttu-id="02929-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02929-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02929-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02929-143">Minimum supported server</span></span><br/> | <span data-ttu-id="02929-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02929-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02929-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="02929-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="02929-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="02929-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="02929-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02929-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="02929-148"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02929-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="02929-149">DLL</span><span class="sxs-lookup"><span data-stu-id="02929-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02929-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02929-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02929-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02929-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02929-152">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="02929-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="02929-153">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-154">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-155">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-156">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-157">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-158">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-159">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-160">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="02929-161">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="02929-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




