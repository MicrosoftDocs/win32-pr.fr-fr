---
title: Direct3D 11 sur du matériel de niveau inférieur
description: Cette section explique comment Direct3D 11 est conçu pour prendre en charge le matériel nouveau ou existant, de DirectX 9 à DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104565741"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 sur du matériel de niveau inférieur

Cette section explique comment Direct3D 11 est conçu pour prendre en charge le matériel nouveau ou existant, de DirectX 9 à DirectX 11.

Ce diagramme montre comment Direct3D 11 prend en charge les matériels nouveaux et existants.

![diagramme du matériel pris en charge par Direct3D 11](images/d3d11-on-downlevel-hardware.png)

Avec Direct3D 11, un nouveau paradigme est présenté sous le nom des niveaux de fonctionnalité. Un niveau de fonctionnalité est un ensemble bien défini de fonctionnalités GPU. À l’aide d’un niveau de fonctionnalité, vous pouvez cibler une application Direct3D à exécuter sur une version de niveau inférieur du matériel Direct3D.

La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                  | Description                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Niveaux de fonctionnalités Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | Cette rubrique traite des niveaux de fonctionnalité Direct3D.<br/>                                                                                                                       |
| [Exceptions](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | Cette rubrique décrit les exceptions lors de l’utilisation de Direct3D 11 sur du matériel de niveau inférieur. <br/>                                                                                      |
| [Nuanceurs de calcul sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | Cette rubrique explique comment utiliser les [nuanceurs de calcul](direct3d-11-advanced-stages-compute-shader.md) dans une application Direct3D 11 sur un matériel Direct3D 10.<br/>             |
| [Prévention des SRVs de nuanceurs de pixels NULL indésirables](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | Cette rubrique explique comment contourner le pilote recevant des vues de nuanceur de ressource (SRVs) **null** , même lorsque les SRVs non **null** sont liés à l’étape nuanceur de pixels.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Rubriques relatives aux niveaux de fonctionnalité



| Rubrique                                                                                                                                                                                                                                                                   | Description                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Procédure : obtention du niveau de fonctionnalité de l’appareil](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Comment obtenir un niveau de fonctionnalité.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





