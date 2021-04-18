---
title: Méthode IRemoteDesktopClientEvents OnAdminMessageReceived
description: Appelé lorsque le contrôle client reçoit un message d’administration.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAdminMessageReceived
- Méthode OnAdminMessageReceived Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnAdminMessageReceived
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384976"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="e2e6e-106">IRemoteDesktopClientEvents :: OnAdminMessageReceived, méthode</span><span class="sxs-lookup"><span data-stu-id="e2e6e-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="e2e6e-107">Appelé lorsque le contrôle client reçoit un message d’administration.</span><span class="sxs-lookup"><span data-stu-id="e2e6e-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e6e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2e6e-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="e2e6e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2e6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e6e-110">*adminMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2e6e-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e6e-111">Message.</span><span class="sxs-lookup"><span data-stu-id="e2e6e-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e6e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2e6e-112">Return value</span></span>

<span data-ttu-id="e2e6e-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e2e6e-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e6e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e6e-114">Requirements</span></span>



| <span data-ttu-id="e2e6e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e6e-115">Requirement</span></span> | <span data-ttu-id="e2e6e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e6e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e6e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e6e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e2e6e-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="e2e6e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e6e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2e6e-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="e2e6e-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e2e6e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2e6e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e6e-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e2e6e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e6e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2e6e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e6e-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e2e6e-125">IID</span><span class="sxs-lookup"><span data-stu-id="e2e6e-125">IID</span></span><br/>                      | <span data-ttu-id="e2e6e-126">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="e2e6e-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2e6e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e6e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e6e-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="e2e6e-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





