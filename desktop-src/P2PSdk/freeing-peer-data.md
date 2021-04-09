---
description: Tous les pointeurs que les fonctions d’infrastructure homologue retournent doivent être libérés à l’aide de PeerGraphFreeData ou PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Libération de données homologues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034519"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="c1e1d-103">Libération de données homologues</span><span class="sxs-lookup"><span data-stu-id="c1e1d-103">Freeing Peer Data</span></span>

<span data-ttu-id="c1e1d-104">Tous les pointeurs que les fonctions d’infrastructure homologue retournent doivent être libérés à l’aide de [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="c1e1d-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="c1e1d-105">Ces fonctions ne doivent être appelées que pour les structures qui sont retournées directement par une fonction d’infrastructure homologue.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="c1e1d-106">N’appelez pas une fonction FreeData différente pour libérer des pointeurs imbriqués, par exemple, n’appelez pas une fonction FreeData sur les pointeurs dans une structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="c1e1d-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="c1e1d-107">Exemple de libération de données</span><span class="sxs-lookup"><span data-stu-id="c1e1d-107">Example of Freeing Data</span></span>

<span data-ttu-id="c1e1d-108">L’extrait de code suivant vous montre comment récupérer les propriétés associées à un graphique, puis libérer les données qui sont retournées.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



