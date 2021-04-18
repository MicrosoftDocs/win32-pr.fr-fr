---
description: La méthode SendNMEvent soumet des événements à Windows Management Instrumentation (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer :: SendNMEvent, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519775"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="c5640-103">IMonitorEventer :: SendNMEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="c5640-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="c5640-104">La méthode **SendNMEvent** soumet des événements à Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c5640-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5640-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5640-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="c5640-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5640-107">*pNMEventData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5640-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5640-108">Pointeur vers l’événement soumis à WMI.</span><span class="sxs-lookup"><span data-stu-id="c5640-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5640-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5640-109">Return value</span></span>

<span data-ttu-id="c5640-110">Si la méthode réussit, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5640-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="c5640-111">Si la méthode échoue, la valeur de retour est NMERR à une \_ mémoire insuffisante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5640-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5640-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5640-112">Requirements</span></span>



| <span data-ttu-id="c5640-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5640-113">Requirement</span></span> | <span data-ttu-id="c5640-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5640-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5640-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5640-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5640-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5640-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c5640-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5640-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5640-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5640-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c5640-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5640-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5640-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5640-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




