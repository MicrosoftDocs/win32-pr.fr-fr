---
description: Les classes d’appareils permettent de spécifier les propriétés icons, label et DeviceHandlers pour tous les appareils de cette classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991549"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="113ae-103">Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil</span><span class="sxs-lookup"><span data-stu-id="113ae-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="113ae-104">Les classes d’appareils permettent de spécifier les propriétés icons, label et DeviceHandlers pour tous les appareils de cette classe.</span><span class="sxs-lookup"><span data-stu-id="113ae-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="113ae-105">Cela est similaire à l’utilisation de groupes d’appareils, mais les classes de périphérique et leurs appartenances sont déterminées par le matériel au lieu d’être créées ou attribuées.</span><span class="sxs-lookup"><span data-stu-id="113ae-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="113ae-106">Chaque nom de clé de classe, qui est le GUID d’interface d’appareil Plug-and-Play, se trouve sous la clé **DeviceClasses** .</span><span class="sxs-lookup"><span data-stu-id="113ae-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="113ae-107">Sous la clé de classe individuelle, assignez les valeurs des icônes, des étiquettes et des DeviceHandlers.</span><span class="sxs-lookup"><span data-stu-id="113ae-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="113ae-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="113ae-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="113ae-109">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="113ae-109">Step 1:</span></span>

<span data-ttu-id="113ae-110">L’exemple suivant montre les valeurs de clé de classe et DeviceHandlers pour l’interface de volume.</span><span class="sxs-lookup"><span data-stu-id="113ae-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

<span data-ttu-id="113ae-111">Vous pouvez également ajouter des propriétés d’appareil personnalisées sous la clé de classe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="113ae-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="113ae-112">Les propriétés de l’appareil personnalisé s’appliquent à tous les appareils de cette classe.</span><span class="sxs-lookup"><span data-stu-id="113ae-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="113ae-113">Les périphériques et les gestionnaires d’appareils doivent toujours avoir des icônes et des étiquettes associées pour répondre aux exigences de configuration minimale.</span><span class="sxs-lookup"><span data-stu-id="113ae-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="113ae-114">Les propriétés définies au niveau de l’instance de l’appareil sont prioritaires par rapport aux propriétés définies au niveau du groupe d’appareils, qui ont à leur tour priorité sur les propriétés définies au niveau de la classe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="113ae-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



