---
description: Contrôle du volume du décodeur
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Contrôle du volume du décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392831"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="7ff1a-103">Contrôle du volume du décodeur</span><span class="sxs-lookup"><span data-stu-id="7ff1a-103">Decoder Volume Control</span></span>

<span data-ttu-id="7ff1a-104">Les applications contrôlent le volume audio par le biais de l’interface [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="7ff1a-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="7ff1a-105">Un gestionnaire d’interface **IBasicAudio** est fourni pour KSProxy.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="7ff1a-106">Pour qu’un décodeur gère les commandes de volume à partir de KSProxy, il doit ajouter plusieurs clés de Registre dans son script d’installation et prendre en charge le jeu de propriétés **\_ Wave KSPROPSETID** .</span><span class="sxs-lookup"><span data-stu-id="7ff1a-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="7ff1a-107">Créez de nouvelles clés de Registre pour le pilote :</span><span class="sxs-lookup"><span data-stu-id="7ff1a-107">Create some new registry keys for the driver:</span></span>


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



<span data-ttu-id="7ff1a-108">Pour implémenter le contrôle du volume, le pilote doit également prendre en charge **KSPROPSETID \_ Wave**, ainsi que KsProperty.ID = KsProperty \_ Wave \_ volume.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="7ff1a-109">Cette propriété est passée au pilote par le biais des méthodes [**IKsPropertySet :: obten**](ikspropertyset-get.md) et [**IKsPropertySet :: Set**](ikspropertyset-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff1a-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="7ff1a-110">Les champs LeftAttenuation et RightAttentuation spécifient les volumes de haut-parleur gauche/droit comme valeurs linéaires de 0x0000 à 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ff1a-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ff1a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ff1a-112">Interfaces et spécifications du décodeur</span><span class="sxs-lookup"><span data-stu-id="7ff1a-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



