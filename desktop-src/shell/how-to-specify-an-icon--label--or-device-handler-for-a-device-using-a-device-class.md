---
description: Les classes d’appareils permettent de spécifier les propriétés icons, label et DeviceHandlers pour tous les appareils de cette classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412481"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil

Les classes d’appareils permettent de spécifier les propriétés icons, label et DeviceHandlers pour tous les appareils de cette classe. Cela est similaire à l’utilisation de groupes d’appareils, mais les classes de périphérique et leurs appartenances sont déterminées par le matériel au lieu d’être créées ou attribuées. Chaque nom de clé de classe, qui est le GUID d’interface d’appareil Plug-and-Play, se trouve sous la clé **DeviceClasses** . Sous la clé de classe individuelle, assignez les valeurs des icônes, des étiquettes et des DeviceHandlers.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

L’exemple suivant montre les valeurs de clé de classe et DeviceHandlers pour l’interface de volume.

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

Vous pouvez également ajouter des propriétés d’appareil personnalisées sous la clé de classe de l’appareil. Les propriétés de l’appareil personnalisé s’appliquent à tous les appareils de cette classe. Les périphériques et les gestionnaires d’appareils doivent toujours avoir des icônes et des étiquettes associées pour répondre aux exigences de configuration minimale.

> [!Note]  
> Les propriétés définies au niveau de l’instance de l’appareil sont prioritaires par rapport aux propriétés définies au niveau du groupe d’appareils, qui ont à leur tour priorité sur les propriétés définies au niveau de la classe de l’appareil.

 

 

 



