---
description: Cette section contient des informations de référence sur les interfaces vidéo de Microsoft Direct3D 12.
ms.assetid: ''
title: Interfaces vidéo Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 4451cac5983ddc300957b4661fc68ff30da0496a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525788"
---
# <a name="direct3d-12-video-interfaces"></a>Interfaces vidéo Direct3D 12

Cette section contient des informations de référence sur les interfaces vidéo de Microsoft Direct3D 12.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                | Description                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [ID3D11VideoContext3](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videocontext3)  | Fournit les fonctionnalités vidéo d’un appareil Microsoft Direct3D 11. |
| [ID3D12VideoDecodeCommandList](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist)  | Encapsule une liste de commandes graphiques pour le décodage vidéo.|
| [ID3D12VideoDecodeCommandList1](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist1)  | Encapsule une liste de commandes graphiques pour le décodage vidéo.|
| [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder)  | Représente un décodeur vidéo Direct3D 12.|
| [ID3D12VideoDecoder1](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder1)  | Représente un décodeur vidéo Direct3D 12 qui contient des ressources indépendantes de la résolution et un État pour effectuer l’opération de décodage. Ajoute la prise en charge des ressources protégées.|
| [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap)  | Représente un tas de décodeur vidéo Direct3D 12.|
| [ID3D12VideoDevice](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodevice)  | Fournit le décodage vidéo et les fonctionnalités de traitement d’un appareil Microsoft Direct3D 12, y compris la possibilité d’interroger les fonctionnalités vidéo et d’instancier les décodeurs et les processeurs vidéo.|
| [ID3D11VideoDevice2](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videodevice2)  | Fournit le décodage vidéo et les fonctionnalités de traitement vidéo d’un appareil Microsoft Direct3D 11.|
| [ID3D12VideoDevice3](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodevice3)  | Étend l’interface ID3D12VideoDevice pour ajouter la prise en charge des fonctionnalités d’encodage vidéo.|
| [ID3D12VideoExtensionCommand](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoextensioncommand)  | Objet de référence compté représentant la commande d’extension vidéo.|
| [ID3D12VideoEncodeCommandList](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist)  | Encapsule une liste de commandes graphiques pour l’encodage vidéo, y compris l’estimation de mouvement.|
| [ID3D12VideoEncodeCommandList1](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist1)  | Cette interface hérite de ID3D12VideoEncodeCommandList et ajoute la prise en charge des commandes d’extension vidéo.|
| [ID3D12VideoEncodeCommandList2](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist2)  | Cette interface hérite de ID3D12VideoEncodeCommandList1 et ajoute des méthodes pour l’encodage de vidéos et 
résolution des métadonnées de l’opération d’encodage.|
| [ID3D12VideoEncoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoencoder)  | Représente un encodeur vidéo Direct3D 12.|
| [ID3D12VideoEncoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoencoderheap)  | Représente un tas de l’encodeur vidéo Direct3D 12.|
| [ID3D12VideoMotionEstimator](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videomotionestimator)  | Cette interface gère le contexte des opérations d’estimation de mouvement vidéo.|
| [ID3D12VideoMotionVectorHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap)  | Représente un segment de mémoire dans lequel sont stockés les vecteurs de mouvement estimés.|
| [ID3D12VideoProcessCommandList](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocesscommandlist)  | Encapsule une liste de commandes graphiques pour le traitement vidéo.|
| [ID3D12VideoProcessCommandList1](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocesscommandlist1)  | Encapsule une liste de commandes graphiques pour le traitement vidéo.|
| [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor)  | Fournit des méthodes pour obtenir des informations sur les paramètres de l’appel à ID3D12VideoDevice :: CreateVideoProcessor qui a créé le processeur vidéo.|



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D 12](direct3d-12-video-apis.md)
</dt> </dl>

 

 




