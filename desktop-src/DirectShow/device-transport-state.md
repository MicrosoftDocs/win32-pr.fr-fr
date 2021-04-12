---
description: État du transport de l’appareil
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: État du transport de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392895"
---
# <a name="device-transport-state"></a><span data-ttu-id="401b5-103">État du transport de l’appareil</span><span class="sxs-lookup"><span data-stu-id="401b5-103">Device Transport State</span></span>

<span data-ttu-id="401b5-104">Pour récupérer l’état actuel de l’appareil, par exemple lire, suspendre ou arrêter, appelez la méthode [**IAMExtTransport :: obtenir le \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) .</span><span class="sxs-lookup"><span data-stu-id="401b5-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="401b5-105">La méthode récupère une constante qui indique l’état de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="401b5-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="401b5-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="401b5-106">Value</span></span>                    | <span data-ttu-id="401b5-107">État de l’appareil</span><span class="sxs-lookup"><span data-stu-id="401b5-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="401b5-108">\_lecture en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="401b5-109">Lire</span><span class="sxs-lookup"><span data-stu-id="401b5-109">Play</span></span>         |
| <span data-ttu-id="401b5-110">\_arrêt en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="401b5-111">Arrêter</span><span class="sxs-lookup"><span data-stu-id="401b5-111">Stop</span></span>         |
| <span data-ttu-id="401b5-112">\_gel en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="401b5-113">Suspendre</span><span class="sxs-lookup"><span data-stu-id="401b5-113">Pause</span></span>        |
| <span data-ttu-id="401b5-114">\_mode Ed \_ FF</span><span class="sxs-lookup"><span data-stu-id="401b5-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="401b5-115">Avance rapide</span><span class="sxs-lookup"><span data-stu-id="401b5-115">Fast-forward</span></span> |
| <span data-ttu-id="401b5-116">\_rembob en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="401b5-117">Rembobiner</span><span class="sxs-lookup"><span data-stu-id="401b5-117">Rewind</span></span>       |
| <span data-ttu-id="401b5-118">\_enregistrement en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="401b5-119">Enregistrement</span><span class="sxs-lookup"><span data-stu-id="401b5-119">Record</span></span>       |
| <span data-ttu-id="401b5-120">\_blocage d' \_ enregistrement en mode Ed \_</span><span class="sxs-lookup"><span data-stu-id="401b5-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="401b5-121">Enregistrement-pause</span><span class="sxs-lookup"><span data-stu-id="401b5-121">Record-pause</span></span> |



 

<span data-ttu-id="401b5-122">Le code suivant vérifie l’état de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="401b5-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="401b5-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="401b5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401b5-124">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="401b5-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



