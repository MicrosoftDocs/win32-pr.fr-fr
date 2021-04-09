---
description: La méthode MCSVC appelle la méthode OnStatus pour notifier à l’analyse qu’un événement de statut NPP existe. Cette méthode doit être implémentée par l’analyse.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor :: OnStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114146"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="9461b-104">IMonitor :: OnStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="9461b-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="9461b-105">La méthode MCSVC appelle la méthode **OnStatus** pour notifier à l’analyse qu’un événement de statut NPP existe.</span><span class="sxs-lookup"><span data-stu-id="9461b-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="9461b-106">Cette méthode doit être implémentée par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="9461b-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9461b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9461b-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="9461b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9461b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9461b-109">*Événement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9461b-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9461b-110">Structure [d' \_ événement de mise à jour](update-event.md) .</span><span class="sxs-lookup"><span data-stu-id="9461b-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9461b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9461b-111">Return value</span></span>

<span data-ttu-id="9461b-112">Si la méthode réussit, la valeur de retour est \_ OK (ce qui est identique à NOERROR) et MCSVC renvoie la valeur retournée au NPP pour traitement.</span><span class="sxs-lookup"><span data-stu-id="9461b-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="9461b-113">Si la méthode échoue, retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9461b-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="9461b-114">En cas d’erreur, MCSVC renvoie la valeur retournée au NPP pour traitement.</span><span class="sxs-lookup"><span data-stu-id="9461b-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9461b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9461b-115">Requirements</span></span>



| <span data-ttu-id="9461b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9461b-116">Requirement</span></span> | <span data-ttu-id="9461b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9461b-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9461b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9461b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9461b-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9461b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9461b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9461b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9461b-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9461b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9461b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9461b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9461b-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9461b-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




