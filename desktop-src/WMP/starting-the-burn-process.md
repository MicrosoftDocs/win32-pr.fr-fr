---
title: Démarrage du processus de gravure
description: Démarrage du processus de gravure
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, démarrage du processus de gravure
- gravure de CD, démarrage du processus de gravure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940696"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="cf167-112">Démarrage du processus de gravure</span><span class="sxs-lookup"><span data-stu-id="cf167-112">Starting the Burn Process</span></span>

<span data-ttu-id="cf167-113">Avant de pouvoir procéder à la gravure, vous devez affecter une sélection à graver.</span><span class="sxs-lookup"><span data-stu-id="cf167-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="cf167-114">Utilisez [IWMPCdromBurn ::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) pour spécifier une sélection pour la gravure.</span><span class="sxs-lookup"><span data-stu-id="cf167-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="cf167-115">Pour plus d’informations sur l’utilisation des sélections, consultez [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="cf167-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="cf167-116">Pour démarrer l’opération de gravure, appelez [IWMPCdromBurn :: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="cf167-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="cf167-117">Vous pouvez arrêter l’opération de gravure en appelant [IWMPCdromBurn :: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span><span class="sxs-lookup"><span data-stu-id="cf167-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="cf167-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf167-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf167-119">**Gravure d’un CD**</span><span class="sxs-lookup"><span data-stu-id="cf167-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="cf167-120">**Récupération de l’interface de gravure de CD**</span><span class="sxs-lookup"><span data-stu-id="cf167-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="cf167-121">**Effacement d’un CD réinscriptible**</span><span class="sxs-lookup"><span data-stu-id="cf167-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="cf167-122">**Récupération de l’état du lecteur et du disque**</span><span class="sxs-lookup"><span data-stu-id="cf167-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="cf167-123">**Récupération de l’état d’avancement**</span><span class="sxs-lookup"><span data-stu-id="cf167-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




