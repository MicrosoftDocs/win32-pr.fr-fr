---
description: Une collection est un objet qui contient un ou plusieurs objets. Les collections offrent un moyen efficace de regrouper des objets similaires. L’acquisition d’images Windows (WIA) fournit des collections pour les objets DeviceInfo et Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Utilisation d’objets de collection WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517523"
---
# <a name="using-wia-collection-objects"></a>Utilisation d’objets de collection WIA

Une collection est un objet qui contient un ou plusieurs objets. Les collections offrent un moyen efficace de regrouper des objets similaires. L’acquisition d’images Windows (WIA) fournit des collections pour les objets [**DeviceInfo**](-wia-deviceinfo.md) et [**Item**](-wia-item.md) .

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

 

 

 



