---
description: Accélération vidéo DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Accélération vidéo DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201151"
---
# <a name="directx-video-acceleration-20"></a>Accélération vidéo DirectX 2,0

DirectX Video Acceleration (DXVA) est une API et une interface DDI correspondante pour l’utilisation de l’accélération matérielle pour accélérer le traitement de codec vidéo. Les codecs logiciels et les processeurs vidéo logiciels peuvent utiliser la fonctionnalité DXVA pour décharger certaines opérations gourmandes en ressources du processeur vers le GPU. Par exemple, un décodeur logiciel peut décharger la transformation de cosinus discrète inverse (iDCT) sur le GPU.

Cette section contient les rubriques suivantes :

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de DXVA 2,0](about-dxva-2-0.md)<br/>                                                   | Vue d’ensemble d’DXVA 2 et de sa relation avec DXVA 1.<br/>                                                                                                                                                        |
| [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md)<br/>                                 | Le gestionnaire de périphériques Microsoft Direct3D permet à deux objets ou plus de partager le même appareil Microsoft Direct3D 9.<br/>                                                                                      |
| [Prise en charge de DXVA 2,0 dans DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans un filtre de décodeur DirectShow.<br/>                                                                                             |
| [Prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans une transformation de Media Foundation (MFT) à l’aide de Direct3D 9<br/>                                                                      |
| [Traitement vidéo DXVA](dxva-video-processing.md)<br/>                                     | Le traitement vidéo DXVA encapsule les fonctions du matériel graphique dédié au traitement d’images vidéo non compressées. Les services de traitement vidéo incluent l’entrelacement et le mixage vidéo.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) est une API pour le traitement vidéo accéléré par le matériel. <br/>                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Spécification DXVA 1](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
