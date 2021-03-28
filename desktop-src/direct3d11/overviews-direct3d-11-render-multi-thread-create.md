---
title: Création d’objets avec multithread
description: Utilisez l’interface ID3D11Device pour créer des ressources et des objets, utilisez le ID3D11DeviceContext pour le rendu.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939987"
---
# <a name="object-creation-with-multithreading"></a>Création d’objets avec multithread

Utilisez l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) pour créer des ressources et des objets, utilisez le [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) pour le [rendu](overviews-direct3d-11-render-multi-thread-render.md).

Voici quelques exemples de création de ressources :

-   [Comment : créer une mémoire tampon de vertex](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Comment : créer un tampon d’index](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Comment : créer une mémoire tampon constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Comment : initialiser une texture à partir d’un fichier](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Considérations sur le multithreading

La quantité de concurrence pour la création et le rendu des ressources que votre application peut atteindre dépend du niveau de prise en charge du multithreading que le pilote implémente. Si le pilote prend en charge les créations simultanées, l’application doit avoir des problèmes de concurrence moins importante. Toutefois, si le pilote ne prend pas en charge la création d’objets simultanés, la quantité d’accès concurrentiel est extrêmement limitée. Pour comprendre la quantité de support disponible dans un pilote, interrogez le pilote sur la valeur du membre **DriverConcurrentCreates** de la structure de thread de données de la [**\_ fonctionnalité \_ \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) . Pour plus d’informations sur la vérification de la prise en charge des pilotes pour le multithreading, consultez [procédure : vérifier la prise en charge des pilotes](overviews-direct3d-11-render-multi-thread-support.md).

Les opérations simultanées n’entraînent pas nécessairement de meilleures performances. Par exemple, la création et le chargement d’une texture sont généralement limités par la bande passante de mémoire. La tentative de création et de chargement de plusieurs textures peut ne pas être plus rapide qu’une texture à la fois, même si cela laisse plusieurs cœurs de processeur inactifs. Toutefois, la création de plusieurs nuanceurs à l’aide de plusieurs threads peut augmenter les performances, car cette opération est moins tributaire des ressources système, telles que la bande passante de la mémoire.

Lorsque le pilote et le matériel graphique prennent en charge le multithreading, vous pouvez généralement initialiser plus efficacement les ressources nouvellement créées en passant un pointeur vers les données initiales dans le paramètre *pInitialData* (par exemple, dans un appel à la méthode [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




