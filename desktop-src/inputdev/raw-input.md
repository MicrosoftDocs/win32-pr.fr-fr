---
title: Entrée brute
description: Cette section décrit comment le système fournit une entrée brute à votre application et comment une application reçoit et traite cette entrée.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Interface utilisateur Windows, entrée utilisateur
- Interface utilisateur Windows, entrée brute
- entrée d’utilisateur, entrée brute
- capture de l’entrée utilisateur, entrée brute
- entrée brute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381884"
---
# <a name="raw-input"></a><span data-ttu-id="f3108-108">Entrée brute</span><span class="sxs-lookup"><span data-stu-id="f3108-108">Raw Input</span></span>

<span data-ttu-id="f3108-109">Cette section décrit comment le système fournit une entrée brute à votre application et comment une application reçoit et traite cette entrée.</span><span class="sxs-lookup"><span data-stu-id="f3108-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="f3108-110">L’entrée brute est parfois appelée entrée générique.</span><span class="sxs-lookup"><span data-stu-id="f3108-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="f3108-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f3108-111">In This Section</span></span>



| <span data-ttu-id="f3108-112">Nom</span><span class="sxs-lookup"><span data-stu-id="f3108-112">Name</span></span>                                           | <span data-ttu-id="f3108-113">Description</span><span class="sxs-lookup"><span data-stu-id="f3108-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3108-114">À propos des entrées brutes</span><span class="sxs-lookup"><span data-stu-id="f3108-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="f3108-115">Décrit l’entrée utilisateur à partir d’appareils tels que les manettes, les écrans tactiles et les microphones.</span><span class="sxs-lookup"><span data-stu-id="f3108-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="f3108-116">Utilisation des entrées brutes</span><span class="sxs-lookup"><span data-stu-id="f3108-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="f3108-117">Fournit un exemple de code pour les tâches relatives à l’entrée brute.</span><span class="sxs-lookup"><span data-stu-id="f3108-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="f3108-118">Référence d’entrée brute</span><span class="sxs-lookup"><span data-stu-id="f3108-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="f3108-119">Contient la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="f3108-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="f3108-120">Fonctions</span><span class="sxs-lookup"><span data-stu-id="f3108-120">Functions</span></span>



| <span data-ttu-id="f3108-121">Nom</span><span class="sxs-lookup"><span data-stu-id="f3108-121">Name</span></span>                                                                 | <span data-ttu-id="f3108-122">Description</span><span class="sxs-lookup"><span data-stu-id="f3108-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3108-123">**DefRawInputProc**</span><span class="sxs-lookup"><span data-stu-id="f3108-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="f3108-124">Appelle la procédure d’entrée brute par défaut pour fournir le traitement par défaut des messages d’entrée bruts qu’une application ne traite pas.</span><span class="sxs-lookup"><span data-stu-id="f3108-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="f3108-125">Cette fonction garantit que chaque message est traité.</span><span class="sxs-lookup"><span data-stu-id="f3108-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="f3108-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) est appelé avec les mêmes paramètres que ceux reçus par la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3108-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="f3108-127">**GetRawInputBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3108-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="f3108-128">Effectue une lecture en mémoire tampon des données d’entrée brutes.</span><span class="sxs-lookup"><span data-stu-id="f3108-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f3108-129">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="f3108-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="f3108-130">Obtient l’entrée brute du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3108-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f3108-131">**GetRawInputDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="f3108-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="f3108-132">Obtient des informations sur l’appareil d’entrée brut.</span><span class="sxs-lookup"><span data-stu-id="f3108-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f3108-133">**GetRawInputDeviceList**</span><span class="sxs-lookup"><span data-stu-id="f3108-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="f3108-134">Énumère les périphériques d’entrée bruts attachés au système.</span><span class="sxs-lookup"><span data-stu-id="f3108-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f3108-135">**GetRegisteredRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="f3108-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="f3108-136">Obtient les informations sur les périphériques d’entrée bruts pour l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="f3108-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="f3108-137">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="f3108-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="f3108-138">Inscrit les appareils qui fournissent les données d’entrée brutes.</span><span class="sxs-lookup"><span data-stu-id="f3108-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="f3108-139">Macros</span><span class="sxs-lookup"><span data-stu-id="f3108-139">Macros</span></span>



| <span data-ttu-id="f3108-140">Nom</span><span class="sxs-lookup"><span data-stu-id="f3108-140">Name</span></span>                                                            | <span data-ttu-id="f3108-141">Description</span><span class="sxs-lookup"><span data-stu-id="f3108-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3108-142">**Obtient \_ le \_ wParam de code RAWINPUT \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="f3108-143">Obtient le code d’entrée de *wParam* dans l' [**\_ entrée WM**](wm-input.md).</span><span class="sxs-lookup"><span data-stu-id="f3108-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="f3108-144">**NEXTRAWINPUTBLOCK**</span><span class="sxs-lookup"><span data-stu-id="f3108-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="f3108-145">Obtient l’emplacement de la structure suivante dans un tableau de structures [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) .</span><span class="sxs-lookup"><span data-stu-id="f3108-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="f3108-146">Notifications</span><span class="sxs-lookup"><span data-stu-id="f3108-146">Notifications</span></span>



| <span data-ttu-id="f3108-147">Nom</span><span class="sxs-lookup"><span data-stu-id="f3108-147">Name</span></span>                                                        | <span data-ttu-id="f3108-148">Description</span><span class="sxs-lookup"><span data-stu-id="f3108-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="f3108-149">**\_entrée WM**</span><span class="sxs-lookup"><span data-stu-id="f3108-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="f3108-150">Envoyé à la fenêtre qui obtient l’entrée brute.</span><span class="sxs-lookup"><span data-stu-id="f3108-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="f3108-151">**modification de l' \_ appareil d’entrée WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="f3108-152">Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute.</span><span class="sxs-lookup"><span data-stu-id="f3108-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="f3108-153">Structures</span><span class="sxs-lookup"><span data-stu-id="f3108-153">Structures</span></span>



| <span data-ttu-id="f3108-154">Nom</span><span class="sxs-lookup"><span data-stu-id="f3108-154">Name</span></span>                                                            | <span data-ttu-id="f3108-155">Description</span><span class="sxs-lookup"><span data-stu-id="f3108-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3108-156">**RAWHID**</span><span class="sxs-lookup"><span data-stu-id="f3108-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="f3108-157">Décrit le format de l’entrée brute à partir d’un périphérique d’interface utilisateur (HID).</span><span class="sxs-lookup"><span data-stu-id="f3108-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="f3108-158">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="f3108-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="f3108-159">Contient l’entrée brute d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="f3108-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="f3108-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="f3108-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="f3108-161">Définit des informations pour les périphériques d’entrée bruts.</span><span class="sxs-lookup"><span data-stu-id="f3108-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="f3108-162">**RAWINPUTDEVICELIST**</span><span class="sxs-lookup"><span data-stu-id="f3108-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="f3108-163">Contient des informations sur un périphérique d’entrée brut.</span><span class="sxs-lookup"><span data-stu-id="f3108-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="f3108-164">**RAWINPUTHEADER**</span><span class="sxs-lookup"><span data-stu-id="f3108-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="f3108-165">Contient les informations d’en-tête qui font partie des données d’entrée brutes.</span><span class="sxs-lookup"><span data-stu-id="f3108-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="f3108-166">**RAWKEYBOARD**</span><span class="sxs-lookup"><span data-stu-id="f3108-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="f3108-167">Contient des informations sur l’état du clavier.</span><span class="sxs-lookup"><span data-stu-id="f3108-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="f3108-168">**RAWMOUSE**</span><span class="sxs-lookup"><span data-stu-id="f3108-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="f3108-169">Contient des informations sur l’état de la souris.</span><span class="sxs-lookup"><span data-stu-id="f3108-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="f3108-170">**\_informations sur l’appareil RID \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="f3108-171">Définit les données d’entrée brutes provenant de n’importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="f3108-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="f3108-172">**\_ \_ HID informations sur l’appareil RID \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="f3108-173">Définit les données d’entrée brutes provenant du HID spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3108-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="f3108-174">**\_ \_ clavier informations sur l’appareil RID \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="f3108-175">Définit les données d’entrée brutes provenant du clavier spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3108-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="f3108-176">**\_souris d' \_ informations sur l’appareil RID \_**</span><span class="sxs-lookup"><span data-stu-id="f3108-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="f3108-177">Définit les données d’entrée brutes provenant de la souris spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f3108-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

