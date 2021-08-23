---
description: Prise en charge de VMR pour l’accélération vidéo DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Prise en charge de VMR pour l’accélération vidéo DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696729"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Prise en charge de VMR pour l’accélération vidéo DirectX

DirectX Video Acceleration est une interface de programmation d’applications (API) et une interface de pilote de périphérique (DDI) correspondante pour l’accélération matérielle du traitement du décodage vidéo numérique, avec prise en charge de la fusion alpha à des fins telles que la prise en charge des sous-images DVD. DirectX VA est documenté dans le Windows DDK. L’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , qui fournit un accès en mode utilisateur à la fonctionnalité DirectX va sur un périphérique matériel, est documentée dans ce kit de développement logiciel (SDK).

VMR prend en charge [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), et son implémentation est identique à l’ancienne Mixer de superposition, à l’exception d’une différence importante. la superposition Mixer garantie que la sortie est rendue dans une surface de recouvrement, tandis que VMR peut envoyer la sortie pour un traitement ultérieur, par exemple une opération 3d, ou elle peut envoyer la sortie vers une surface hors écran qui est ensuite blitted à la surface principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’accélération vidéo DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



