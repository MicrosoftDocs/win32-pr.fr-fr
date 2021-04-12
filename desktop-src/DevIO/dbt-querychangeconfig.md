---
description: Le système diffuse l’événement de l' \_ appareil DBT QUERYCHANGECONFIG pour demander l’autorisation de modifier la configuration actuelle (ancrer ou détacher). Toute application peut refuser cette demande et annuler la modification.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Événement DBT_QUERYCHANGECONFIG (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523652"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="37897-104">\_Événement DBT QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="37897-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="37897-105">Le système diffuse l’événement de l' \_ appareil DBT QUERYCHANGECONFIG pour demander l’autorisation de modifier la configuration actuelle (ancrer ou détacher).</span><span class="sxs-lookup"><span data-stu-id="37897-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="37897-106">Toute application peut refuser cette demande et annuler la modification.</span><span class="sxs-lookup"><span data-stu-id="37897-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="37897-107">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ QUERYCHANGECONFIG et *lParam* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="37897-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="37897-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37897-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37897-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="37897-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="37897-110">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="37897-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="37897-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="37897-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="37897-112">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="37897-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="37897-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37897-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37897-114">Définissez sur DBT \_ QUERYCHANGECONFIG.</span><span class="sxs-lookup"><span data-stu-id="37897-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="37897-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37897-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37897-116">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="37897-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37897-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37897-117">Return value</span></span>

<span data-ttu-id="37897-118">Retourne la **valeur true** pour accorder l’autorisation de modifier la configuration.</span><span class="sxs-lookup"><span data-stu-id="37897-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="37897-119">Retournez \_ la requête \_ de diffusion Deny pour refuser l’autorisation de modifier la configuration.</span><span class="sxs-lookup"><span data-stu-id="37897-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="37897-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37897-120">Requirements</span></span>



| <span data-ttu-id="37897-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37897-121">Requirement</span></span> | <span data-ttu-id="37897-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="37897-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="37897-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37897-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37897-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37897-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="37897-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37897-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37897-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37897-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="37897-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="37897-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="37897-128"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="37897-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37897-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37897-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37897-130">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="37897-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="37897-131">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="37897-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="37897-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="37897-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




