---
description: Structure qui décrit une seule valeur de couleur.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521376"
---
# <a name="xps_color"></a>\_couleur XPS

Structure qui décrit une seule valeur de couleur.

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a>Notes

Le format de la structure dépend de la valeur de *colorType*.

<dl>

[**\_type de couleur XPS \_ \_ sRVB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**\_type de couleur XPS \_ \_ ScRVB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**\_contexte du \_ type de couleur XPS \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| En-tête<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                              |
| MIDL<br/>                      | <dl> <dt>XpsObjectModel. idl</dt> </dl>                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

