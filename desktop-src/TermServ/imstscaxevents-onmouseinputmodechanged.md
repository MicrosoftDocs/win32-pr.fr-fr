---
title: Méthode IMsTscAxEvents OnMouseInputModeChanged
description: Appelé lorsque le mode d’entrée de la souris a changé.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnMouseInputModeChanged
- Méthode OnMouseInputModeChanged Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104320"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="b76ef-106">IMsTscAxEvents :: OnMouseInputModeChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="b76ef-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="b76ef-107">Appelé lorsque le mode d’entrée de la souris a changé.</span><span class="sxs-lookup"><span data-stu-id="b76ef-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b76ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b76ef-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="b76ef-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b76ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b76ef-110">*fMouseModeRelative* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b76ef-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b76ef-111">Indique si la souris est en mode relatif.</span><span class="sxs-lookup"><span data-stu-id="b76ef-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b76ef-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b76ef-112">Return value</span></span>

<span data-ttu-id="b76ef-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b76ef-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b76ef-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b76ef-114">Remarks</span></span>

<span data-ttu-id="b76ef-115">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le mode de saisie de la souris a changé.</span><span class="sxs-lookup"><span data-stu-id="b76ef-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b76ef-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b76ef-116">Requirements</span></span>



| <span data-ttu-id="b76ef-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b76ef-117">Requirement</span></span> | <span data-ttu-id="b76ef-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b76ef-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b76ef-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b76ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b76ef-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b76ef-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b76ef-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b76ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b76ef-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b76ef-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b76ef-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b76ef-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b76ef-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b76ef-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b76ef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b76ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b76ef-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b76ef-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b76ef-127">IID</span><span class="sxs-lookup"><span data-stu-id="b76ef-127">IID</span></span><br/>                      | <span data-ttu-id="b76ef-128">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b76ef-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b76ef-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b76ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76ef-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="b76ef-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





