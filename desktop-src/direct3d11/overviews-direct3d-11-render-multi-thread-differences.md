---
title: Différences de threads entre les versions Direct3D
description: De nombreux modèles de programmation multithread utilisent des primitives de synchronisation (telles que des mutex) pour créer des sections critiques et empêcher l’accès à du code par plusieurs threads à la fois.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382284"
---
# <a name="threading-differences-between-direct3d-versions"></a>Différences de threads entre les versions Direct3D

De nombreux modèles de programmation multithread utilisent des primitives de synchronisation (telles que des mutex) pour créer des sections critiques et empêcher l’accès à du code par plusieurs threads à la fois.

Toutefois, les méthodes de création de ressources de l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) ont été conçues pour être réentrantes, sans nécessiter de primitives de synchronisation et de sections critiques. Par conséquent, les méthodes de création de ressources sont efficaces et faciles à utiliser.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 11, 10 et 9 :<br/> Direct3D 11 utilise par défaut thread-safe et continue à autoriser les applications à désinscrire à l’aide de D3D11 \_ créer un \_ SINGLETHREADED d’appareil \_ . Si les applications ne peuvent pas être thread-safe, elles doivent adhérer aux règles de thread. Le runtime synchronise les threads pour le compte de l’application, ce qui permet l’exécution de threads simultanés. En fait, la synchronisation dans Direct3D 11 est plus efficace que l’utilisation de la couche thread-safe dans Direct3D 10.<br/> Direct3D 10 peut prendre en charge l’exécution d’un seul thread à la fois. Direct3D 10 est entièrement sécurisé au niveau du thread et permet à une application de refuser ce comportement à l’aide de l’D3D10 \_ créer un \_ appareil à \_ \_ thread unique. <br/> Direct3D 9 n’utilise pas la valeur par défaut thread-safe. Toutefois, lorsque vous appelez [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) ou [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) pour créer un appareil, vous pouvez spécifier l' \_ indicateur multithread D3DCREATE pour rendre le thread de l’API Direct3D 9 sécurisé. Cela entraîne une surcharge de synchronisation importante. Par conséquent, le fait de rendre le thread de l’API Direct3D 9 sécurisé n’est pas recommandé, car les performances peuvent être dégradées.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

