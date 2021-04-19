---
description: 'En savoir plus sur : connexion à un appareil'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Connexion à un appareil
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517865"
---
# <a name="connecting-to-a-device"></a>Connexion à un appareil

> [!Note]  
> Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA). Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

La première étape d’une application ou d’un script qui utilise le modèle de script WIA (Windows Image Acquisition) consiste à créer l’objet [**WIA**](-wia-wia.md) . Cet objet fournit des méthodes pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) et connecter ces objets aux appareils. Il offre également la possibilité d’écouter les événements matériels WIA.

La ligne de code Microsoft Visual Basic Scripting Edition (VBScript) suivante crée l’objet [**WIA**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Après avoir créé l’objet [**WIA**](-wia-wia.md) , utilisez la méthode [**Create**](-wia-iwia-create.md) pour se connecter à un périphérique matériel WIA.

Vous pouvez également utiliser la propriété [**Devices**](-wia-iwia-devices.md) de l’objet [**WIA**](-wia-wia.md) pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) . Énumérez cette collection et utilisez la méthode [**Create**](-wia-iwiadeviceinfo-create.md) pour vous connecter à un appareil.

 

 
