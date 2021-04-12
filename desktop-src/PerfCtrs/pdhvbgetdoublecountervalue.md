---
description: La fonction PdhVbGetDoubleCounterValue retourne la valeur actuelle du compteur spécifié sous la forme d’une valeur à virgule flottante double précision.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319181"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="39aef-103">PdhVbGetDoubleCounterValue fonction)</span><span class="sxs-lookup"><span data-stu-id="39aef-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="39aef-104">La fonction **PdhVbGetDoubleCounterValue** retourne la valeur actuelle du compteur spécifié sous la forme d’une valeur à virgule flottante double précision.</span><span class="sxs-lookup"><span data-stu-id="39aef-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="39aef-105">Vous devez vérifier *CounterStatus* avant d’utiliser le nombre retourné, car le compteur peut ne pas être valide lorsqu’il est lu.</span><span class="sxs-lookup"><span data-stu-id="39aef-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="39aef-106">Pour vérifier l’état du compteur, appelez la fonction [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="39aef-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39aef-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="39aef-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="39aef-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="39aef-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="39aef-109">Function PdhVbGetDoubleCounterValue ( \_ ByVal CounterHandle As long, \_ ByVal CounterStatus As long \_ ) As Double</span><span class="sxs-lookup"><span data-stu-id="39aef-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="39aef-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39aef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39aef-111">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="39aef-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="39aef-112">ID du compteur dont la valeur actuelle doit être lue.</span><span class="sxs-lookup"><span data-stu-id="39aef-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="39aef-113">*CounterStatus*</span><span class="sxs-lookup"><span data-stu-id="39aef-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="39aef-114">Variable dans laquelle l’état actuel de la valeur de compteur est retourné à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="39aef-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="39aef-115">La valeur de données renvoyée est valide si et seulement si la valeur retournée dans CounterStatus est PDH \_ CSTATUS \_ Valid \_ Data ou PDH \_ CSTATUS \_ New \_ Data (voir les codes d’erreur PDH).</span><span class="sxs-lookup"><span data-stu-id="39aef-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="39aef-116">Si la valeur retournée dans CounterStatus est toute autre valeur, n’utilisez pas les données.</span><span class="sxs-lookup"><span data-stu-id="39aef-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39aef-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39aef-117">Return value</span></span>

<span data-ttu-id="39aef-118">La fonction retourne la valeur à virgule flottante double précision du compteur actuel, calculée et mise en forme comme défini par le type de compteur.</span><span class="sxs-lookup"><span data-stu-id="39aef-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="39aef-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39aef-119">Requirements</span></span>



| <span data-ttu-id="39aef-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39aef-120">Requirement</span></span> | <span data-ttu-id="39aef-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="39aef-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39aef-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39aef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="39aef-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39aef-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39aef-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39aef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="39aef-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39aef-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39aef-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39aef-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="39aef-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39aef-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="39aef-128">DLL</span><span class="sxs-lookup"><span data-stu-id="39aef-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39aef-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39aef-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39aef-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39aef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39aef-131">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="39aef-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




