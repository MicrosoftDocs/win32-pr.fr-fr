---
title: gestion des appareils et des Services Bluetooth
description: deux approches principales de la programmation de la Bluetooth pour Windows la programmation avec l’interface Windows sockets et la gestion des appareils directement avec les interfaces de Bluetooth sans socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- gestion des appareils et des Services Bluetooth
- Bluetooth Appareils et services, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74979fe0a604204e777f0daabe07a4531d9974c9fef55231ce98b7ee7fe9c3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959178"
---
# <a name="managing-bluetooth-devices-and-services"></a>gestion des appareils et des Services Bluetooth

cette section décrit comment utiliser l’API Bluetooth pour contrôler directement Bluetooth appareils et services.

pour plus d’informations sur l’utilisation de l’interface Windows sockets pour programmer Bluetooth sur Windows, consultez [prise en charge des sockets Windows pour Bluetooth](windows-sockets-support-for-bluetooth.md).

> [!Note]  
> Bluetooth n’empêche pas les fonctionnalités de gestion de l’alimentation d’interrompre Bluetooth transmission. les applications compatibles Bluetooth peuvent analyser les messages d’alimentation pour empêcher une telle interruption. Pour plus d’informations, consultez Utilisation de la [gestion de l’alimentation](/windows/desktop/Power/using-power-management).

 

Cette section contient les rubriques suivantes :

| Section                                                                               | Content                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [sélection d’un appareil Bluetooth](selecting-a-bluetooth-device.md)                      | décrit comment sélectionner un appareil Bluetooth.                                   |
| [Messages Bluetooth et WM \_ DEVICECHANGE](bluetooth-and-wm-devicechange-messages.md) | explique l’interaction entre les Bluetooth et les messages **WM \_ DEVICECHANGE** . |



 

 

 