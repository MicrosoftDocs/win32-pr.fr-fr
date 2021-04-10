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
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031779"
---
# <a name="porting-glx-pixmap-code"></a>Portage du code GLX pixmap

Le système de fenêtre X utilise des *pixmaps*, qui sont des surfaces de dessin virtuel hors écran sous la forme d’un tableau de bits à trois dimensions. Vous pouvez considérer un pixmap comme une pile de bitmaps : un tableau à deux dimensions de pixels, chaque pixel ayant une valeur comprise entre 0 et 2N1, où N est la profondeur du pixmap.

Pour les programmes OpenGL, vous utilisez les fonctions GLX, **glXCreateGLXPixmap** et **glXDestroyGLXPixmap**, pour créer et détruire glx pixmaps utilisé pour le rendu hors écran.

Windows utilise des bitmaps indépendantes du périphérique qui remplissent la même fonction que le système X Window pixmaps. Utilisez les fonctions bitmap Windows standard pour créer et détruire des bitmaps.

Le tableau suivant répertorie les fonctions GLX pixmap et leurs fonctions bitmap Windows équivalentes.



| GLX pixmap et font, fonction                                                          | Fonction bitmap et police Windows                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(Display *\* dpy* *\* , XVisualInfo,* pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const octet *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**(Display *\* dpy*, GLXPixmap *pix*)                        | BOOL [SupprimerObjet](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

