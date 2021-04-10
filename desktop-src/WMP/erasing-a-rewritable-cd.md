---
title: Effacement d’un CD réinscriptible
description: Effacement d’un CD réinscriptible
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, effacement des CD réinscriptibles
- gravure de CD, effacement des CD réinscriptibles
- effacement des CD réinscriptibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030804"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="fd2db-113">Effacement d’un CD réinscriptible</span><span class="sxs-lookup"><span data-stu-id="fd2db-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="fd2db-114">L’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fournit une méthode d’effacement des disques CD-RW.</span><span class="sxs-lookup"><span data-stu-id="fd2db-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="fd2db-115">Avant d’effacer un CD-ROM, vous devez d’abord vous assurer que l’opération est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd2db-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="fd2db-116">Pour plus d’informations, consultez [récupération de l’état du lecteur et du disque](retrieving-the-drive-and-disc-status.md).</span><span class="sxs-lookup"><span data-stu-id="fd2db-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="fd2db-117">Pour commencer à effacer le contenu d’un CD réinscriptible, appelez [IWMPCdromBurn :: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="fd2db-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="fd2db-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd2db-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd2db-119">**Gravure d’un CD**</span><span class="sxs-lookup"><span data-stu-id="fd2db-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="fd2db-120">**Récupération de l’interface de gravure de CD**</span><span class="sxs-lookup"><span data-stu-id="fd2db-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="fd2db-121">**Démarrage du processus de gravure**</span><span class="sxs-lookup"><span data-stu-id="fd2db-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="fd2db-122">**Récupération de l’état du lecteur et du disque**</span><span class="sxs-lookup"><span data-stu-id="fd2db-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="fd2db-123">**Récupération de l’état d’avancement**</span><span class="sxs-lookup"><span data-stu-id="fd2db-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




