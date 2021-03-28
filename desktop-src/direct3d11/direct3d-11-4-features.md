---
title: Fonctionnalités Direct3D 11,4
description: Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,4.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941149"
---
# <a name="direct3d-114-features"></a>Fonctionnalités Direct3D 11,4

Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,4.

Consultez également [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Suppression de l’appareil Direct3D

Les méthodes [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)et [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) sont prises en charge par une nouvelle interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), pour prendre en charge la réception d’une notification d’événement asynchrone lorsqu’un périphérique Direct3D a été supprimé.

## <a name="multithreaded-protection"></a>Protection multithread

Pour vous assurer que les commandes graphiques en particulier sont exécutées dans un ordre spécifique, l’interface [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) a des méthodes permettant d’activer et de désactiver la protection multithread, ainsi que les méthodes d’entrée et de sortie du code critique nécessitant cette protection.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Clôtures pour la synchronisation de plusieurs appareils et l’interopérabilité avec Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) et [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) fournissent les mêmes fonctionnalités de barrière que Direct3D 12 pour Direct3D 11. Les délimiteurs sont utilisés pour synchroniser plusieurs appareils Direct3D11, et pour l’interopérabilité entre Direct3D 11 et Direct3D 12. Les délimiteurs sont pris en charge dans Windows 10 Creators Update.

## <a name="extended-nv12-texture-support"></a>Prise en charge étendue de la texture NV12

Les textures NV12 avec des fonctionnalités d’encodage vidéo et de capture prennent désormais en charge le partage. Les indicateurs de texture D3D11 plus anciens pour l’encodage vidéo et la capture sont dépréciés pour NV12, car ils seront définis en permanence pour les nouveaux pilotes. Ces textures peuvent être partagées non seulement avec D3D11, mais également avec D3D12. Dans D3D12, aucun nouvel indicateur ne représente ces fonctionnalités de texture.

Reportez-vous au paramètre booléen dans [**d3d11 \_ Feature \_ Data \_ d3d11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Mise en cache du nuanceur

Les pilotes peuvent prendre en charge la mise en cache des nuanceurs gérés par le système d’exploitation des applications Direct3D11 dans Windows 10 Creators Update.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 