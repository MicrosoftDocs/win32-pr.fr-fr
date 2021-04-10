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
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="98622-107">Portage du code GLX pixmap</span><span class="sxs-lookup"><span data-stu-id="98622-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="98622-108">Le système de fenêtre X utilise des *pixmaps*, qui sont des surfaces de dessin virtuel hors écran sous la forme d’un tableau de bits à trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="98622-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="98622-109">Vous pouvez considérer un pixmap comme une pile de bitmaps : un tableau à deux dimensions de pixels, chaque pixel ayant une valeur comprise entre 0 et 2N1, où N est la profondeur du pixmap.</span><span class="sxs-lookup"><span data-stu-id="98622-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="98622-110">Pour les programmes OpenGL, vous utilisez les fonctions GLX, **glXCreateGLXPixmap** et **glXDestroyGLXPixmap**, pour créer et détruire glx pixmaps utilisé pour le rendu hors écran.</span><span class="sxs-lookup"><span data-stu-id="98622-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="98622-111">Windows utilise des bitmaps indépendantes du périphérique qui remplissent la même fonction que le système X Window pixmaps.</span><span class="sxs-lookup"><span data-stu-id="98622-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="98622-112">Utilisez les fonctions bitmap Windows standard pour créer et détruire des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="98622-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="98622-113">Le tableau suivant répertorie les fonctions GLX pixmap et leurs fonctions bitmap Windows équivalentes.</span><span class="sxs-lookup"><span data-stu-id="98622-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="98622-114">GLX pixmap et font, fonction</span><span class="sxs-lookup"><span data-stu-id="98622-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="98622-115">Fonction bitmap et police Windows</span><span class="sxs-lookup"><span data-stu-id="98622-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98622-116">GLXPixmap **glXCreateGLXPixmap**(Display *\* dpy* *\* , XVisualInfo,* pixmap *pixmap*)</span><span class="sxs-lookup"><span data-stu-id="98622-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="98622-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const octet *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint \* fuUsage \***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)</span><span class="sxs-lookup"><span data-stu-id="98622-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="98622-118">void **glXDestroyGLXPixmap**(Display *\* dpy*, GLXPixmap *pix*)</span><span class="sxs-lookup"><span data-stu-id="98622-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="98622-119">BOOL [SupprimerObjet](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)</span><span class="sxs-lookup"><span data-stu-id="98622-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

