---
description: La méthode OnFrames doit être implémentée par le moniteur. Le MCSVC appelle cette méthode lorsque la mémoire tampon de capture est pleine ou que l’heure de mise à jour est passée.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor :: OnFrames, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751085"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="36e94-104">IMonitor :: OnFrames, méthode</span><span class="sxs-lookup"><span data-stu-id="36e94-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="36e94-105">La méthode **OnFrames** doit être implémentée par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="36e94-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="36e94-106">Le MCSVC appelle cette méthode lorsque la mémoire tampon de capture est pleine ou que l’heure de mise à jour est passée.</span><span class="sxs-lookup"><span data-stu-id="36e94-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e94-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36e94-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="36e94-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36e94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e94-109">*Événement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36e94-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36e94-110">[Mettre à jour \_ ](update-event.md) Structure d’événement qui contient les informations de frame utilisées pour mettre à jour les événements.</span><span class="sxs-lookup"><span data-stu-id="36e94-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e94-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36e94-111">Return value</span></span>

<span data-ttu-id="36e94-112">Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).</span><span class="sxs-lookup"><span data-stu-id="36e94-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="36e94-113">MCSVC renvoie la valeur retournée au NPP pour traitement.</span><span class="sxs-lookup"><span data-stu-id="36e94-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="36e94-114">Si la méthode échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="36e94-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="36e94-115">MCSVC renvoie la valeur retournée au NPP pour traitement.</span><span class="sxs-lookup"><span data-stu-id="36e94-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e94-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36e94-116">Requirements</span></span>



| <span data-ttu-id="36e94-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36e94-117">Requirement</span></span> | <span data-ttu-id="36e94-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="36e94-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36e94-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e94-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36e94-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36e94-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36e94-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e94-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36e94-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36e94-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36e94-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="36e94-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e94-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="36e94-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




