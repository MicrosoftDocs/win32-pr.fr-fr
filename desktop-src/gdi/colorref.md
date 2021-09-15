---
Description: La valeur COLORREF est utilisée pour spécifier une couleur RVB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (WINDEF. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525877"
---
# <a name="colorref"></a>COLORREF

La valeur COLORREF est utilisée pour spécifier une couleur [RVB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Notes

Lorsque vous spécifiez une couleur [RVB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) explicite, la valeur **COLORREF** est au format hexadécimal suivant :

`0x00bbggrr`

L’octet de poids faible contient une valeur pour l’intensité relative du rouge ; le deuxième octet contient une valeur pour le vert ; et le troisième octet contient une valeur pour le bleu. L’octet de poids fort doit être égal à zéro. La valeur maximale d’un seul octet est 0xFF.

Pour créer une valeur de couleur **COLORREF** , utilisez la macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Pour extraire les valeurs individuelles des composants rouge, vert et bleu d’une valeur de couleur, utilisez respectivement les macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)et [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .

## <a name="example"></a>Exemple

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples) sur GitHub.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>Windef. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des couleurs](colors.md)
</dt> <dt>

[Structures de couleurs](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




