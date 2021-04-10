---
description: La fonction GetFrameRecognizeData retourne une table de structures RECOGNIZEDATA. Chacune de ces structures contient un identificateur de protocole et un décalage qui pointe vers le début du protocole spécifié dans les données.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: GetFrameRecognizeData, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950963"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="8bb9c-104">GetFrameRecognizeData fonction)</span><span class="sxs-lookup"><span data-stu-id="8bb9c-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="8bb9c-105">La fonction **GetFrameRecognizeData** retourne une table de structures **RECOGNIZEDATA** .</span><span class="sxs-lookup"><span data-stu-id="8bb9c-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="8bb9c-106">Chacune de ces structures contient un identificateur de protocole et un décalage qui pointe vers le début du protocole spécifié dans les données.</span><span class="sxs-lookup"><span data-stu-id="8bb9c-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb9c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bb9c-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8bb9c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bb9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb9c-109">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8bb9c-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb9c-110">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="8bb9c-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb9c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8bb9c-111">Return value</span></span>

<span data-ttu-id="8bb9c-112">Si la fonction réussit, la valeur de retour est un pointeur vers une structure **RECOGNIZEDATATABLE** .</span><span class="sxs-lookup"><span data-stu-id="8bb9c-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="8bb9c-113">Si la fonction échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="8bb9c-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb9c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8bb9c-114">Remarks</span></span>

<span data-ttu-id="8bb9c-115">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameRecognizeData** .</span><span class="sxs-lookup"><span data-stu-id="8bb9c-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb9c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bb9c-116">Requirements</span></span>



| <span data-ttu-id="8bb9c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bb9c-117">Requirement</span></span> | <span data-ttu-id="8bb9c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bb9c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb9c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb9c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb9c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8bb9c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb9c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb9c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8bb9c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bb9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb9c-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb9c-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8bb9c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8bb9c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bb9c-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bb9c-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8bb9c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb9c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bb9c-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bb9c-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




