---
description: La fonction GetFrameNumber retourne le numéro d’un cadre.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: GetFrameNumber, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950964"
---
# <a name="getframenumber-function"></a><span data-ttu-id="0f644-103">GetFrameNumber fonction)</span><span class="sxs-lookup"><span data-stu-id="0f644-103">GetFrameNumber function</span></span>

<span data-ttu-id="0f644-104">La fonction **GetFrameNumber** retourne le numéro d’un cadre.</span><span class="sxs-lookup"><span data-stu-id="0f644-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f644-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f644-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0f644-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f644-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f644-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f644-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f644-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="0f644-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f644-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f644-109">Return value</span></span>

<span data-ttu-id="0f644-110">Si la fonction réussit, la valeur de retour est un numéro de frame de base zéro.</span><span class="sxs-lookup"><span data-stu-id="0f644-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="0f644-111">Si la fonction échoue, la valeur de retour est moins un (-1).</span><span class="sxs-lookup"><span data-stu-id="0f644-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f644-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0f644-112">Remarks</span></span>

<span data-ttu-id="0f644-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameNumber** .</span><span class="sxs-lookup"><span data-stu-id="0f644-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f644-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f644-114">Requirements</span></span>



| <span data-ttu-id="0f644-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f644-115">Requirement</span></span> | <span data-ttu-id="0f644-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f644-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f644-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f644-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f644-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f644-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0f644-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f644-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f644-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f644-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f644-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f644-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f644-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f644-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0f644-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f644-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f644-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f644-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f644-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f644-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f644-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f644-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




