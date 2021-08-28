---
description: Une collection est un objet qui contient un ou plusieurs objets. Les collections offrent un moyen efficace de regrouper des objets similaires. Windows L’acquisition d’images (WIA) fournit des collections pour les objets DeviceInfo et Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Utilisation d’objets de collection WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 58a4003394bcc163e9013914da6797a504ec16582b8bfac7915d7a49947c18f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813509"
---
# <a name="using-wia-collection-objects"></a>Utilisation d’objets de collection WIA

Une collection est un objet qui contient un ou plusieurs objets. Les collections offrent un moyen efficace de regrouper des objets similaires. Windows L’acquisition d’images (WIA) fournit des collections pour les objets [**DeviceInfo**](-wia-deviceinfo.md) et [**Item**](-wia-item.md) .

Utilisez des collections pour énumérer les objets qu’ils contiennent. Par exemple, l’exemple VBScript suivant obtient une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) à partir de la méthode [**Devices**](-wia-iwia-devices.md) , puis utilise une **pour... Chaque** boucle pour itérer au sein de la collection :


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> Les objets de collection WIA sont basés sur 0.

 

 

 



