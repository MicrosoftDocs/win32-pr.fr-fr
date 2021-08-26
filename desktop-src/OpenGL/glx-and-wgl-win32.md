---
title: GLX et WGL/Windows
description: certaines fonctions WGL et les fonctions Windows sont plus ou moins analogues aux fonctions de fenêtre GLX X. la liste suivante présente les fonctions GLX et leurs fonctions WGL/Windows correspondantes, si elles sont disponibles.
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- OpenGL sur Windows, fonctions GLX
- GLX fonctions OpenGL
- WGL, comparaison avec les fonctions GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24b88caeed9aea7bae8e38f73818ac180aad9117806508f40550b02eb8a4e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035381"
---
# <a name="glx-and-wglwindows"></a>GLX et WGL/Windows

certaines fonctions WGL et les fonctions Windows sont plus ou moins analogues aux fonctions de fenêtre GLX X. la liste suivante présente les fonctions GLX et leurs fonctions WGL/Windows correspondantes, si elles sont disponibles.



| GLX, fonctions             | fonctions WGL/Windows                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                              |
| **glXCopyContext**        |                                                                                                                                                             |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                                |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)  /  [ **CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                     |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                                |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                        |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                          |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                        |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                                  |
| **glXIsDirect**           |                                                                                                                                                             |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                                    |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                          |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)  /  [ **wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)                                                           |
| **glXWaitGL**             |                                                                                                                                                             |
| **glXWaitX**              |                                                                                                                                                             |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                                    |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)  /  [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) et [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)  /  [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                                |
|                           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                                    |
|                           | [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)                                                                                                              |
|                           | [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)                                                                                                                      |



 

Pour plus d’informations, reportez-vous au *Guide de Portage*.

 

 