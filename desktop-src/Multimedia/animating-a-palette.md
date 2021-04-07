---
title: Animation d’une palette
description: Animation d’une palette
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, palettes
- DrawDibRealize fonction)
- DrawDibDraw fonction)
- DrawDibChangePalette fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726725"
---
# <a name="animating-a-palette"></a><span data-ttu-id="ccc45-107">Animation d’une palette</span><span class="sxs-lookup"><span data-stu-id="ccc45-107">Animating a Palette</span></span>

<span data-ttu-id="ccc45-108">L’exemple suivant anime une palette à l’aide des fonctions [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)et [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="ccc45-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="ccc45-109">Vous pouvez modifier les couleurs d’une image bitmap à l’aide de la fonction [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) en association avec [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span><span class="sxs-lookup"><span data-stu-id="ccc45-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="ccc45-110">Tout d’abord, pour autoriser les modifications de palette, spécifiez l' \_ indicateur d’animation DDF dans l’appel à **DrawDibBegin**.</span><span class="sxs-lookup"><span data-stu-id="ccc45-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="ccc45-111">Ensuite, définissez les valeurs de la table des couleurs à partir des entrées de palette à l’aide de **DrawDibChangePalette**.</span><span class="sxs-lookup"><span data-stu-id="ccc45-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="ccc45-112">Par exemple, si *LPPE* est une adresse du tableau [PaletteEntry](/previous-versions//ms532623(v=vs.85)) contenant les nouvelles couleurs, et *lpbi* est la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) utilisée dans [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) ou [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), le fragment suivant met à jour la table des couleurs dib.</span><span class="sxs-lookup"><span data-stu-id="ccc45-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="ccc45-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccc45-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc45-114">Utilisation de DrawDib</span><span class="sxs-lookup"><span data-stu-id="ccc45-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 