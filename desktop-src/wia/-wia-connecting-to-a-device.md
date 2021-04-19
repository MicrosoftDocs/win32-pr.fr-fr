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
# <a name="connecting-to-a-device"></a><span data-ttu-id="29253-103">Connexion à un appareil</span><span class="sxs-lookup"><span data-stu-id="29253-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="29253-104">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="29253-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="29253-105">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="29253-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="29253-106">La première étape d’une application ou d’un script qui utilise le modèle de script WIA (Windows Image Acquisition) consiste à créer l’objet [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="29253-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="29253-107">Cet objet fournit des méthodes pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) et connecter ces objets aux appareils.</span><span class="sxs-lookup"><span data-stu-id="29253-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="29253-108">Il offre également la possibilité d’écouter les événements matériels WIA.</span><span class="sxs-lookup"><span data-stu-id="29253-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="29253-109">La ligne de code Microsoft Visual Basic Scripting Edition (VBScript) suivante crée l’objet [**WIA**](-wia-wia.md) :</span><span class="sxs-lookup"><span data-stu-id="29253-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="29253-110">Après avoir créé l’objet [**WIA**](-wia-wia.md) , utilisez la méthode [**Create**](-wia-iwia-create.md) pour se connecter à un périphérique matériel WIA.</span><span class="sxs-lookup"><span data-stu-id="29253-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="29253-111">Vous pouvez également utiliser la propriété [**Devices**](-wia-iwia-devices.md) de l’objet [**WIA**](-wia-wia.md) pour obtenir une collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="29253-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="29253-112">Énumérez cette collection et utilisez la méthode [**Create**](-wia-iwiadeviceinfo-create.md) pour vous connecter à un appareil.</span><span class="sxs-lookup"><span data-stu-id="29253-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
