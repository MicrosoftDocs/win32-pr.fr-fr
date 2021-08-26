---
description: Windows Les spécificateurs de type d’appareil d’acquisition d’images (WIA) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Spécificateurs de type d’appareil WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056969"
---
# <a name="wia-device-type-specifiers"></a>Spécificateurs de type d’appareil WIA

Windows Les spécificateurs de type d’appareil d’acquisition d’images (WIA) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur. Utilisez la macro obtenir le \_ \_ type STIDEVICE pour obtenir ces valeurs à partir de la propriété type d’appareil WIA. Les spécificateurs de type d’appareil WIA valides sont les suivants : 

| Type d’appareil                 | Signification                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Appareil WIA générique. Pendant les énumérations d’appareils, cette constante est utilisée pour énumérer tous les périphériques WIA.                         |
| StiDeviceTypeDigitalCamera  | L’appareil est une caméra. *ce spécificateur n’est pas pris en charge par* Windows Vista *et versions ultérieures.*                                     |
| StiDeviceTypeScanner        | L’appareil est un scanneur.                                                                                                    |
| StiDeviceTypeStreamingVideo | L’appareil contient une vidéo de diffusion en continu. *ce spécificateur n’est pas pris en charge par* Windows Server 2003 *,* Windows Vista *ou version ultérieure.* |



 

 

 



