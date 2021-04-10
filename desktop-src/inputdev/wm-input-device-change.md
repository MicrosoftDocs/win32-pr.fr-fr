---
title: Message WM_INPUT_DEVICE_CHANGE (winuser. h)
description: Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104032033"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="5a4c1-105">Message WM_INPUT_DEVICE_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5a4c1-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="5a4c1-106">Description</span><span class="sxs-lookup"><span data-stu-id="5a4c1-106">Description</span></span>

<span data-ttu-id="5a4c1-107">Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="5a4c1-108">Les notifications d’entrée brutes ne sont disponibles qu’une fois que l’application a appelé [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) avec [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) indicateur.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="5a4c1-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5a4c1-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="5a4c1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a4c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a4c1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a4c1-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="5a4c1-112">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-112">Type: **WPARAM**</span></span>

<span data-ttu-id="5a4c1-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="5a4c1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a4c1-114">Value</span></span>                    | <span data-ttu-id="5a4c1-115">Signification</span><span class="sxs-lookup"><span data-stu-id="5a4c1-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="5a4c1-116">**\_arrivée GIDC**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="5a4c1-117">1</span><span class="sxs-lookup"><span data-stu-id="5a4c1-117">1</span></span> | <span data-ttu-id="5a4c1-118">Un nouvel appareil a été ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="5a4c1-119">Vous pouvez appeler [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) pour obtenir plus d’informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="5a4c1-120">**suppression de GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="5a4c1-121">2</span><span class="sxs-lookup"><span data-stu-id="5a4c1-121">2</span></span> | <span data-ttu-id="5a4c1-122">Un appareil a été supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="5a4c1-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a4c1-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="5a4c1-124">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-124">Type: **LPARAM**</span></span>

<span data-ttu-id="5a4c1-125">**Handle** de l’appareil d’entrée brut.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a4c1-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a4c1-126">Return value</span></span>

<span data-ttu-id="5a4c1-127">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5a4c1-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a4c1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a4c1-128">See also</span></span>

<span data-ttu-id="5a4c1-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-129">**Conceptual**</span></span>

[<span data-ttu-id="5a4c1-130">Entrée brute</span><span class="sxs-lookup"><span data-stu-id="5a4c1-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="5a4c1-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5a4c1-131">**Reference**</span></span>

[<span data-ttu-id="5a4c1-132">RegisterRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="5a4c1-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="5a4c1-133">RAWINPUTDEVICE, structure</span><span class="sxs-lookup"><span data-stu-id="5a4c1-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

