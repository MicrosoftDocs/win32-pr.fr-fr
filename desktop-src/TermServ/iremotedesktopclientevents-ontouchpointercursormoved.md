---
title: Méthode IRemoteDesktopClientEvents OnTouchPointerCursorMoved
description: Appelé lorsque le curseur tactile a été déplacé et que la propriété EventsEnabled a la valeur true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnTouchPointerCursorMoved
- Méthode OnTouchPointerCursorMoved Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnTouchPointerCursorMoved
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536909"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="ad7b1-106">IRemoteDesktopClientEvents :: OnTouchPointerCursorMoved, méthode</span><span class="sxs-lookup"><span data-stu-id="ad7b1-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="ad7b1-107">Appelé lorsque le curseur tactile a été déplacé et que la propriété [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="ad7b1-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad7b1-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="ad7b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad7b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7b1-110">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad7b1-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="ad7b1-111">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad7b1-111">*y* \[in\]</span></span>
<span data-ttu-id="ad7b1-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ad7b1-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ad7b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad7b1-113">Return value</span></span>

<span data-ttu-id="ad7b1-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ad7b1-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7b1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad7b1-115">Requirements</span></span>



| <span data-ttu-id="ad7b1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad7b1-116">Requirement</span></span> | <span data-ttu-id="ad7b1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad7b1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7b1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7b1-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad7b1-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="ad7b1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7b1-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad7b1-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="ad7b1-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ad7b1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad7b1-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad7b1-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ad7b1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ad7b1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad7b1-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad7b1-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ad7b1-126">IID</span><span class="sxs-lookup"><span data-stu-id="ad7b1-126">IID</span></span><br/>                      | <span data-ttu-id="ad7b1-127">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="ad7b1-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad7b1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad7b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7b1-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="ad7b1-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

