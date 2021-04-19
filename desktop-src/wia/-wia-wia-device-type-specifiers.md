---
description: Les spécificateurs de type d’appareil WIA (Windows Image Acquisition) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Spécificateurs de type d’appareil WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513424"
---
# <a name="wia-device-type-specifiers"></a>Spécificateurs de type d’appareil WIA

Les spécificateurs de type d’appareil WIA (Windows Image Acquisition) sont des constantes qui indiquent le type d’appareil attaché à l’ordinateur d’un utilisateur. Utilisez la macro obtenir le \_ \_ type STIDEVICE pour obtenir ces valeurs à partir de la propriété type d’appareil WIA. Les spécificateurs de type d’appareil WIA valides sont les suivants : 

| Type d’appareil                 | Signification                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Appareil WIA générique. Pendant les énumérations d’appareils, cette constante est utilisée pour énumérer tous les périphériques WIA.                         |
| StiDeviceTypeDigitalCamera  | L’appareil est une caméra. *Ce spécificateur n’est pas pris en charge par* Windows Vista *et versions ultérieures.*                                     |
| StiDeviceTypeScanner        | L’appareil est un scanneur.                                                                                                    |
| StiDeviceTypeStreamingVideo | L’appareil contient une vidéo de diffusion en continu. *Ce spécificateur n’est pas pris en charge par* Windows Server 2003 *,* Windows Vista *ou version ultérieure.* |



 

 

 



