---
title: Gestion des appareils et des services Bluetooth
description: Deux approches de programmation Bluetooth principales pour la programmation Windows avec l’interface Windows Sockets et la gestion des appareils directement avec les interfaces Bluetooth sans Socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Gestion des appareils et des services Bluetooth
- Appareils et services Bluetooth, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101697"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="4924e-105">Gestion des appareils et des services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="4924e-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="4924e-106">Cette section décrit comment utiliser l’API Bluetooth pour contrôler directement les appareils et les services Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="4924e-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="4924e-107">Pour plus d’informations sur l’utilisation de l’interface Windows Sockets pour programmer Bluetooth sur Windows, consultez [prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="4924e-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="4924e-108">Bluetooth n’empêche pas les fonctionnalités de gestion de l’alimentation d’interrompre les transmissions Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="4924e-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="4924e-109">Les applications compatibles Bluetooth peuvent analyser les messages d’alimentation pour empêcher une telle interruption.</span><span class="sxs-lookup"><span data-stu-id="4924e-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="4924e-110">Pour plus d’informations, consultez Utilisation de la [gestion de l’alimentation](/windows/desktop/Power/using-power-management).</span><span class="sxs-lookup"><span data-stu-id="4924e-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="4924e-111">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4924e-111">This section contains the following topics.</span></span>

| <span data-ttu-id="4924e-112">Section</span><span class="sxs-lookup"><span data-stu-id="4924e-112">Section</span></span>                                                                               | <span data-ttu-id="4924e-113">Content</span><span class="sxs-lookup"><span data-stu-id="4924e-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="4924e-114">Sélection d’un périphérique Bluetooth</span><span class="sxs-lookup"><span data-stu-id="4924e-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="4924e-115">Décrit comment sélectionner un appareil Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="4924e-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="4924e-116">Messages Bluetooth et WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="4924e-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="4924e-117">Explique l’interaction entre les messages Bluetooth et **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="4924e-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 