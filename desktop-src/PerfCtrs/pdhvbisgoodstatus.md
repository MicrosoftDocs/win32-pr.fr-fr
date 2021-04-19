---
description: La fonction PdhVbIsGoodStatus teste une valeur d’État pour déterminer s’il s’agit d’un code de réussite ou d’échec. Si la valeur d’État est une valeur réussie, la valeur de retour est différente de zéro. S’il s’agit d’un code d’état d’échec, la valeur de retour est égale à zéro.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519115"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="1bc12-105">PdhVbIsGoodStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="1bc12-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="1bc12-106">La fonction **PdhVbIsGoodStatus** teste une valeur d’État pour déterminer s’il s’agit d’un code de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="1bc12-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="1bc12-107">Si la valeur d’État est une valeur réussie, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1bc12-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="1bc12-108">S’il s’agit d’un code d’état d’échec, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1bc12-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bc12-109">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1bc12-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="1bc12-110">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1bc12-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="1bc12-111">Function PdhVbIsGoodStatus ( \_ ByVal StatusValue As long \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="1bc12-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="1bc12-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bc12-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc12-113">*StatusValue*</span><span class="sxs-lookup"><span data-stu-id="1bc12-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc12-114">Valeur d’État retournée par une autre fonction PDH qui doit être testée.</span><span class="sxs-lookup"><span data-stu-id="1bc12-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc12-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bc12-115">Return value</span></span>

<span data-ttu-id="1bc12-116">La fonction retourne zéro si le code d’État est un code d’état d’échec.</span><span class="sxs-lookup"><span data-stu-id="1bc12-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="1bc12-117">Elle retourne une valeur différente de zéro si le code d’État est un code d’état de réussite.</span><span class="sxs-lookup"><span data-stu-id="1bc12-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc12-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bc12-118">Requirements</span></span>



| <span data-ttu-id="1bc12-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bc12-119">Requirement</span></span> | <span data-ttu-id="1bc12-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc12-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc12-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc12-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc12-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc12-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bc12-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc12-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc12-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc12-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1bc12-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bc12-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bc12-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc12-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="1bc12-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc12-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc12-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc12-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc12-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc12-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc12-130">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="1bc12-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




