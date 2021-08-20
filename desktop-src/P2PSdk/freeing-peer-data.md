---
description: Tous les pointeurs que les fonctions d’infrastructure homologue retournent doivent être libérés à l’aide de PeerGraphFreeData ou PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Libération de données homologues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9492fec9a22da8252188a75d6d4cee73d2055d29f47e25fc7d55a26cc7909c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794576"
---
# <a name="freeing-peer-data"></a>Libération de données homologues

Tous les pointeurs que les fonctions d’infrastructure homologue retournent doivent être libérés à l’aide de [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Ces fonctions ne doivent être appelées que pour les structures qui sont retournées directement par une fonction d’infrastructure homologue. N’appelez pas une fonction FreeData différente pour libérer des pointeurs imbriqués, par exemple, n’appelez pas une fonction FreeData sur les pointeurs dans une structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) .

## <a name="example-of-freeing-data"></a>Exemple de libération de données

L’extrait de code suivant vous montre comment récupérer les propriétés associées à un graphique, puis libérer les données qui sont retournées.


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



 

 



