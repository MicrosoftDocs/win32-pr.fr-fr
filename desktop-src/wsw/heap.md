---
title: Segment de mémoire (heap)
description: Un segment de mémoire effectue le suivi d’un groupe d’allocations libérées en tant qu’unité.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Services Web du tas pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005929"
---
# <a name="heap"></a>Segment de mémoire (heap)

Un segment de mémoire effectue le suivi d’un groupe d’allocations libérées en tant qu’unité.

Cela vous permet d’éviter des modèles complexes d’allocation et de libération de mémoire lorsque vous utilisez WWSAPI.


Un segment de mémoire est associé à chaque message. Lorsqu’un message est envoyé ou qu’un message est reçu, le segment de mémoire du message est utilisé pour toutes les allocations associées à ce message particulier. Après l’envoi ou la réception d’un message, le segment de mémoire est réinitialisé (ce qui nettoie toutes les allocations associées au message en question).

Les segments de mémoire peuvent également être utilisés pour stocker des données de message indépendamment de la durée de vie d’un message. La plupart des spécifications allow de l’API du tas à utiliser lors de la lecture des données donnent un contrôle explicite sur la durée de vie des données lues.

L’alignement des allocations d’un segment de mémoire sur au moins une limite de 8 octets est garanti.

Les allocations de zéro octet retournent un pointeur non NULL.

dans Windows 7, si PageHeap est activé, un segment de mémoire retourné par HeapCreate est utilisé pour gérer la mémoire. Dans ce cas, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) est directement mappé à HeapAlloc et [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) est mappé à HeapDestroy.

L’énumération suivante est utilisée avec le tas :

-   [**\_ID de \_ propriété du tas WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Les fonctions suivantes sont utilisées avec le tas :

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

Le handle suivant est utilisé avec le tas :

-   [\_tas WS](ws-heap.md)

Les structures suivantes sont utilisées avec le tas :

-   [**\_Propriétés du tas WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_propriété du tas WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




