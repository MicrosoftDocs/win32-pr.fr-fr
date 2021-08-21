---
description: Contrôle du volume du décodeur
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Contrôle du volume du décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e96ed9efb17a4fb32c41d8b10313edbe015c202b7f7d1f4287e1af20cca559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953148"
---
# <a name="decoder-volume-control"></a>Contrôle du volume du décodeur

Les applications contrôlent le volume audio par le biais de l’interface [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) . Un gestionnaire d’interface **IBasicAudio** est fourni pour KSProxy. Pour qu’un décodeur gère les commandes de volume à partir de KSProxy, il doit ajouter plusieurs clés de Registre dans son script d’installation et prendre en charge le jeu de propriétés **\_ Wave KSPROPSETID** .

Créez de nouvelles clés de Registre pour le pilote :


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



Pour implémenter le contrôle du volume, le pilote doit également prendre en charge **KSPROPSETID \_ Wave**, ainsi que KsProperty.ID = KsProperty \_ Wave \_ volume. Cette propriété est passée au pilote par le biais des méthodes [**IKsPropertySet :: obten**](ikspropertyset-get.md) et [**IKsPropertySet :: Set**](ikspropertyset-set.md) . Les champs LeftAttenuation et RightAttentuation spécifient les volumes de haut-parleur gauche/droit comme valeurs linéaires de 0x0000 à 0xFFFF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces et spécifications du décodeur](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



