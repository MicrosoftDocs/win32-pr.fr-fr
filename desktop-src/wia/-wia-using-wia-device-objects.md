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
# <a name="using-wia-device-objects"></a>Utilisation d’objets d’appareil WIA

Un appareil d’acquisition d’images est représenté dans WIA (Windows Image Acquisition) comme une arborescence hiérarchique d’objets d’élément WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ). En règle générale, la racine de cette arborescence d’éléments représente l’appareil lui-même, tandis que les autres éléments de l’arborescence représentent les images, les régions d’un appareil photo ou les régions d’analyse, pour un scanneur.

Les applications utilisent le gestionnaire d’appareils WIA pour créer et énumérer des appareils WIA. Les sections suivantes expliquent comment créer et utiliser des appareils WIA :

-   [Sélection d’un appareil](-wia-selecting-a-device.md)
-   [Appareils photo WIA](-wia-wia-camera-devices.md)
-   [Appareils de scanneur WIA](-wia-wia-scanner-devices.md)

 

 



