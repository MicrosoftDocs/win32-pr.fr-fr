---
title: Fonctionnalités de l’appareil MCI
description: Fonctionnalités de l’appareil MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig macro)
- MCIWndCanEject macro)
- MCIWndCanPlay macro)
- MCIWndCanRecord macro)
- MCIWndCanSave macro)
- MCIWndCanWindow macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029761"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="d9b30-109">Fonctionnalités de l’appareil MCI</span><span class="sxs-lookup"><span data-stu-id="d9b30-109">MCI Device Capabilities</span></span>

<span data-ttu-id="d9b30-110">MCIWnd comprend les macros suivantes qui vous permettent d’interroger les périphériques MCI pour leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d9b30-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="d9b30-111">Macro</span><span class="sxs-lookup"><span data-stu-id="d9b30-111">Macro</span></span>                                      | <span data-ttu-id="d9b30-112">Description</span><span class="sxs-lookup"><span data-stu-id="d9b30-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9b30-113">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="d9b30-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="d9b30-114">Détermine si un appareil dispose d’une boîte de dialogue de configuration pour prendre en charge plusieurs configurations, telles que le périphérique MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="d9b30-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="d9b30-115">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="d9b30-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="d9b30-116">Détermine si un appareil dispose d’une fonction d’éjection contrôlée par logiciel.</span><span class="sxs-lookup"><span data-stu-id="d9b30-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="d9b30-117">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="d9b30-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="d9b30-118">Détermine si un appareil peut lire le contenu existant.</span><span class="sxs-lookup"><span data-stu-id="d9b30-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="d9b30-119">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="d9b30-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="d9b30-120">Détermine si un appareil peut enregistrer.</span><span class="sxs-lookup"><span data-stu-id="d9b30-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="d9b30-121">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="d9b30-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="d9b30-122">Détermine si un appareil peut stocker des données.</span><span class="sxs-lookup"><span data-stu-id="d9b30-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="d9b30-123">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="d9b30-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="d9b30-124">Détermine si un appareil prend en charge les commandes de fenêtre MCI (telles que [**Window**](window.md), [**put**](put.md) et [**Where**](where.md)).</span><span class="sxs-lookup"><span data-stu-id="d9b30-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="d9b30-125">Ces macros retournent **true** si l’appareil prend en charge la fonctionnalité spécifique, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d9b30-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




