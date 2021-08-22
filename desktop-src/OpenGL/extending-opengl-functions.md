---
title: Extension des fonctions OpenGL
description: La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL sur Windows, fonctions d’extension
- fonctions d’extension OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361341"
---
# <a name="extending-opengl-functions"></a>Extension des fonctions OpenGL

La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions. Les fonctions d’extension prises en charge dans un contexte de rendu ne sont pas nécessairement prises en charge dans un contexte de rendu différent. Pour un contexte de rendu donné dans une application à l’aide de fonctions d’extension, utilisez uniquement les adresses de fonction retournées par la fonction [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .

 

 




