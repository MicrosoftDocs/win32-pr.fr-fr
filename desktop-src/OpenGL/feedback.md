---
title: Commentaires
description: En mode commentaires, chaque primitive à pixelliser génère un bloc de valeurs qui est copié dans le tableau de commentaires.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- mode commentaires, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5d307b9033a60a03b585cb4df6109293d3b9b0b276bde822ca595eb37fcd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082449"
---
# <a name="feedback-mode"></a>Mode Commentaires

En mode commentaires, chaque primitive à pixelliser génère un bloc de valeurs qui est copié dans le tableau de commentaires. Fournissez ce tableau avec [**glFeedbackBuffer**](glfeedbackbuffer.md), que vous devez appeler avant de placer OpenGL en mode commentaires. Chaque bloc de valeurs commence par un code qui indique le type primitif, suivi de valeurs qui décrivent les vertex de la primitive et les données associées. Les entrées sont également écrites pour les bitmaps et les rectangles de pixels. Il n’est pas garanti que les valeurs soient écrites dans le tableau de commentaires tant que vous n’avez pas appelé [**glRenderMode**](glrendermode.md) pour prendre en charge l’extraction en mode feedback. Vous pouvez utiliser [**glPassThrough**](glpassthrough.md) pour fournir un marqueur renvoyé en mode Feedback comme s’il s’agissait d’une primitive.

 

 




