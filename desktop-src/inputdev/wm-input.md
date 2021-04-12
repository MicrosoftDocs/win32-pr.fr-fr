---
title: Message WM_INPUT (winuser. h)
description: Envoyé à la fenêtre qui obtient l’entrée brute. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384420"
---
# <a name="wm_input-message"></a><span data-ttu-id="ebaab-105">\_Message d’entrée WM</span><span class="sxs-lookup"><span data-stu-id="ebaab-105">WM\_INPUT message</span></span>

<span data-ttu-id="ebaab-106">Envoyé à la fenêtre qui obtient l’entrée brute.</span><span class="sxs-lookup"><span data-stu-id="ebaab-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="ebaab-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ebaab-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="ebaab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebaab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebaab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebaab-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="ebaab-110">Code d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ebaab-110">The input code.</span></span> <span data-ttu-id="ebaab-111">Utilisez la macro [**\_ RAWINPUT \_ code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) pour récupérer la valeur.</span><span class="sxs-lookup"><span data-stu-id="ebaab-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="ebaab-112">Peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebaab-112">Can be one of the following values:</span></span>

| <span data-ttu-id="ebaab-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebaab-113">Value</span></span> | <span data-ttu-id="ebaab-114">Signification</span><span class="sxs-lookup"><span data-stu-id="ebaab-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="ebaab-115"><dt>**Bord \_ ENTRÉE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ebaab-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="ebaab-116">Une entrée s’est produite pendant que l’application était au premier plan.</span><span class="sxs-lookup"><span data-stu-id="ebaab-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="ebaab-117">L’application doit appeler [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour que le système puisse effectuer un nettoyage.</span><span class="sxs-lookup"><span data-stu-id="ebaab-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="ebaab-118"><dt>**Bord \_ INPUTSINK**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ebaab-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="ebaab-119">Une entrée s’est produite alors que l’application ne se trouvait pas au premier plan.</span><span class="sxs-lookup"><span data-stu-id="ebaab-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="ebaab-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebaab-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="ebaab-121">Handle **HRAWINPUT** vers la structure [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) qui contient l’entrée brute de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ebaab-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="ebaab-122">Pour récupérer les données brutes, utilisez ce handle dans l’appel à [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span><span class="sxs-lookup"><span data-stu-id="ebaab-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebaab-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebaab-123">Return value</span></span>

<span data-ttu-id="ebaab-124">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ebaab-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebaab-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ebaab-125">Remarks</span></span>

<span data-ttu-id="ebaab-126">Les entrées brutes sont disponibles uniquement quand l’application appelle [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) avec des spécifications de périphérique valides.</span><span class="sxs-lookup"><span data-stu-id="ebaab-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebaab-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebaab-127">Requirements</span></span>

| <span data-ttu-id="ebaab-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebaab-128">Requirement</span></span> | <span data-ttu-id="ebaab-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebaab-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="ebaab-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebaab-130">Minimum supported client</span></span> | <span data-ttu-id="ebaab-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebaab-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="ebaab-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebaab-132">Minimum supported server</span></span> | <span data-ttu-id="ebaab-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebaab-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="ebaab-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebaab-134">Header</span></span> | <dl> <span data-ttu-id="ebaab-135"><dt>**Winuser. h (inclure Windows. h)**</dt></span><span class="sxs-lookup"><span data-stu-id="ebaab-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ebaab-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebaab-136">See also</span></span>

<span data-ttu-id="ebaab-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ebaab-137">**Reference**</span></span>

[<span data-ttu-id="ebaab-138">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="ebaab-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="ebaab-139">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="ebaab-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="ebaab-140">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="ebaab-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="ebaab-141">**Obtient \_ le \_ wParam de code RAWINPUT \_**</span><span class="sxs-lookup"><span data-stu-id="ebaab-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="ebaab-142">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ebaab-142">**Conceptual**</span></span>

[<span data-ttu-id="ebaab-143">Entrée brute</span><span class="sxs-lookup"><span data-stu-id="ebaab-143">Raw Input</span></span>](raw-input.md)
