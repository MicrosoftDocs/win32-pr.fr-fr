---
title: Portage du code GLX pixmap
description: Portage du code GLX pixmap
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL sur Windows, pixmaps
- portage vers OpenGL, pixmaps
- Portage OpenGL, pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012057"
---
# <a name="porting-glx-pixmap-code"></a>Portage du code GLX pixmap

Le système de fenêtre X utilise des *pixmaps*, qui sont des surfaces de dessin virtuel hors écran sous la forme d’un tableau de bits à trois dimensions. Vous pouvez considérer un pixmap comme une pile de bitmaps : un tableau à deux dimensions de pixels, chaque pixel ayant une valeur comprise entre 0 et 2N1, où N est la profondeur du pixmap.

Pour les programmes OpenGL, vous utilisez les fonctions GLX, **glXCreateGLXPixmap** et **glXDestroyGLXPixmap**, pour créer et détruire glx pixmaps utilisé pour le rendu hors écran.

Windows utilise des bitmaps indépendantes du périphérique qui remplissent la même fonction que le système X Window pixmaps. utilisez les fonctions bitmap Windows standard pour créer et détruire des bitmaps.

le tableau suivant répertorie les fonctions GLX pixmap et leurs équivalents Windows bitmap functions.



| GLX pixmap et font, fonction                                                          | Windows fonction bitmap et de police                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(Display *\* dpy* *\* , XVisualInfo,* pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const octet *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**(Display *\* dpy*, GLXPixmap *pix*)                        | BOOL [SupprimerObjet](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

