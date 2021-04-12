---
title: Méthode IRemoteDesktopClientEvents OnKeyCombinationPressed
description: Appelé lorsque des combinaisons de touches spéciales sont activées dans la session à distance.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnKeyCombinationPressed
- Méthode OnKeyCombinationPressed Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384291"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="c3372-106">IRemoteDesktopClientEvents :: OnKeyCombinationPressed, méthode</span><span class="sxs-lookup"><span data-stu-id="c3372-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="c3372-107">Appelé lorsque des combinaisons de touches spéciales sont activées dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="c3372-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3372-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3372-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="c3372-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3372-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3372-110">*combinaison de touches* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3372-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="c3372-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c3372-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="c3372-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3372-112">Return value</span></span>

<span data-ttu-id="c3372-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c3372-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3372-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3372-114">Requirements</span></span>



| <span data-ttu-id="c3372-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3372-115">Requirement</span></span> | <span data-ttu-id="c3372-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3372-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3372-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3372-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3372-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3372-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="c3372-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3372-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3372-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3372-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="c3372-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c3372-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3372-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3372-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c3372-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3372-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3372-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3372-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c3372-125">IID</span><span class="sxs-lookup"><span data-stu-id="c3372-125">IID</span></span><br/>                      | <span data-ttu-id="c3372-126">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="c3372-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3372-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3372-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3372-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="c3372-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





