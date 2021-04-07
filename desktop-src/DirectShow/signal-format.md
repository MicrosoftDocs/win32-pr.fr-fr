---
description: Format de signal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Format de signal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846413"
---
# <a name="signal-format"></a><span data-ttu-id="63f96-103">Format de signal</span><span class="sxs-lookup"><span data-stu-id="63f96-103">Signal Format</span></span>

<span data-ttu-id="63f96-104">Le format de signal d’un caméscope DV peut être NTSC ou PAL, standard ou long Play.</span><span class="sxs-lookup"><span data-stu-id="63f96-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="63f96-105">**Pilote MSDV**</span><span class="sxs-lookup"><span data-stu-id="63f96-105">**MSDV Driver**</span></span>

<span data-ttu-id="63f96-106">Pour récupérer le format du signal d’entrée à partir du pilote MSDV, appelez la méthode [**IAMExtTransport :: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) et transmettez l' \_ indicateur de \_ signal d’entrée de base Ed \_ .</span><span class="sxs-lookup"><span data-stu-id="63f96-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="63f96-107">La méthode retourne une constante définie, indiquant le format.</span><span class="sxs-lookup"><span data-stu-id="63f96-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="63f96-108">Le code suivant vérifie le format de signal et utilise cette valeur pour calculer le temps moyen par frame.</span><span class="sxs-lookup"><span data-stu-id="63f96-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="63f96-109">Le mode variable reçoit la constante de format de signal.</span><span class="sxs-lookup"><span data-stu-id="63f96-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="63f96-110">Pour connaître le format de signal de sortie, appelez la même méthode avec l' \_ indicateur de signal de sortie de base Ed \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="63f96-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="63f96-111">**Pilote UVC**</span><span class="sxs-lookup"><span data-stu-id="63f96-111">**UVC Driver**</span></span>

<span data-ttu-id="63f96-112">Pour récupérer le format du signal d’entrée ou de sortie à partir du pilote UVC, appelez [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) sur le code confidentiel et examinez le bloc de format vidéo.</span><span class="sxs-lookup"><span data-stu-id="63f96-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="63f96-113">(Pour les appareils UVC, le code affiché dans l’exemple précédent retourne généralement ED \_ \_Signal de transbasic \_ inconnu. il n’est donc pas fiable.)</span><span class="sxs-lookup"><span data-stu-id="63f96-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="63f96-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63f96-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f96-115">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="63f96-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



