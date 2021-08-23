---
description: un périphérique d’acquisition d’images est représenté dans l’Acquisition d’images Windows (WIA) sous la forme d’une arborescence d’objets d’élément wia (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Utilisation d’objets d’appareil WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f9ec9fd4a3fc4746b1908863ae6afcdcc60b54aa7f9f8f73c769d52ad08688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813479"
---
# <a name="using-wia-device-objects"></a>Utilisation d’objets d’appareil WIA

un périphérique d’acquisition d’images est représenté dans l’Acquisition d’images Windows (WIA) sous la forme d’une arborescence d’objets d’élément wia (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ). En règle générale, la racine de cette arborescence d’éléments représente l’appareil lui-même, tandis que les autres éléments de l’arborescence représentent les images, les régions d’un appareil photo ou les régions d’analyse, pour un scanneur.

Les applications utilisent le gestionnaire d’appareils WIA pour créer et énumérer des appareils WIA. Les sections suivantes expliquent comment créer et utiliser des appareils WIA :

-   [Sélection d’un appareil](-wia-selecting-a-device.md)
-   [Appareils photo WIA](-wia-wia-camera-devices.md)
-   [Appareils de scanneur WIA](-wia-wia-scanner-devices.md)

 

 



