---
description: À propos des périphériques de capture vidéo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: À propos des périphériques de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746373"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="3e814-103">À propos des périphériques de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="3e814-103">About Video Capture Devices</span></span>

<span data-ttu-id="3e814-104">La plupart des nouveaux périphériques de capture vidéo utilisent des pilotes Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="3e814-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="3e814-105">Dans l’architecture WDM, Microsoft fournit un ensemble de pilotes indépendants du matériel, appelés pilotes de classe, et le fournisseur de matériel fournit des minipilotes spécifiques au matériel.</span><span class="sxs-lookup"><span data-stu-id="3e814-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="3e814-106">Un minipilote implémente toutes les fonctions spécifiques à l’appareil. pour la plupart des fonctions, le minipilote appelle le pilote de classe Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e814-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="3e814-107">Dans un graphique de filtre DirectShow, tous les périphériques de capture WDM apparaissent en tant que filtre de [capture vidéo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3e814-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="3e814-108">Le filtre de capture vidéo WDM se configure lui-même en fonction des caractéristiques du pilote.</span><span class="sxs-lookup"><span data-stu-id="3e814-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="3e814-109">Il apparaît sous un nom fourni par le pilote : vous ne verrez pas de filtre appelé « filtre de capture vidéo WDM » n’importe où dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="3e814-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="3e814-110">Certains périphériques de capture plus anciens utilisent encore des pilotes de vidéo pour Windows (VFW).</span><span class="sxs-lookup"><span data-stu-id="3e814-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="3e814-111">Bien que ces pilotes soient à présent obsolètes, ils sont pris en charge dans DirectShow via le filtre de [capture VFW](vfw-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3e814-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e814-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e814-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e814-113">À propos de la capture vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e814-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



