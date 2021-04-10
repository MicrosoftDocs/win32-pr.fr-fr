---
description: Les fonctions suivantes sont utilisées dans la gestion des périphériques.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Fonctions de gestion des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950582"
---
# <a name="device-management-functions"></a><span data-ttu-id="e4a8b-103">Fonctions de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="e4a8b-103">Device Management Functions</span></span>

<span data-ttu-id="e4a8b-104">Les fonctions suivantes sont utilisées dans la gestion des périphériques.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="e4a8b-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="e4a8b-105">Function</span></span>                                                             | <span data-ttu-id="e4a8b-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4a8b-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4a8b-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="e4a8b-108">Envoie un code de contrôle directement à un pilote de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="e4a8b-109">**InstallNewDevice**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="e4a8b-110">Installe un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-110">Installs a new device.</span></span> <span data-ttu-id="e4a8b-111">L’utilisateur est invité à sélectionner l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="e4a8b-112">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="e4a8b-113">Inscrit l’appareil ou le type d’appareil pour lequel une fenêtre recevra des notifications.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="e4a8b-114">**UnregisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="e4a8b-115">Ferme le handle de notification de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="e4a8b-116">Les fonctions suivantes sont utilisées avec les lecteurs de CD-ROM et de DVD.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="e4a8b-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="e4a8b-117">Function</span></span>                                                               | <span data-ttu-id="e4a8b-118">Description</span><span class="sxs-lookup"><span data-stu-id="e4a8b-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4a8b-119">**CdromDisableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="e4a8b-120">Désactive la lecture numérique pour le lecteur de CD-ROM ou de DVD spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="e4a8b-121">**CdromEnableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="e4a8b-122">Active la lecture numérique pour le lecteur de CD-ROM ou de DVD spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="e4a8b-123">**CdromIsDigitalPlaybackEnabled**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="e4a8b-124">Détermine si la lecture numérique est activée pour le lecteur de CD-ROM ou de DVD spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="e4a8b-125">**CdromKnownGoodDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="e4a8b-126">Détermine si le lecteur de CD-ROM ou de DVD spécifié a une lecture numérique reconnue comme correcte.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="e4a8b-127">**DvdLauncher**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="e4a8b-128">Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
