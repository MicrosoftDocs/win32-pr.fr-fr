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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007291"
---
# <a name="animating-a-palette"></a>Animation d’une palette

L’exemple suivant anime une palette à l’aide des fonctions [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)et [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

Vous pouvez modifier les couleurs d’une image bitmap à l’aide de la fonction [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) en association avec [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette). Tout d’abord, pour autoriser les modifications de palette, spécifiez l' \_ indicateur d’animation DDF dans l’appel à **DrawDibBegin**. Ensuite, définissez les valeurs de la table des couleurs à partir des entrées de palette à l’aide de **DrawDibChangePalette**.

Par exemple, si *LPPE* est une adresse du tableau [PaletteEntry](/previous-versions//ms532623(v=vs.85)) contenant les nouvelles couleurs, et *lpbi* est la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) utilisée dans [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) ou [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), le fragment suivant met à jour la table des couleurs dib.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DrawDib](using-drawdib.md)
</dt> </dl>

 

 