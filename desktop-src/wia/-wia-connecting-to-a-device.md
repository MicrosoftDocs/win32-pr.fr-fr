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
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451219"
---
# <a name="connecting-to-a-device"></a>Connexion à un appareil

> [!Note]  
> ce système de script a été remplacé par la couche d’automatisation d’acquisition d’images Windows (WIA). consultez [Windows couche automatisation](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)de l’Acquisition d’images.

 

la première étape d’une application ou d’un script qui utilise le modèle de script d’acquisition d’images Windows (wia) crée l’objet [**WIA**](-wia-wia.md) . Cet objet fournit des méthodes pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) et connecter ces objets aux appareils. Il offre également la possibilité d’écouter les événements matériels WIA.

la ligne de code VBScript (Microsoft Visual Basic scripting Edition) suivante crée l’objet [**Wia**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Après avoir créé l’objet [**WIA**](-wia-wia.md) , utilisez la méthode [**Create**](-wia-iwia-create.md) pour se connecter à un périphérique matériel WIA.

Vous pouvez également utiliser la propriété [**Devices**](-wia-iwia-devices.md) de l’objet [**WIA**](-wia-wia.md) pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) . Énumérez cette collection et utilisez la méthode [**Create**](-wia-iwiadeviceinfo-create.md) pour vous connecter à un appareil.

 

 
