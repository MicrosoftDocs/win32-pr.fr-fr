---
title: Traduction de la bibliothèque GLX
description: Traduction de la bibliothèque GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL sur Windows, bibliothèque GLX
- portage vers OpenGL, bibliothèque GLX
- Portage OpenGL, bibliothèque GLX
- Bibliothèque GLX OpenGL
- Xlib fonctions OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382504"
---
# <a name="translating-the-glx-library"></a>Traduction de la bibliothèque GLX

Les programmes système de fenêtre OpenGL X utilisent l’extension OpenGL avec la bibliothèque X Window System (GLX). La bibliothèque est un ensemble de fonctions et de routines qui initialisent le format de pixel, le rendu du contrôle et effectuent d’autres tâches spécifiques à OpenGL. Il connecte la bibliothèque OpenGL au système de fenêtres X en gérant les handles de fenêtre et les contextes de rendu. Vous devez traduire ces fonctions en leurs fonctions Windows équivalentes. Le tableau suivant répertorie les fonctions GLX du système X Window et leurs fonctions Windows équivalentes.



| GLX/Xlib, fonction         | Fonction Windows                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | Non applicable.                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | Non applicable.                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc), [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Non applicable.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Certaines fonctions GLX n’ont pas de fonction Windows équivalente. Pour porter ces fonctions vers Windows, réécrivez votre code pour obtenir la même fonctionnalité. Par exemple, **glXWaitGL** n’a pas de fonction Windows équivalente, mais vous pouvez obtenir le même résultat, en exécutant toutes les commandes OpenGL en attente, en appelant [**glFinish**](glfinish.md).

Les rubriques suivantes décrivent comment porter les fonctions GLX qui définissent le format de pixel et comment gérer les contextes de rendu, les pixmaps et les bitmaps.

 

 