---
title: Méthode IRemoteDesktopClientEvents OnStatusChanged (Locationapi. h)
description: Appelé lorsque le contrôle client a mis à jour son état.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnStatusChanged
- Méthode OnStatusChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466750"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="857a1-106">IRemoteDesktopClientEvents :: OnStatusChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="857a1-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="857a1-107">Appelé lorsque le contrôle client a mis à jour son état.</span><span class="sxs-lookup"><span data-stu-id="857a1-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="857a1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="857a1-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="857a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="857a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="857a1-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="857a1-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="857a1-111">Nouveau code d’État.</span><span class="sxs-lookup"><span data-stu-id="857a1-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="857a1-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="857a1-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="857a1-113">Texte du message d’État.</span><span class="sxs-lookup"><span data-stu-id="857a1-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="857a1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="857a1-114">Return value</span></span>

<span data-ttu-id="857a1-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="857a1-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="857a1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="857a1-116">Requirements</span></span>



| <span data-ttu-id="857a1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="857a1-117">Requirement</span></span> | <span data-ttu-id="857a1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="857a1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="857a1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="857a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="857a1-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="857a1-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="857a1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="857a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="857a1-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="857a1-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="857a1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="857a1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="857a1-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="857a1-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="857a1-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="857a1-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="857a1-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857a1-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="857a1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="857a1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857a1-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857a1-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="857a1-129">IID</span><span class="sxs-lookup"><span data-stu-id="857a1-129">IID</span></span><br/>                      | <span data-ttu-id="857a1-130">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="857a1-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="857a1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="857a1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857a1-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="857a1-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





