---
title: Extension des fonctions OpenGL
description: La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL sur Windows, fonctions d’extension
- fonctions d’extension OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413678"
---
# <a name="extending-opengl-functions"></a>Extension des fonctions OpenGL

La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions. Les fonctions d’extension prises en charge dans un contexte de rendu ne sont pas nécessairement prises en charge dans un contexte de rendu différent. Pour un contexte de rendu donné dans une application à l’aide de fonctions d’extension, utilisez uniquement les adresses de fonction retournées par la fonction [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .

 

 




