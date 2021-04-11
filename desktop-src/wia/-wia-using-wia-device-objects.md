---
description: Un appareil d’acquisition d’images est représenté dans WIA (Windows Image Acquisition) comme une arborescence hiérarchique d’objets d’élément WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Utilisation d’objets d’appareil WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113271"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="07608-103">Utilisation d’objets d’appareil WIA</span><span class="sxs-lookup"><span data-stu-id="07608-103">Using WIA Device Objects</span></span>

<span data-ttu-id="07608-104">Un appareil d’acquisition d’images est représenté dans WIA (Windows Image Acquisition) comme une arborescence hiérarchique d’objets d’élément WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ).</span><span class="sxs-lookup"><span data-stu-id="07608-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="07608-105">En règle générale, la racine de cette arborescence d’éléments représente l’appareil lui-même, tandis que les autres éléments de l’arborescence représentent les images, les régions d’un appareil photo ou les régions d’analyse, pour un scanneur.</span><span class="sxs-lookup"><span data-stu-id="07608-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="07608-106">Les applications utilisent le gestionnaire d’appareils WIA pour créer et énumérer des appareils WIA.</span><span class="sxs-lookup"><span data-stu-id="07608-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="07608-107">Les sections suivantes expliquent comment créer et utiliser des appareils WIA :</span><span class="sxs-lookup"><span data-stu-id="07608-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="07608-108">Sélection d’un appareil</span><span class="sxs-lookup"><span data-stu-id="07608-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="07608-109">Appareils photo WIA</span><span class="sxs-lookup"><span data-stu-id="07608-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="07608-110">Appareils de scanneur WIA</span><span class="sxs-lookup"><span data-stu-id="07608-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



