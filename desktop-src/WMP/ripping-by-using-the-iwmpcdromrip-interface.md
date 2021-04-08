---
title: Extraction à l’aide de l’interface IWMPCdromRip
description: Extraction à l’aide de l’interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, interface IWMPCdromRip
- extraction de CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841909"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="5233b-113">Extraction à l’aide de l’interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="5233b-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="5233b-114">Cette section décrit comment utiliser l’interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) pour extraire de la musique à partir d’un CD.</span><span class="sxs-lookup"><span data-stu-id="5233b-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="5233b-115">L’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5233b-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="5233b-116">Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5233b-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="5233b-117">Pour plus d’informations sur l’extraction de CD, consultez « extraction de musique à partir de CD » dans l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5233b-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="5233b-118">Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="5233b-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="5233b-119">En-têtes inclus</span><span class="sxs-lookup"><span data-stu-id="5233b-119">Included Headers</span></span>

<span data-ttu-id="5233b-120">Pour utiliser le code de cette section, incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="5233b-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="5233b-121">Pointeurs d’interface</span><span class="sxs-lookup"><span data-stu-id="5233b-121">Interface Pointers</span></span>

<span data-ttu-id="5233b-122">Les interfaces pour le lecteur Windows Media sont stockées dans les variables de membre suivantes.</span><span class="sxs-lookup"><span data-stu-id="5233b-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="5233b-123">Les sections suivantes décrivent l’utilisation de l’interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="5233b-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="5233b-124">Récupération de l’interface d’extraction</span><span class="sxs-lookup"><span data-stu-id="5233b-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="5233b-125">Démarrage du processus RIP</span><span class="sxs-lookup"><span data-stu-id="5233b-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="5233b-126">Récupération de l’État RIP</span><span class="sxs-lookup"><span data-stu-id="5233b-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="5233b-127">Sélection d’éléments pour l’extraction</span><span class="sxs-lookup"><span data-stu-id="5233b-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




