---
title: Méthode IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged
description: Appelé lorsque la taille du Bureau à distance a changé.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteDesktopSizeChanged
- Méthode OnRemoteDesktopSizeChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741317"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="1ab79-106">IRemoteDesktopClientEvents :: OnRemoteDesktopSizeChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="1ab79-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="1ab79-107">Appelé lorsque la taille du Bureau à distance a changé.</span><span class="sxs-lookup"><span data-stu-id="1ab79-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab79-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab79-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="1ab79-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ab79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab79-110">*largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab79-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1ab79-111">*hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab79-111">*height* \[in\]</span></span>
<span data-ttu-id="1ab79-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1ab79-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1ab79-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ab79-113">Return value</span></span>

<span data-ttu-id="1ab79-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1ab79-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab79-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ab79-115">Requirements</span></span>



| <span data-ttu-id="1ab79-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ab79-116">Requirement</span></span> | <span data-ttu-id="1ab79-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ab79-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab79-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab79-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ab79-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="1ab79-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab79-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab79-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ab79-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="1ab79-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1ab79-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ab79-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ab79-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1ab79-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1ab79-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ab79-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ab79-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1ab79-126">IID</span><span class="sxs-lookup"><span data-stu-id="1ab79-126">IID</span></span><br/>                      | <span data-ttu-id="1ab79-127">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="1ab79-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ab79-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab79-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab79-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="1ab79-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





