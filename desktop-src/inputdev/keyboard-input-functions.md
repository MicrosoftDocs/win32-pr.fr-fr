---
title: Fonctions d’entrée au clavier
description: .
ms.assetid: 731b8209-1ca8-4667-bd39-7bd0cef45380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d034ef3f9c20591200247c312fb3c45521d086
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315101"
---
# <a name="keyboard-input-functions"></a><span data-ttu-id="34a65-103">Fonctions d’entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="34a65-103">Keyboard Input Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34a65-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="34a65-104">In This Section</span></span>

-   [<span data-ttu-id="34a65-105">**ActivateKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="34a65-105">**ActivateKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout)
-   [<span data-ttu-id="34a65-106">**BlockInput**</span><span class="sxs-lookup"><span data-stu-id="34a65-106">**BlockInput**</span></span>](/windows/win32/api/winuser/nf-winuser-blockinput)
-   [<span data-ttu-id="34a65-107">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="34a65-107">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
-   [<span data-ttu-id="34a65-108">**GetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="34a65-108">**GetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-getactivewindow)
-   [<span data-ttu-id="34a65-109">**GetAsyncKeyState**</span><span class="sxs-lookup"><span data-stu-id="34a65-109">**GetAsyncKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getasynckeystate)
-   [<span data-ttu-id="34a65-110">**Focus**</span><span class="sxs-lookup"><span data-stu-id="34a65-110">**GetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-getfocus)
-   [<span data-ttu-id="34a65-111">**GetKBCodePage**</span><span class="sxs-lookup"><span data-stu-id="34a65-111">**GetKBCodePage**</span></span>](/windows/win32/api/winuser/nf-winuser-getkbcodepage)
-   [<span data-ttu-id="34a65-112">**GetKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="34a65-112">**GetKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)
-   [<span data-ttu-id="34a65-113">**GetKeyboardLayoutList**</span><span class="sxs-lookup"><span data-stu-id="34a65-113">**GetKeyboardLayoutList**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist)
-   [<span data-ttu-id="34a65-114">**GetKeyboardLayoutName**</span><span class="sxs-lookup"><span data-stu-id="34a65-114">**GetKeyboardLayoutName**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)
-   [<span data-ttu-id="34a65-115">**GetKeyboardState**</span><span class="sxs-lookup"><span data-stu-id="34a65-115">**GetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardstate)
-   [<span data-ttu-id="34a65-116">**GetKeyboardType**</span><span class="sxs-lookup"><span data-stu-id="34a65-116">**GetKeyboardType**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardtype)
-   [<span data-ttu-id="34a65-117">**GetKeyNameText**</span><span class="sxs-lookup"><span data-stu-id="34a65-117">**GetKeyNameText**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeynametexta)
-   [<span data-ttu-id="34a65-118">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="34a65-118">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
-   [<span data-ttu-id="34a65-119">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="34a65-119">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
-   [<span data-ttu-id="34a65-120">**IsWindowEnabled**</span><span class="sxs-lookup"><span data-stu-id="34a65-120">**IsWindowEnabled**</span></span>](/windows/win32/api/winuser/nf-winuser-iswindowenabled)
-   [<span data-ttu-id="34a65-121">**\_événement keybd**</span><span class="sxs-lookup"><span data-stu-id="34a65-121">**keybd\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-keybd_event)
-   [<span data-ttu-id="34a65-122">**LoadKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="34a65-122">**LoadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)
-   [<span data-ttu-id="34a65-123">**MapVirtualKey**</span><span class="sxs-lookup"><span data-stu-id="34a65-123">**MapVirtualKey**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)
-   [<span data-ttu-id="34a65-124">**MapVirtualKeyEx**</span><span class="sxs-lookup"><span data-stu-id="34a65-124">**MapVirtualKeyEx**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa)
-   [<span data-ttu-id="34a65-125">**OemKeyScan**</span><span class="sxs-lookup"><span data-stu-id="34a65-125">**OemKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-oemkeyscan)
-   [<span data-ttu-id="34a65-126">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="34a65-126">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
-   [<span data-ttu-id="34a65-127">**SendInput**</span><span class="sxs-lookup"><span data-stu-id="34a65-127">**SendInput**</span></span>](/windows/win32/api/winuser/nf-winuser-sendinput)
-   [<span data-ttu-id="34a65-128">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="34a65-128">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
-   [<span data-ttu-id="34a65-129">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="34a65-129">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
-   [<span data-ttu-id="34a65-130">**SetKeyboardState**</span><span class="sxs-lookup"><span data-stu-id="34a65-130">**SetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-setkeyboardstate)
-   [<span data-ttu-id="34a65-131">**ToAscii**</span><span class="sxs-lookup"><span data-stu-id="34a65-131">**ToAscii**</span></span>](/windows/win32/api/winuser/nf-winuser-toascii)
-   [<span data-ttu-id="34a65-132">**ToAsciiEx**</span><span class="sxs-lookup"><span data-stu-id="34a65-132">**ToAsciiEx**</span></span>](/windows/win32/api/winuser/nf-winuser-toasciiex)
-   [<span data-ttu-id="34a65-133">**ToUnicode**</span><span class="sxs-lookup"><span data-stu-id="34a65-133">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)
-   [<span data-ttu-id="34a65-134">**ToUnicodeEx**</span><span class="sxs-lookup"><span data-stu-id="34a65-134">**ToUnicodeEx**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicodeex)
-   [<span data-ttu-id="34a65-135">**UnloadKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="34a65-135">**UnloadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)
-   [<span data-ttu-id="34a65-136">**UnregisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="34a65-136">**UnregisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-unregisterhotkey)
-   [<span data-ttu-id="34a65-137">**VkKeyScan**</span><span class="sxs-lookup"><span data-stu-id="34a65-137">**VkKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscana)
-   [<span data-ttu-id="34a65-138">**VkKeyScanEx**</span><span class="sxs-lookup"><span data-stu-id="34a65-138">**VkKeyScanEx**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscanexa)

 

 