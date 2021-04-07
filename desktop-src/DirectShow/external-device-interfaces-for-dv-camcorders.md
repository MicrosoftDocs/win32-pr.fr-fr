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
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="452fd-103">Interfaces d’appareil externe pour les caméscopes DV</span><span class="sxs-lookup"><span data-stu-id="452fd-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="452fd-104">Le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) expose trois interfaces pour le contrôle d’un caméscope.</span><span class="sxs-lookup"><span data-stu-id="452fd-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="452fd-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="452fd-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="452fd-106">Interface de base pour le contrôle de périphérique externe.</span><span class="sxs-lookup"><span data-stu-id="452fd-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="452fd-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="452fd-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="452fd-108">Contrôle les fonctions VCR.</span><span class="sxs-lookup"><span data-stu-id="452fd-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="452fd-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="452fd-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="452fd-110">Lit le code temporel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="452fd-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="452fd-111">Pour utiliser ces interfaces avec le pilote de caméscope MSDV, incluez le fichier d’en-tête XPrtDefs. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="452fd-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="452fd-112">Après avoir sélectionné un périphérique de capture et créé une instance du filtre de capture, interrogez le filtre pour obtenir ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="452fd-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="452fd-113">L’exemple suivant déclare une structure personnalisée qui contient les pointeurs d’interface, ainsi que des valeurs booléennes qui spécifient la disponibilité de chaque interface :</span><span class="sxs-lookup"><span data-stu-id="452fd-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="452fd-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="452fd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="452fd-115">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="452fd-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



