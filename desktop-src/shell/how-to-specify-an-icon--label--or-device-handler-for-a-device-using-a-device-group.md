---
description: Les groupes d’appareils permettent de spécifier les propriétés icons, label ou DeviceHandlers pour tout appareil qui déclare lui-même une partie de ce groupe.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951936"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="38951-103">Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="38951-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="38951-104">Les groupes d’appareils permettent de spécifier les propriétés icons, label ou DeviceHandlers pour tout appareil qui déclare lui-même une partie de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="38951-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="38951-105">Si le groupe d’appareils n’est pas un groupe d’appareils fourni par le système, une clé qui définit le groupe d’appareils sera ajoutée sous la clé **AutoplayHandlers** \\ **DeviceGroups** .</span><span class="sxs-lookup"><span data-stu-id="38951-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="38951-106">Vous n’avez pas besoin de définir les trois propriétés pour chaque groupe ; vous pouvez définir uniquement les propriétés que vous souhaitez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="38951-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="38951-107">Toutefois, les périphériques et les gestionnaires d’appareils doivent toujours avoir des icônes et des étiquettes associées pour répondre aux exigences de configuration minimale.</span><span class="sxs-lookup"><span data-stu-id="38951-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="38951-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="38951-108">Instructions</span></span>


<span data-ttu-id="38951-109">L’exemple suivant utilise un système avec plusieurs lecteurs Zip attachés.</span><span class="sxs-lookup"><span data-stu-id="38951-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="38951-110">Si vous ne spécifiez pas les valeurs icons, label et DeviceHandlers pour chaque lecteur individuellement, vous créez un groupe d’appareils appelé ZipDrive et définissez ces valeurs dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="38951-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="38951-111">Chaque lecteur Zip est ensuite déclaré membre du groupe ZipDrive.</span><span class="sxs-lookup"><span data-stu-id="38951-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="38951-112">Tout d’abord, définissez le groupe d’appareils en ajoutant la clé *ZipDrive* suivante et ses valeurs.</span><span class="sxs-lookup"><span data-stu-id="38951-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

<span data-ttu-id="38951-113">Chaque périphérique de lecteur Zip est ensuite déclaré dans le cadre du groupe ZipDrive, en héritant des propriétés de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="38951-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="38951-114">Sous la clé **DeviceParameters** de l’instance de l’appareil, ajoutez une valeur nommée DeviceGroup en tant que type **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="38951-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="38951-115">L’entrée de données pour cette valeur est le nom du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="38951-115">The data entry for this value is the name of the device group.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

<span data-ttu-id="38951-116">Vous pouvez également ajouter des propriétés d’appareil personnalisées autres que icons, label et DeviceHandlers sous la clé du groupe de périphériques, puis les appliquer à tous les appareils qui appartiennent à ce groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="38951-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="38951-117">Les propriétés définies au niveau de l’instance de l’appareil sont prioritaires par rapport aux propriétés définies au niveau du groupe d’appareils, qui ont à leur tour priorité sur les propriétés définies au niveau de la classe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="38951-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



