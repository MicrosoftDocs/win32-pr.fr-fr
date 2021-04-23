---
description: Interfaces d’appareil externe pour les caméscopes DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces d’appareil externe pour les caméscopes DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909797"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="0d465-103">Interfaces d’appareil externe pour les caméscopes DV</span><span class="sxs-lookup"><span data-stu-id="0d465-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="0d465-104">Le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) expose trois interfaces pour le contrôle d’un caméscope.</span><span class="sxs-lookup"><span data-stu-id="0d465-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="0d465-105">Étiquette</span><span class="sxs-lookup"><span data-stu-id="0d465-105">Label</span></span> | <span data-ttu-id="0d465-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d465-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="0d465-107">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="0d465-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="0d465-108">Interface de base pour le contrôle de périphérique externe.</span><span class="sxs-lookup"><span data-stu-id="0d465-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="0d465-109">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="0d465-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="0d465-110">Contrôle les fonctions VCR.</span><span class="sxs-lookup"><span data-stu-id="0d465-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="0d465-111">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="0d465-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="0d465-112">Lit le code temporel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d465-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="0d465-113">Pour utiliser ces interfaces avec le pilote de caméscope MSDV, incluez le fichier d’en-tête XPrtDefs. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="0d465-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="0d465-114">Après avoir sélectionné un périphérique de capture et créé une instance du filtre de capture, interrogez le filtre pour obtenir ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0d465-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="0d465-115">L’exemple suivant déclare une structure personnalisée qui contient les pointeurs d’interface, ainsi que des valeurs booléennes qui spécifient la disponibilité de chaque interface :</span><span class="sxs-lookup"><span data-stu-id="0d465-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0d465-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d465-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d465-117">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="0d465-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



