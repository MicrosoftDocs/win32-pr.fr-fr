---
description: La fonction GetFrameStoredLength retourne la longueur du frame.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: GetFrameStoredLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521865"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="75801-103">GetFrameStoredLength fonction)</span><span class="sxs-lookup"><span data-stu-id="75801-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="75801-104">La fonction **GetFrameStoredLength** retourne la longueur du frame.</span><span class="sxs-lookup"><span data-stu-id="75801-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="75801-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75801-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="75801-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75801-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75801-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75801-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75801-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="75801-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75801-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75801-109">Return value</span></span>

<span data-ttu-id="75801-110">Si la fonction réussit, la valeur de retour est la longueur de la trame telle qu’elle est stockée.</span><span class="sxs-lookup"><span data-stu-id="75801-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="75801-111">Si la fonction échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="75801-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="75801-112">Notes</span><span class="sxs-lookup"><span data-stu-id="75801-112">Remarks</span></span>

<span data-ttu-id="75801-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameStoredLength** .</span><span class="sxs-lookup"><span data-stu-id="75801-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75801-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75801-114">Requirements</span></span>



| <span data-ttu-id="75801-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75801-115">Requirement</span></span> | <span data-ttu-id="75801-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="75801-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75801-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75801-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75801-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75801-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75801-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75801-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75801-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75801-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75801-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="75801-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75801-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75801-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="75801-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75801-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="75801-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75801-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="75801-125">DLL</span><span class="sxs-lookup"><span data-stu-id="75801-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75801-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75801-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75801-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75801-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75801-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="75801-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




