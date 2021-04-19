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
# <a name="using-wia-collection-objects"></a><span data-ttu-id="e61d5-105">Utilisation d’objets de collection WIA</span><span class="sxs-lookup"><span data-stu-id="e61d5-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="e61d5-106">Une collection est un objet qui contient un ou plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="e61d5-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="e61d5-107">Les collections offrent un moyen efficace de regrouper des objets similaires.</span><span class="sxs-lookup"><span data-stu-id="e61d5-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="e61d5-108">L’acquisition d’images Windows (WIA) fournit des collections pour les objets [**DeviceInfo**](-wia-deviceinfo.md) et [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="e61d5-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="e61d5-109">Utilisez des collections pour énumérer les objets qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="e61d5-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="e61d5-110">Par exemple, l’exemple VBScript suivant obtient une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) à partir de la méthode [**Devices**](-wia-iwia-devices.md) , puis utilise une **pour... Chaque** boucle pour itérer au sein de la collection :</span><span class="sxs-lookup"><span data-stu-id="e61d5-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


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
> <span data-ttu-id="e61d5-111">Les objets de collection WIA sont basés sur 0.</span><span class="sxs-lookup"><span data-stu-id="e61d5-111">WIA collection objects are 0-based.</span></span>

 

 

 



