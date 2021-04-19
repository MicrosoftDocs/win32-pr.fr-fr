---
description: La fonction GetFrameLength retourne la longueur du frame.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: GetFrameLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514785"
---
# <a name="getframelength-function"></a><span data-ttu-id="7ab43-103">GetFrameLength fonction)</span><span class="sxs-lookup"><span data-stu-id="7ab43-103">GetFrameLength function</span></span>

<span data-ttu-id="7ab43-104">La fonction **GetFrameLength** retourne la longueur du frame.</span><span class="sxs-lookup"><span data-stu-id="7ab43-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ab43-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7ab43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ab43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab43-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ab43-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab43-108">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="7ab43-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab43-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ab43-109">Return value</span></span>

<span data-ttu-id="7ab43-110">Si la fonction réussit, la valeur de retour est la longueur du frame en octets.</span><span class="sxs-lookup"><span data-stu-id="7ab43-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="7ab43-111">Si la fonction échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="7ab43-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab43-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7ab43-112">Remarks</span></span>

<span data-ttu-id="7ab43-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameLength** .</span><span class="sxs-lookup"><span data-stu-id="7ab43-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab43-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ab43-114">Requirements</span></span>



| <span data-ttu-id="7ab43-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ab43-115">Requirement</span></span> | <span data-ttu-id="7ab43-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ab43-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab43-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ab43-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab43-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ab43-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7ab43-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ab43-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab43-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ab43-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ab43-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ab43-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab43-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab43-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7ab43-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ab43-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ab43-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ab43-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ab43-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ab43-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ab43-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ab43-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




