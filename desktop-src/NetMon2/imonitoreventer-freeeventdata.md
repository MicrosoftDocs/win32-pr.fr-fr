---
description: La méthode FreeEventData libère de l’espace alloué pour la structure NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer :: FreeEventData, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517229"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="69c19-103">IMonitorEventer :: FreeEventData, méthode</span><span class="sxs-lookup"><span data-stu-id="69c19-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="69c19-104">La méthode **FreeEventData** libère de l’espace alloué pour la structure [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="69c19-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69c19-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="69c19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c19-107">*pNMEventData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69c19-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c19-108">Adresse de la structure [**NMEVENTDATA**](nmeventdata.md) , dont la mémoire est libérée.</span><span class="sxs-lookup"><span data-stu-id="69c19-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c19-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69c19-109">Return value</span></span>

<span data-ttu-id="69c19-110">Cette méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69c19-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c19-111">Notes</span><span class="sxs-lookup"><span data-stu-id="69c19-111">Remarks</span></span>

<span data-ttu-id="69c19-112">Les analyses appellent cette méthode pour libérer la mémoire qu’elles allouent pour la structure des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="69c19-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="69c19-113">Sachez que bien que le moniteur ait toujours un pointeur vers des chaînes dans une structure [**NMEVENTDATA**](nmeventdata.md) allouée, la mémoire de ces chaînes doit être libérée avant l’appel de la méthode **FreeEventData** .</span><span class="sxs-lookup"><span data-stu-id="69c19-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="69c19-114">Pour plus d’informations sur la façon d’allouer de la mémoire pour une structure [**NMEVENTDATA**](nmeventdata.md) , consultez [**IMonitorEventer :: GetEventData**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="69c19-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69c19-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69c19-115">Requirements</span></span>



| <span data-ttu-id="69c19-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69c19-116">Requirement</span></span> | <span data-ttu-id="69c19-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="69c19-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="69c19-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69c19-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69c19-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69c19-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="69c19-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69c19-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69c19-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69c19-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="69c19-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="69c19-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c19-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c19-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c19-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69c19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c19-125">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="69c19-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="69c19-126">**IMonitorEventer::GetEventData**</span><span class="sxs-lookup"><span data-stu-id="69c19-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="69c19-127">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="69c19-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




