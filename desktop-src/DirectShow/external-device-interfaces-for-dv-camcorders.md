---
description: Interfaces d’appareil externe pour les caméscopes DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces d’appareil externe pour les caméscopes DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846881"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfaces d’appareil externe pour les caméscopes DV

Le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) expose trois interfaces pour le contrôle d’un caméscope.



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Interface de base pour le contrôle de périphérique externe. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Contrôle les fonctions VCR.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Lit le code temporel de l’appareil.                 |



 

> [!Note]  
> Pour utiliser ces interfaces avec le pilote de caméscope MSDV, incluez le fichier d’en-tête XPrtDefs. h dans votre projet.

 

Après avoir sélectionné un périphérique de capture et créé une instance du filtre de capture, interrogez le filtre pour obtenir ces interfaces. L’exemple suivant déclare une structure personnalisée qui contient les pointeurs d’interface, ainsi que des valeurs booléennes qui spécifient la disponibilité de chaque interface :


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



