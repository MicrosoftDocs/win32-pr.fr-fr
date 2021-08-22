---
description: WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Appareils photo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592722"
---
# <a name="wia-camera-devices"></a>Appareils photo WIA

WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . l’élément racine, retourné par un appel à la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) de Windows l’Acquisition d’images (WIA), est utilisé pour obtenir et définir les informations de l’appareil, pour contrôler l’appareil et pour commencer l’énumération des éléments de périphérique.

> [!Note]  
> WIA ne prend pas en charge les caméras dans Windows Vista ou version ultérieure. pour ces versions du Windows, utilisez l’API de l’appareil Portable Windows (WPD) décrite dans le kit de développement de pilotes (DDK) Windows pour obtenir des images à partir d’appareils photo.

 

Le diagramme suivant illustre un exemple d’implémentation d’appareil photo. L’élément racine de l’appareil photo comporte trois éléments enfants, deux images et un dossier. Le dossier contient deux éléments enfants, les deux images.

![exemple d’implémentation d’appareil photo](images/wihierar.gif)

 

 



