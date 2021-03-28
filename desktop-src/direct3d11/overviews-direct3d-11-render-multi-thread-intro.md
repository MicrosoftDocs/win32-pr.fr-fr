---
title: Introduction au multithreading dans Direct3D 11
description: Le multithreading est conçu pour améliorer les performances en effectuant un travail à l’aide d’un ou plusieurs threads en même temps.
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315198"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Introduction au multithreading dans Direct3D 11

Le multithreading est conçu pour améliorer les performances en effectuant un travail à l’aide d’un ou plusieurs threads en même temps.

Dans le passé, cela a souvent été fait en générant un seul thread principal pour le rendu et un ou plusieurs threads pour effectuer des tâches de préparation telles que la création d’objets, le chargement, le traitement, etc. Toutefois, avec la synchronisation intégrée dans Direct3D 11, l’objectif de l’utilisation de multithreads est d’utiliser tous les PROCESSEURs et tous les cycles GPU sans qu’un processeur n’attende un autre processeur (en particulier, le GPU n’est pas en attente, car il a un impact direct sur la fréquence d’images). En procédant ainsi, vous pouvez générer la plus grande quantité de travail tout en conservant la meilleure fréquence d’images. Le concept d’une trame unique pour le rendu n’est plus nécessaire, car l’API implémente la synchronisation.

Le multithreading requiert une certaine forme de synchronisation. Par exemple, si plusieurs threads qui s’exécutent dans une application doivent accéder à un seul contexte de périphérique ([**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)), cette application doit utiliser un mécanisme de synchronisation, tel que les sections critiques, pour synchroniser l’accès à ce contexte de périphérique. Cela est dû au fait que le traitement des commandes de rendu (généralement effectuées sur le GPU) et la génération des commandes de rendu (effectuées généralement sur le processeur via la création d’objets, le chargement des données, la modification d’État, le traitement des données) utilisent souvent les mêmes ressources (textures, nuanceurs, état du pipeline, etc.). L’organisation du travail entre plusieurs threads nécessite une synchronisation pour empêcher un thread de modifier ou de lire des données qui sont modifiées par un autre thread.

Alors que l’utilisation d’un contexte de périphérique ([**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) n’est pas thread-safe, l’utilisation d’un appareil Direct3D 11 ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) est thread-safe. Étant donné que chaque **ID3D11DeviceContext** est mono-thread, un seul thread peut appeler un **ID3D11DeviceContext** à la fois. Si plusieurs threads doivent accéder à un seul **ID3D11DeviceContext**, ils doivent utiliser un mécanisme de synchronisation, tel que les sections critiques, pour synchroniser l’accès à ce **ID3D11DeviceContext**. Toutefois, plusieurs threads ne sont pas tenus d’utiliser des sections critiques ou des primitives de synchronisation pour accéder à un seul **ID3D11Device**. Par conséquent, si une application utilise **ID3D11Device** pour créer des objets de ressource, cette application n’est pas obligée d’utiliser la synchronisation pour créer plusieurs objets de ressource en même temps.

La prise en charge du multithreading divise l’API en deux zones fonctionnelles distinctes :

-   [Création d’objets avec multithread](overviews-direct3d-11-render-multi-thread-create.md)
-   [Rendu immédiat et différé](overviews-direct3d-11-render-multi-thread-render.md)

Les performances du multithreading dépendent de la prise en charge du pilote. [Procédure : vérifier la prise en charge des pilotes](overviews-direct3d-11-render-multi-thread-support.md) fournit plus d’informations sur l’interrogation du pilote et sur la signification des résultats.

Direct3D 11 a été conçu dès le départ pour prendre en charge le multithreading. Direct3D 10 implémente une prise en charge limitée du multithreading à l’aide de la [couche thread-safe](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers). Cette page répertorie les différences de comportement entre les deux versions de DirectX : [différences de Threading entre les versions Direct3D](overviews-direct3d-11-render-multi-thread-differences.md).

## <a name="multithreading-and-dxgi"></a>Multithread et DXGI

Un seul thread à la fois doit utiliser le contexte immédiat. Toutefois, votre application doit également utiliser ce même thread pour les opérations Microsoft DirectX Graphics infrastructure (DXGI), surtout lorsque l’application effectue des appels à la méthode [**IDXGISwapChain ::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) revertie.

> [!Note]  
> L’utilisation simultanée d’un contexte immédiat avec la plupart des fonctions d’interface DXGI n’est pas valide. Pour les SDK DirectX de mars 2009 et versions ultérieures, les seules fonctions DXGI sécurisées sont [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

 

Pour plus d’informations sur l’utilisation de DXGI avec plusieurs threads, consultez [considérations multithread](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traitement multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 