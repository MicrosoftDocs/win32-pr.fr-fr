---
title: Gestion des appareils et des services Bluetooth
description: Deux approches de programmation Bluetooth principales pour la programmation Windows avec l’interface Windows Sockets et la gestion des appareils directement avec les interfaces Bluetooth sans Socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Gestion des appareils et des services Bluetooth
- Appareils et services Bluetooth, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101697"
---
# <a name="managing-bluetooth-devices-and-services"></a>Gestion des appareils et des services Bluetooth

Cette section décrit comment utiliser l’API Bluetooth pour contrôler directement les appareils et les services Bluetooth.

Pour plus d’informations sur l’utilisation de l’interface Windows Sockets pour programmer Bluetooth sur Windows, consultez [prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).

> [!Note]  
> Bluetooth n’empêche pas les fonctionnalités de gestion de l’alimentation d’interrompre les transmissions Bluetooth. Les applications compatibles Bluetooth peuvent analyser les messages d’alimentation pour empêcher une telle interruption. Pour plus d’informations, consultez Utilisation de la [gestion de l’alimentation](/windows/desktop/Power/using-power-management).

 

Cette section contient les rubriques suivantes :

| Section                                                                               | Content                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Sélection d’un périphérique Bluetooth](selecting-a-bluetooth-device.md)                      | Décrit comment sélectionner un appareil Bluetooth.                                   |
| [Messages Bluetooth et WM \_ DEVICECHANGE](bluetooth-and-wm-devicechange-messages.md) | Explique l’interaction entre les messages Bluetooth et **WM \_ DEVICECHANGE** . |



 

 

 