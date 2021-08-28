---
title: Présentation d’un appareil dans Direct3D 11
description: Le modèle objet Direct3D 11 sépare les fonctionnalités de création et de rendu des ressources dans un appareil et un ou plusieurs contextes. Cette séparation est conçue pour faciliter le multithread.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475705"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Présentation d’un appareil dans Direct3D 11

Le modèle objet Direct3D 11 sépare les fonctionnalités de création et de rendu des ressources dans un appareil et un ou plusieurs contextes. Cette séparation est conçue pour faciliter le multithread.

-   [Appareil](#introduction-to-a-device-in-direct3d-11)
-   [Contexte de périphérique](#device-context)
    -   [Contexte immédiat](#immediate-context)
    -   [Contexte différé](#deferred-context)
-   [Considérations relatives aux threads](#threading-considerations)
-   [Rubriques connexes](#related-topics)

## <a name="device"></a>Appareil

Un appareil est utilisé pour créer des ressources et énumérer les fonctionnalités d’un adaptateur d’affichage. Dans Direct3D 11, un appareil est représenté par une interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

Chaque application doit avoir au moins un périphérique, la plupart des applications ne créent qu’un seul appareil. Créez un appareil pour l’un des pilotes matériels installés sur votre ordinateur en appelant [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) et spécifiez le type de pilote avec l’indicateur de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Chaque périphérique peut utiliser un ou plusieurs contextes de périphérique, en fonction de la fonctionnalité souhaitée.

## <a name="device-context"></a>Contexte de périphérique

Un contexte de périphérique contient la circonstance ou le paramètre dans lequel un appareil est utilisé. Plus précisément, un contexte de périphérique est utilisé pour définir l’état du pipeline et générer des commandes de rendu à l’aide des ressources détenues par un appareil. Direct3D 11 implémente deux types de contextes de périphérique, un pour le rendu immédiat et l’autre pour le rendu différé ; les deux contextes sont représentés par une interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

### <a name="immediate-context"></a>Contexte immédiat

Un contexte immédiat est restitué directement au pilote. Chaque appareil a un seul et unique contexte immédiat qui peut récupérer des données du GPU. Un contexte immédiat peut être utilisé pour restituer (ou lire) immédiatement une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md).

Il existe deux façons d’accéder à un contexte immédiat :

-   En appelant [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   En appelant [**ID3D11Device :: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Contexte différé

Un contexte différé enregistre les commandes GPU dans une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md). Un contexte différé est principalement utilisé pour le multithreading et n’est pas nécessaire pour une application à thread unique. Un contexte différé est généralement utilisé par un thread de travail plutôt que par le thread de rendu principal. Lorsque vous créez un contexte différé, il n’hérite d’aucun État du contexte immédiat.

Pour obtenir un contexte différé, appelez [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Tout contexte (immédiat ou différé) peut être utilisé sur n’importe quel thread à condition que le contexte soit utilisé uniquement dans un thread à la fois.

## <a name="threading-considerations"></a>Considérations relatives aux threads

Ce tableau met en évidence les différences entre le modèle de thread dans Direct3D 11 et les versions antérieures de Direct3D.




| | | Différences entre Direct3D 11 et les versions antérieures de Direct3D :<br /> Toutes les méthodes de l’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> sont libres de thread, ce qui signifie qu’il est possible d’avoir plusieurs threads qui appellent les fonctions en même temps.<br /><ul><li>Toutes les interfaces dérivées de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) sont libres de threads.</li><li>Direct3D 11 fractionne la création et le rendu des ressources en deux interfaces. Map, DEMAPPAGE, Begin, end et GetData sont implémentés sur <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> , car <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> définit fortement l’ordre des opérations. Les interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> et <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> implémentent également des méthodes pour les opérations à thread libre.</li><li>Les méthodes <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (à l’exception de celles qui existent sur <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) ne sont pas de thread libre, autrement dit, elles nécessitent un thread unique. Un seul thread peut appeler en toute sécurité l’une de ses méthodes (dessin, copie, mappage, etc.) à la fois.</li><li>En général, les threads libres réduisent le nombre de primitives de synchronisation utilisées, ainsi que leur durée. Toutefois, une application qui utilise la synchronisation maintenue pendant une longue période peut avoir un impact direct sur la quantité de simultanéité qu’une application peut espérer atteindre.</li></ul>Les méthodes d’interface ID3D10Device ne sont pas conçues pour être libres de threads. ID3D10Device implémente toutes les fonctionnalités de création et de rendu (comme le fait ID3D9Device dans Direct3D 9). Les mappages et les mappages sont implémentés sur les interfaces dérivées de ID3D10Resource, Begin, end et GetData sont implémentées sur les interfaces dérivées de ID3D10Asynchronous.<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





