---
description: WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Appareils photo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201481"
---
# <a name="wia-camera-devices"></a>Appareils photo WIA

WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . L’élément racine, retourné par un appel à la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) de l’acquisition d’images Windows (WIA), est utilisé pour obtenir et définir les informations de l’appareil, pour contrôler l’appareil et pour commencer l’énumération des éléments de périphérique.

> [!Note]  
> WIA ne prend pas en charge les caméras dans Windows Vista ou version ultérieure. Pour ces versions de Windows, utilisez l’API Windows Mobile Device (WPD) décrite dans le kit de développement de pilotes (DDK) Windows pour obtenir des images à partir d’appareils photo.

 

Le diagramme suivant illustre un exemple d’implémentation d’appareil photo. L’élément racine de l’appareil photo comporte trois éléments enfants, deux images et un dossier. Le dossier contient deux éléments enfants, les deux images.

![exemple d’implémentation d’appareil photo](images/wihierar.gif)

 

 



