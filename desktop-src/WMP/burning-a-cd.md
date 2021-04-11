---
title: Gravure d’un CD
description: Gravure d’un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, à propos de
- gravure de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101273"
---
# <a name="burning-a-cd"></a><span data-ttu-id="7d73e-112">Gravure d’un CD</span><span class="sxs-lookup"><span data-stu-id="7d73e-112">Burning a CD</span></span>

<span data-ttu-id="7d73e-113">Cette section décrit comment utiliser l’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) pour graver de la musique sur un CD.</span><span class="sxs-lookup"><span data-stu-id="7d73e-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="7d73e-114">L’interface **IWMPCdromBurn** fournit des fonctionnalités permettant de graver des playlists sur des CD comme des pistes audio ou des données, ainsi que d’effacer CD-RWS.</span><span class="sxs-lookup"><span data-stu-id="7d73e-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="7d73e-115">Utilisation du code</span><span class="sxs-lookup"><span data-stu-id="7d73e-115">Code Usage</span></span>

<span data-ttu-id="7d73e-116">Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="7d73e-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="7d73e-117">En-têtes inclus</span><span class="sxs-lookup"><span data-stu-id="7d73e-117">Included Headers</span></span>

<span data-ttu-id="7d73e-118">Pour utiliser le code de cette section, incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="7d73e-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="7d73e-119">Pointeurs d’interface</span><span class="sxs-lookup"><span data-stu-id="7d73e-119">Interface Pointers</span></span>

<span data-ttu-id="7d73e-120">Les interfaces pour le lecteur Windows Media sont stockées dans les variables membres suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d73e-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="7d73e-121">Les rubriques suivantes décrivent comment utiliser l’API de gravage de CD.</span><span class="sxs-lookup"><span data-stu-id="7d73e-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="7d73e-122">Récupération de l’interface de gravure de CD</span><span class="sxs-lookup"><span data-stu-id="7d73e-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="7d73e-123">Démarrage du processus de gravure</span><span class="sxs-lookup"><span data-stu-id="7d73e-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="7d73e-124">Effacement d’un CD réinscriptible</span><span class="sxs-lookup"><span data-stu-id="7d73e-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="7d73e-125">Récupération de l’état du lecteur et du disque</span><span class="sxs-lookup"><span data-stu-id="7d73e-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="7d73e-126">Récupération de l’état d’avancement</span><span class="sxs-lookup"><span data-stu-id="7d73e-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="7d73e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d73e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d73e-128">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="7d73e-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




