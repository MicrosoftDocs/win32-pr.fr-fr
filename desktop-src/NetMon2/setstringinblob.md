---
description: Définit une chaîne à un emplacement donné au sein d’un objet BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: SetStringInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201580"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="a05ed-103">SetStringInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="a05ed-103">SetStringInBlob function</span></span>

<span data-ttu-id="a05ed-104">La fonction **SetStringInBlob** définit une chaîne à un emplacement donné au sein d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="a05ed-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="a05ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a05ed-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="a05ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a05ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05ed-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05ed-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="a05ed-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a05ed-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05ed-110">Pointeur vers la section **propriétaire** de l’objet BLOB, où la chaîne est définie.</span><span class="sxs-lookup"><span data-stu-id="a05ed-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="a05ed-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05ed-112">Pointeur vers la section de **catégorie** de l’objet BLOB, où la chaîne est définie.</span><span class="sxs-lookup"><span data-stu-id="a05ed-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="a05ed-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05ed-114">Pointeur vers la **balise** de la chaîne demandée.</span><span class="sxs-lookup"><span data-stu-id="a05ed-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="a05ed-115">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05ed-116">Pointeur vers la variable où un pointeur vers la chaîne sera retourné.</span><span class="sxs-lookup"><span data-stu-id="a05ed-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05ed-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a05ed-117">Return value</span></span>

<span data-ttu-id="a05ed-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a05ed-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a05ed-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique le problème.</span><span class="sxs-lookup"><span data-stu-id="a05ed-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="a05ed-120">Si les informations de **propriétaire**, de **catégorie** ou de **balise** spécifiées n’existent pas, la valeur de retour est NMERR l' \_ entrée d’objet BLOB \_ \_ n' \_ \_ existe pas.</span><span class="sxs-lookup"><span data-stu-id="a05ed-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="a05ed-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a05ed-121">Requirements</span></span>



| <span data-ttu-id="a05ed-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a05ed-122">Requirement</span></span> | <span data-ttu-id="a05ed-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a05ed-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a05ed-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a05ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a05ed-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a05ed-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a05ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a05ed-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a05ed-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a05ed-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a05ed-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05ed-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05ed-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a05ed-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a05ed-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a05ed-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a05ed-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a05ed-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a05ed-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a05ed-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a05ed-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05ed-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a05ed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05ed-135">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-136">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-137">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-138">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-139">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-140">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-141">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-142">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="a05ed-143">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="a05ed-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




