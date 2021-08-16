---
title: Stratégies de dessin OpenGL multithread
description: GDI ne prend pas en charge plusieurs threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL sur Windows, dessin multithread
- dessin OpenGL multithread OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d928a481e4334f97cad2f7009f008c899ad8378f3fd15cf9e117e6b9599393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937254"
---
# <a name="multithread-opengl-drawing-strategies"></a>Stratégies de dessin OpenGL multithread

GDI ne prend pas en charge plusieurs threads. Vous devez utiliser un contexte de périphérique distinct et un contexte de rendu distinct pour chaque thread. Cela a tendance à limiter les avantages en termes de performances liés à l’utilisation de plusieurs threads avec des systèmes à un seul processeur exécutant des applications OpenGL. Toutefois, il existe des moyens d’utiliser des threads avec un système à processeur unique pour améliorer les performances. Par exemple, vous pouvez utiliser un thread distinct pour passer des appels de rendu OpenGL au matériel 3D dédié.

Les systèmes de multitraitement symétrique (SMP) peuvent tirer parti de l’utilisation de plusieurs threads. Une stratégie évidente consiste à utiliser un thread distinct pour chaque processeur afin de gérer le rendu OpenGL dans des fenêtres distinctes. Par exemple, dans une application de simulation de vol, vous pouvez utiliser des processeurs et des threads distincts pour afficher les vues avant, arrière et latérale.

Un thread ne peut avoir qu’un seul contexte de rendu actif en cours. Lorsque vous utilisez plusieurs threads et plusieurs contextes de rendu, vous devez veiller à synchroniser leur utilisation. Par exemple, utilisez un seul thread pour appeler [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) une fois que tous les threads ont fini de dessiner.

 

 




