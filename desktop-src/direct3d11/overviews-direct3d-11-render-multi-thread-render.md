---
title: Rendu immédiat et différé
description: Direct3D 11 prend en charge deux types de rendu immédiats et différés. Les deux sont implémentés à l’aide de l’interface ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740a957ec4b7f2edacb4b753c7f68230494b10cf33721ef6c2d869de334517b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912931"
---
# <a name="immediate-and-deferred-rendering"></a>Rendu immédiat et différé

Direct3D 11 prend en charge deux types de rendu : immédiat et différé. Les deux sont implémentés à l’aide de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

## <a name="immediate-rendering"></a>Rendu immédiat

Le rendu immédiat fait référence à l’appel d’API ou de commandes de rendu à partir d’un appareil, qui met en file d’attente les commandes dans une mémoire tampon pour l’exécution sur le GPU. Utilisez un contexte immédiat pour le rendu, la définition de l’état du pipeline et la lecture d’une liste de commandes.

Créez un contexte immédiat à l’aide de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Rendu différé

Le rendu différé enregistre les commandes graphiques dans une mémoire tampon de commande afin qu’elles puissent être lues à un moment donné. Utilisez un contexte différé pour enregistrer les commandes (rendu et paramètre d’État) dans une liste de commandes. Le rendu différé est un nouveau concept dans Direct3D 11. le rendu différé est conçu pour prendre en charge le rendu sur un thread lors de l’enregistrement de commandes de rendu sur des threads supplémentaires. Cette stratégie multithread parallèle vous permet de diviser des scènes complexes en tâches simultanées. Pour plus d’informations sur le rendu des scènes complexes, consultez [rendu à plusieurs passes](overviews-direct3d-11-render-multipass.md).

Créez un contexte différé à l’aide de [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D génère une surcharge de rendu lorsqu’il met en file d’attente des commandes dans le tampon de commande. En revanche, une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md) s’exécute bien plus efficacement pendant la lecture. Pour utiliser une liste de commandes, enregistrez les commandes de rendu avec un contexte différé et lisez-les à l’aide d’un contexte immédiat.

Vous ne pouvez générer qu’une seule liste de commandes en mode monothread. Toutefois, vous pouvez créer et utiliser plusieurs contextes différés simultanément, chacun dans un thread séparé. Ensuite, vous pouvez utiliser ces plusieurs contextes différés pour créer simultanément plusieurs listes de commandes.

Vous ne pouvez pas lire deux ou plusieurs listes de commandes simultanément sur le contexte immédiat.

Pour déterminer si un contexte de périphérique est un contexte immédiat ou différé, appelez [**ID3D11DeviceContext :: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

La méthode [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) est uniquement prise en charge dans un contexte différé pour les ressources dynamiques ([**\_ utilisation \_ dynamique d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) où le premier appel dans la liste de commandes est [**d3d11 \_ mappage d' \_ écriture \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). **D3d11 \_ Le mappage d' \_ écriture \_ sans \_** remplacement est pris en charge lors des appels suivants, s’ils sont disponibles pour le type de ressource donné.

Les requêtes dans un contexte différé sont limitées à la génération de données et au dessin prédicat. Vous ne pouvez pas appeler [**ID3D11DeviceContext :: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) sur un contexte différé pour obtenir des données sur une requête ; vous pouvez uniquement appeler **GetData** dans le contexte immédiat pour obtenir des données sur une requête. Vous pouvez définir un prédicat de rendu (un type de requête) en appelant [**D3D11DeviceContext :: SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) pour utiliser les résultats de requête sur le GPU. Vous pouvez générer des données de requête par le biais d’appels à [**ID3D11DeviceContext :: Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) et [**ID3D11DeviceContext :: end**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end). Toutefois, les données de requête ne sont pas disponibles tant que vous n’avez pas appelé [**ID3D11DeviceContext :: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) dans le contexte immédiat pour envoyer la liste de commandes de contexte différée. Les données de la requête sont ensuite traitées par le GPU.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traitement multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




