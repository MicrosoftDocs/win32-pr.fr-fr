---
title: Rendre un contexte de rendu non actuel
description: Pour détacher un contexte de rendu d’un thread, rendez-le non actuel. Pour ce faire, vous pouvez appeler la fonction wglMakeCurrent avec les paramètres définis sur NULL. Voici un exemple de cette tâche simple.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL sur Windows, contextes de rendu
- contextes de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121294"
---
# <a name="making-a-rendering-context-not-current"></a>Rendre un contexte de rendu non actuel

Pour détacher un contexte de rendu d’un thread, rendez-le non actuel. Pour ce faire, vous pouvez appeler la fonction [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) avec les paramètres définis sur **null**. Voici un exemple de cette tâche simple.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




