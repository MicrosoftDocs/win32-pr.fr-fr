---
description: Interfaces de capture audio et de rendu
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de capture audio et de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514915"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfaces de capture audio et de rendu

Ces interfaces prennent en charge la capture et le rendu audio dans DirectShow



| Interface                                              | Description                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Accédez aux entrées analogiques de la carte son du système et ajustez les caractéristiques, telles que mono ou stéréo, le niveau de mélange, le niveau de panoramique, le bruit, les aigus et les basses. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Obtenir des informations statistiques sur les performances des renderering audio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Contrôler la façon dont le filtre de capture audio alloue des tampons.                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Contrôler la tolérance d’un convertisseur audio lorsqu’il correspond à des vitesses avec une autre horloge.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Permet à une application de spécifier la fenêtre qui a le focus pour contrôler la lecture audio DirectSound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Maintenez une ressource de périphérique audio avant qu’elle ne soit nécessaire.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Interrogez et définissez le format de sortie du filtre de capture.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Définissez le volume et le solde de sortie audio.                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



