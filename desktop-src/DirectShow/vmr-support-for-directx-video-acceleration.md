---
description: Prise en charge de VMR pour l’accélération vidéo DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Prise en charge de VMR pour l’accélération vidéo DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753812"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="9cf08-103">Prise en charge de VMR pour l’accélération vidéo DirectX</span><span class="sxs-lookup"><span data-stu-id="9cf08-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="9cf08-104">DirectX Video Acceleration est une interface de programmation d’applications (API) et une interface de pilote de périphérique (DDI) correspondante pour l’accélération matérielle du traitement du décodage vidéo numérique, avec prise en charge de la fusion alpha à des fins telles que la prise en charge des sous-images DVD.</span><span class="sxs-lookup"><span data-stu-id="9cf08-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="9cf08-105">DirectX VA est documenté dans le DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="9cf08-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="9cf08-106">L’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , qui fournit un accès en mode utilisateur à la fonctionnalité DirectX va sur un périphérique matériel, est documentée dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9cf08-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="9cf08-107">VMR prend en charge [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)et son implémentation est identique à l’ancien mélangeur de superposition, à l’exception d’une différence importante.</span><span class="sxs-lookup"><span data-stu-id="9cf08-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="9cf08-108">Le mélangeur de superposition garantit que la sortie est rendue dans une surface de recouvrement, tandis que VMR peut envoyer la sortie pour un traitement ultérieur, par exemple une opération 3D, ou envoyer la sortie vers une surface hors écran qui est ensuite blitted à la surface principale.</span><span class="sxs-lookup"><span data-stu-id="9cf08-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cf08-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cf08-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf08-110">À propos de l’accélération vidéo DirectX</span><span class="sxs-lookup"><span data-stu-id="9cf08-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



