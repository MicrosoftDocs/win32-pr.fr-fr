---
description: Retourne une chaîne située à une position donnée dans un objet BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: GetStringFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484321"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="19afc-103">GetStringFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="19afc-103">GetStringFromBlob function</span></span>

<span data-ttu-id="19afc-104">La fonction **GetStringFromBlob** retourne une chaîne située à une position donnée dans un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="19afc-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="19afc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19afc-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="19afc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19afc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19afc-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19afc-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19afc-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="19afc-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="19afc-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19afc-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19afc-110">Section **propriétaire** de l’objet BLOB dans laquelle se trouve la chaîne.</span><span class="sxs-lookup"><span data-stu-id="19afc-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="19afc-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19afc-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19afc-112">Section de **catégorie** BLOB dans laquelle se trouve la chaîne.</span><span class="sxs-lookup"><span data-stu-id="19afc-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="19afc-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19afc-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19afc-114">**Balise** de la chaîne demandée.</span><span class="sxs-lookup"><span data-stu-id="19afc-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="19afc-115">*ppString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19afc-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19afc-116">Pointeur vers une variable qui pointe vers la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="19afc-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19afc-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19afc-117">Return value</span></span>

<span data-ttu-id="19afc-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="19afc-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="19afc-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="19afc-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="19afc-120">Si le **propriétaire**, la **catégorie** ou les données de **balise** spécifiés n’existent pas, la fonction retourne l' **entrée d' \_ objet BLOB NMERR \_ \_ n' \_ \_ existe pas**.</span><span class="sxs-lookup"><span data-stu-id="19afc-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="19afc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19afc-121">Requirements</span></span>



| <span data-ttu-id="19afc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19afc-122">Requirement</span></span> | <span data-ttu-id="19afc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="19afc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19afc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19afc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19afc-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19afc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="19afc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19afc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19afc-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19afc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19afc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="19afc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19afc-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="19afc-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="19afc-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19afc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="19afc-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19afc-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="19afc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="19afc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19afc-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19afc-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19afc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19afc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19afc-135">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-136">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-137">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-138">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-139">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-140">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-141">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-142">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-143">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="19afc-144">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="19afc-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




