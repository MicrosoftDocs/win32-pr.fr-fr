---
title: Portage de contextes de rendu
description: Portage de contextes de rendu
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextes de rendu OpenGL, Portage
- OpenGL sur Windows, contextes de rendu
- portage vers OpenGL, contextes de rendu
- Portage OpenGL, contextes de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fcb6a70f6858ac9c11258c681345ee88a8807c91230f8d3d35fc579ab3371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358339"
---
# <a name="porting-rendering-contexts"></a>Portage de contextes de rendu

le système de fenêtres X et Windows restituer les contextes de rendu. Six fonctions GLX gèrent les contextes de rendu et cinq d’entre elles ont une fonction Windows équivalente.

le tableau suivant répertorie les fonctions de rendu GLX et leurs fonctions Windows équivalentes.



| GLX fonction de contexte de rendu                                                                            | Windows fonction de contexte de rendu                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**(Display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)            | Non applicable.                                                         |
| GLXContext **glXCreateContext**(Display *\* dpy* *\* , XVisualInfo,* GLXContext *shareList*, bool *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)          |
| void **glXDeleteContext**(Display *\* dpy*, GLXContext *CTX*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)                  |
| Bool **glXMakeCurrent**(Display *\* dpy*, GLXDrawable *Draw*, GLXContext *CTX*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*) |



 

Les types de retour et d’autres types ont des noms différents dans le système de fenêtres X que dans Windows. Vous pouvez rechercher des occurrences de GLXContext pour vous aider à trouver des parties de votre code qui doivent être portées.

Les sections suivantes comparent le rendu des exemples de code de contexte dans un programme système X Window et le même code une fois qu’il a été porté à Windows.

Pour plus d’informations sur le rendu des contextes, consultez [contextes de rendu](rendering-contexts.md).

 

 




