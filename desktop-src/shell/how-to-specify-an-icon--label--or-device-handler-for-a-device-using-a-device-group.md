---
description: Les groupes d’appareils permettent de spécifier les propriétés icons, label ou DeviceHandlers pour tout appareil qui déclare lui-même une partie de ce groupe.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412479"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils

Les groupes d’appareils permettent de spécifier les propriétés icons, label ou DeviceHandlers pour tout appareil qui déclare lui-même une partie de ce groupe. Si le groupe d’appareils n’est pas un groupe d’appareils fourni par le système, une clé qui définit le groupe d’appareils sera ajoutée sous la clé **AutoplayHandlers** \\ **DeviceGroups** . Vous n’avez pas besoin de définir les trois propriétés pour chaque groupe ; vous pouvez définir uniquement les propriétés que vous souhaitez personnaliser. Toutefois, les périphériques et les gestionnaires d’appareils doivent toujours avoir des icônes et des étiquettes associées pour répondre aux exigences de configuration minimale.

## <a name="instructions"></a>Instructions


L’exemple suivant utilise un système avec plusieurs lecteurs Zip attachés. Si vous ne spécifiez pas les valeurs icons, label et DeviceHandlers pour chaque lecteur individuellement, vous créez un groupe d’appareils appelé ZipDrive et définissez ces valeurs dans celui-ci. Chaque lecteur Zip est ensuite déclaré membre du groupe ZipDrive.

Tout d’abord, définissez le groupe d’appareils en ajoutant la clé *ZipDrive* suivante et ses valeurs.

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

Chaque périphérique de lecteur Zip est ensuite déclaré dans le cadre du groupe ZipDrive, en héritant des propriétés de ce groupe. Sous la clé **DeviceParameters** de l’instance de l’appareil, ajoutez une valeur nommée DeviceGroup en tant que type **reg \_ SZ**. L’entrée de données pour cette valeur est le nom du groupe d’appareils.

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

Vous pouvez également ajouter des propriétés d’appareil personnalisées autres que icons, label et DeviceHandlers sous la clé du groupe de périphériques, puis les appliquer à tous les appareils qui appartiennent à ce groupe d’appareils.

> [!Note]  
> Les propriétés définies au niveau de l’instance de l’appareil sont prioritaires par rapport aux propriétés définies au niveau du groupe d’appareils, qui ont à leur tour priorité sur les propriétés définies au niveau de la classe de l’appareil.

 

 

 



