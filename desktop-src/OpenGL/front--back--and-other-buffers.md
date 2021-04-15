---
title: Mémoires tampons avant, arrière et autres
description: OpenGL stocke et manipule les données de pixels dans un trame.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL sur Windows, mémoires tampons
- framebuffers OpenGL
- mémoires tampons de couleur OpenGL
- mémoires tampons de profondeur OpenGL
- mémoires tampons d’accumulation OpenGL
- mémoires tampons de stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380075"
---
# <a name="front-back-and-other-buffers"></a>Mémoires tampons avant, arrière et autres

OpenGL stocke et manipule les données de pixels dans un trame. Le trame se compose d’un ensemble de mémoires tampons logiques : couleur, profondeur, accumulation et mémoires tampons de stencil. La mémoire tampon de couleur est constituée d’un ensemble de mémoires tampons logiques ; Cet ensemble peut inclure l’avant-plan, le front-droit, l’arrière-plan, l’arrière-plan, le verso et un certain nombre de mémoires tampons auxiliaires. Un format de pixel particulier ou une implémentation OpenGL peut ne pas fournir toutes ces mémoires tampons. Par exemple, la version actuelle de l’implémentation de OpenGL de Microsoft dans Windows ne prend pas en charge les images stéréoscopiques. par conséquent, un format de pixel ne peut pas avoir de mémoires tampons de couleur gauche et droite. En outre, la version actuelle ne prend pas en charge les tampons auxiliaires. Pour plus d’informations sur les mémoires tampons OpenGL et les fonctions OpenGL qui fonctionnent sur elles, consultez le *Manuel de référence OpenGL* et le *Guide de programmation OpenGL*.

L’implémentation de OpenGL par Microsoft dans Windows prend en charge la double mise en mémoire tampon des images. Il s’agit d’une technique dans laquelle une application dessine des pixels dans une mémoire tampon hors écran, puis, lorsque cette image est prête à être affichée, copie le contenu de la mémoire tampon hors écran dans une mémoire tampon à l’écran. La double mise en mémoire tampon permet de lisser les modifications d’image, ce qui est particulièrement important pour les images animées.

Deux mémoires tampons de couleur sont disponibles pour les applications qui utilisent la double mise en mémoire tampon : une mémoire tampon d’arrière-plan et une mémoire tampon d’arrière-plan. Par défaut, les commandes de dessin sont dirigées vers la mémoire tampon d’arrière-plan (la mémoire tampon hors écran), tandis que la mémoire tampon d’avant est affichée à l’écran. Lorsque la mémoire tampon hors écran est prête à être affichée, vous appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)et Windows copie le contenu de la mémoire tampon hors écran dans la mémoire tampon à l’écran.

L’implémentation générique utilise une image bitmap indépendante du périphérique (DIB) comme mémoire tampon d’arrière-plan et l’écran s’affiche comme mémoire tampon d’arrière-plan. Les périphériques matériels et leurs pilotes peuvent utiliser des approches différentes.

La double mise en mémoire tampon est une propriété au format pixel. Pour demander une double mise en mémoire tampon pour un format de pixel, définissez l' \_ indicateur PFD DOUBLEBUFFER dans la structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) dans un appel à [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

La fonction principale OpenGL, [**glDrawBuffer**](gldrawbuffer.md), sélectionne des mémoires tampons pour l’écriture et l’effacement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de mémoire tampon](buffer-functions.md)
</dt> </dl>

 

 




