---
description: Exigences générales pour le développement d’applications
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Configuration générale requise pour le développement d’applications (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203642"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="03b8f-103">Configuration générale requise pour le développement d’applications (API WPD)</span><span class="sxs-lookup"><span data-stu-id="03b8f-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="03b8f-104">Pour créer une application d’appareils mobiles Windows, le kit de [développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads) doit être installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03b8f-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="03b8f-105">Les en-têtes et les bibliothèques nécessaires s’affichent dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="03b8f-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="03b8f-106">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="03b8f-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="03b8f-107">PortableDevice. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-107">PortableDevice.h</span></span>
-   <span data-ttu-id="03b8f-108">PortableDeviceTypes. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="03b8f-109">PortableDeviceApi. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="03b8f-110">Toutes les autres bibliothèques et en-têtes nécessaires à votre application pour utiliser ou afficher des fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="03b8f-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="03b8f-111">Si votre application prend en charge les nouvelles interfaces de services d’appareils, elle inclura également un ou plusieurs des fichiers d’en-tête suivants.</span><span class="sxs-lookup"><span data-stu-id="03b8f-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="03b8f-112">AnchorSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-113">BridgeDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-114">CalendarDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-115">ContactDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-116">DeviceServices. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-116">DeviceServices.h</span></span>
-   <span data-ttu-id="03b8f-117">FullEnumSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-118">HintsDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-119">MessageDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-120">MetadataDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-121">NotesDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-122">RingtoneDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-123">StatusDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-124">SyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="03b8f-125">TaskDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="03b8f-125">TaskDeviceService.h</span></span>

<span data-ttu-id="03b8f-126">Parmi les fichiers de la liste précédente, BridgeDeviceService. h et DeviceService. h sont requis pour presque toutes les applications qui prennent en charge les services d’appareils. les autres fichiers définissent différents types de services d’appareil et sont inclus comme il convient.</span><span class="sxs-lookup"><span data-stu-id="03b8f-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b8f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03b8f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b8f-128">**Appareils mobiles Windows**</span><span class="sxs-lookup"><span data-stu-id="03b8f-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
