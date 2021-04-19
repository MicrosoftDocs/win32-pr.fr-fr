---
title: Méthode IMsTscAxEvents OnIdleTimeoutNotification
description: Appelé quand aucune entrée de souris ou de clavier n’a été effectuée par l’utilisateur pendant la période définie par la méthode IMsRdpClientAdvancedSettings put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnIdleTimeoutNotification
- Méthode OnIdleTimeoutNotification Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511370"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="d8a9d-106">IMsTscAxEvents :: OnIdleTimeoutNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="d8a9d-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="d8a9d-107">Appelé quand aucune entrée de souris ou de clavier n’a été effectuée par l’utilisateur pendant la période définie par la méthode [**IMsRdpClientAdvancedSettings ::p ut \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="d8a9d-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a9d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8a9d-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="d8a9d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8a9d-109">Parameters</span></span>

<span data-ttu-id="d8a9d-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8a9d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8a9d-111">Return value</span></span>

<span data-ttu-id="d8a9d-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a9d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d8a9d-113">Remarks</span></span>

<span data-ttu-id="d8a9d-114">Par défaut, la valeur de la propriété [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) est définie sur zéro et le système ne surveille pas les délais d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="d8a9d-115">Cet événement se produit uniquement si la propriété est définie sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="d8a9d-116">La valeur de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) est automatiquement réinitialisée à chaque fois que l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="d8a9d-117">Les applications peuvent utiliser [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) dans les situations où il est utile de déconnecter un utilisateur. par exemple, dans une borne ou un autre scénario de terminal public.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a9d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8a9d-118">Requirements</span></span>



| <span data-ttu-id="d8a9d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8a9d-119">Requirement</span></span> | <span data-ttu-id="d8a9d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8a9d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a9d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8a9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a9d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8a9d-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d8a9d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8a9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a9d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8a9d-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d8a9d-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d8a9d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8a9d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8a9d-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8a9d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d8a9d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8a9d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8a9d-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8a9d-129">IID</span><span class="sxs-lookup"><span data-stu-id="d8a9d-129">IID</span></span><br/>                      | <span data-ttu-id="d8a9d-130">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="d8a9d-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d8a9d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a9d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a9d-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





