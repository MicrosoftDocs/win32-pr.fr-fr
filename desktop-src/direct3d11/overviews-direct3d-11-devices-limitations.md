---
title: Limitations de la création d’appareils de déformation et de référence
description: Certaines limitations existent pour la création de périphériques de déformation et de référence dans Direct3D 10,1 et Direct3D 11,0. Cette rubrique présente ces limitations.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483ed6d5fd7348df39a4f3064f377845d6bfae1fe46abc47be5acd99e191c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608609"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitations de la création d’appareils de déformation et de référence

Certaines limitations existent pour la création de périphériques de déformation et de référence dans Direct3D 10,1 et Direct3D 11,0. Cette rubrique présente ces limitations.

Les types de pilote de référence de type de pilote D3D10 \_ \_ \_ Warp et D3D10 \_ \_ \_ ne sont pas pris en charge sur les \_ niveaux de fonctionnalité D3D10 Feature de \_ \_ 9 \_ 1 à D3D10 \_ Feature \_ Level \_ 9 \_ 3 dans Direct3D 10,1. En outre, le \_ \_ type de pilote de type Warp du pilote D3D \_ n’est pas pris en charge sur le \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 0 dans Direct3D 11,0. Autrement dit, lorsque vous appelez [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer un périphérique Direct3D 10,1 ou lorsque vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11,0, si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité dans l’appel, l’appel n’est pas valide. Seules les combinaisons suivantes de niveaux de fonctionnalité, runtimes et types de pilotes sont valides pour les périphériques de déviation et de référence :

-   \_TYPE de pilote D3D \_ \_ WARP sur tous les niveaux de fonctionnalités dans Direct3D 11,1, qui Windows 8 comprend

    \_ \_ \_ Référence du type de pilote D3D sur tous les niveaux de fonctionnalités dans Direct3D 11,1

    Quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11,1, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.

-   \_ \_ Type de pilote D3D \_ Warp sur le \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 1 à \_ l’aide de fonctionnalités \_ \_ de niveau de fonctionnalité 10 \_ 1 dans Direct3D 11

    Informations \_ \_ \_ de référence sur le type de pilote D3D sur les niveaux de fonctionnalité de \_ \_ \_ 9 \_ 1 à D3D \_ de niveau de fonctionnalité \_ \_ 11 \_ 0 dans Direct3D 11

    Quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.

-   D3D10 \_ de \_ type \_ de pilote Warp et D3D10 \_ \_ \_ référence de type de pilote sur D3D10 niveau de fonctionnalité \_ \_ \_ 10 \_ 0 à D3D10 \_ \_ \_ \_ niveaux de fonctionnalité 10 1 dans Direct3D 10,1

    Quand vous appelez [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer un appareil Direct3D 10,1, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Présentation de Direct3D 11 sur le matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Comment : créer un appareil WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Comment : créer un appareil de référence](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**\_Type de pilote D3D10 \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ fonctionnalité de \_ niveau1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**\_Type de pilote D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**\_Niveau de fonctionnalité D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 