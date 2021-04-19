---
title: Surveillance de la progression des compresseurs et des décompresseurs
description: Surveillance de la progression des compresseurs et des décompresseurs
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Gestionnaire de compression vidéo (VCM), surveillance
- VCM (gestionnaire de compression vidéo), surveillance
- ICSetStatusProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510009"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a><span data-ttu-id="52b80-106">Surveillance de la progression des compresseurs et des décompresseurs</span><span class="sxs-lookup"><span data-stu-id="52b80-106">Monitoring the Progress of Compressors and Decompressors</span></span>

<span data-ttu-id="52b80-107">Votre application peut surveiller la progression d’une longue opération effectuée par un compresseur ou un décompresseur en lui envoyant l’adresse d’une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="52b80-107">Your application can monitor the progress of a lengthy operation performed by a compressor or decompressor by sending it the address of a callback function.</span></span> <span data-ttu-id="52b80-108">Vous pouvez utiliser la fonction [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) pour envoyer l’adresse au compresseur ou au décompresseur.</span><span class="sxs-lookup"><span data-stu-id="52b80-108">You can use the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function to send the address to the compressor or decompressor.</span></span> <span data-ttu-id="52b80-109">Lorsque le compresseur ou le décompresseur reçoit cette adresse, il envoie des messages d’État à la fonction.</span><span class="sxs-lookup"><span data-stu-id="52b80-109">When the compressor or decompressor receives this address, it sends status messages to the function.</span></span> <span data-ttu-id="52b80-110">Ces messages indiquent si l’opération est en cours de démarrage, d’arrêt, de production ou de poursuite.</span><span class="sxs-lookup"><span data-stu-id="52b80-110">These messages indicate whether the operation is starting, stopping, yielding, or proceeding.</span></span>

 

 




