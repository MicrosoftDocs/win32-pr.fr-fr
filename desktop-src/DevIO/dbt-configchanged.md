---
description: Le système diffuse l' \_ événement de l’appareil DBT CONFIGCHANGED pour indiquer que la configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion. Une application ou un pilote qui stocke des données dans le Registre sous la \_ clé de configuration HKEY Current \_ doit mettre à jour les données.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Événement DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200990"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="65b28-104">\_Événement DBT CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="65b28-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="65b28-105">Le système diffuse l' \_ événement de l’appareil DBT CONFIGCHANGED pour indiquer que la configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="65b28-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="65b28-106">Une application ou un pilote qui stocke des données dans le Registre sous la \_ clé de configuration HKEY Current \_ doit mettre à jour les données.</span><span class="sxs-lookup"><span data-stu-id="65b28-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="65b28-107">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ CONFIGCHANGED et *lParam* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="65b28-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="65b28-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65b28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b28-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="65b28-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="65b28-110">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="65b28-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="65b28-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="65b28-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="65b28-112">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="65b28-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="65b28-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65b28-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65b28-114">Définissez sur DBT \_ CONFIGCHANGED.</span><span class="sxs-lookup"><span data-stu-id="65b28-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="65b28-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65b28-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65b28-116">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="65b28-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b28-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65b28-117">Return value</span></span>

<span data-ttu-id="65b28-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="65b28-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b28-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65b28-119">Requirements</span></span>



| <span data-ttu-id="65b28-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65b28-120">Requirement</span></span> | <span data-ttu-id="65b28-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="65b28-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="65b28-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65b28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65b28-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="65b28-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="65b28-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65b28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65b28-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65b28-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="65b28-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="65b28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b28-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b28-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b28-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65b28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b28-129">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="65b28-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="65b28-130">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="65b28-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="65b28-131">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="65b28-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




