---
title: Démarrage du processus RIP
description: Démarrage du processus RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, démarrage du processus RIP
- extraction de CD, démarrage du processus RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512714"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="01b90-112">Démarrage du processus RIP</span><span class="sxs-lookup"><span data-stu-id="01b90-112">Starting the Rip Process</span></span>

<span data-ttu-id="01b90-113">Après avoir récupéré l’interface d’extraction comme expliqué dans la section précédente, démarrez le processus d’extraction en appelant [IWMPCdromRip :: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="01b90-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="01b90-114">Vous pouvez arrêter l’opération d’extraction en appelant [IWMPCdromRip :: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="01b90-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="01b90-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01b90-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01b90-116">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="01b90-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="01b90-117">**Récupération de l’interface d’extraction**</span><span class="sxs-lookup"><span data-stu-id="01b90-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="01b90-118">**Récupération de l’État RIP**</span><span class="sxs-lookup"><span data-stu-id="01b90-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="01b90-119">**Sélection d’éléments pour l’extraction**</span><span class="sxs-lookup"><span data-stu-id="01b90-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




