---
title: Méthode ID2D1CommandSink1 SetPrimitiveBlend1
description: Définit un nouveau mode de fusion primitif.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1, méthode Direct2D
- Méthode SetPrimitiveBlend1 Direct2D, interface ID2D1CommandSink1
- ID2D1CommandSink1, méthode SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113053"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>ID2D1CommandSink1 :: SetPrimitiveBlend1, méthode

Définit un nouveau mode de fusion primitif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*primitiveBlend* 
</dt> <dd>

Type : **[ **d2d1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

Fusion primitive qui s’appliquera aux primitives suivantes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si la méthode est réussie, elle retourne la valeur **\_ OK**. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

### <a name="blend-modes"></a>Modes de fusion

Pour le rendu avec alias (à l’exception du mode MIN), la valeur de sortie O est calculée en interpolant de manière linéaire la valeur *Blend (S, D)* avec la valeur de pixel de destination, en fonction de la quantité de la primitive qui couvre le pixel de destination.

Le tableau ci-dessous montre les modes de fusion primitifs pour la fusion avec alias et l’anticrénelage. Les équations figurant dans le tableau utilisent les éléments suivants :

-   O = sortie
-   S = source
-   SA = source alpha
-   D = destination
-   DA = alpha de destination
-   C = couverture en pixels



| Mode de fusion primitif                 | Fusion avec alias                            | Fusion avec anticrénelage            | Description                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| \_Source de \_ fusion primitive d2d1 \_ \_ sur | O = (S + (1 SA) \* D) \* C + D \* (1 c) | O = S \* C + D \* (1 sa \* c)   | Mode de fusion standard de la source sur la destination.                                                                         |
| \_Copie de \_ fusion \_ primitive d2d1         | O = S \* C + D \* (1 c)                   | O = S \* C + D \* (1 c)       | La source est copiée vers la destination ; les pixels de destination sont ignorés.                                             |
| D2D1 \_ primitive \_ fusion \_ min.          | O = min (S + 1-SA, D)                        | O = min (S \* c + 1 sa \* c, D) | Les valeurs de pixel obtenues utilisent la valeur minimale des valeurs de pixel source et de destination. disponible dans Windows 8 et versions ultérieures. |
| \_Ajouter un \_ mélange \_ primitif d2d1          | O = (S + D) \* C + d \* (1 c)             | O = S \* C + D                  | Les valeurs de pixel obtenues sont la somme des valeurs de pixel source et de destination. disponible dans Windows 8 et versions ultérieures.     |



 

![illustration des modes de fusion primitifs de Direct2D avec l’opacité et l’arrière-plan variables.](images/primblenddemo.png)

Illustration des modes de fusion primitifs avec l’opacité et l’arrière-plan variables.

La fusion primitive s’applique à toute la primitive dessinée sur le contexte, sauf si elle est remplacée par le paramètre *compositeMode* sur l’API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .

La fusion primitive s’applique à l’intérieur des primitives dessinées sur le contexte. Dans le cas de [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), cela sera implicite par le rectangle d’image, le décalage et la transformation universelle.

Si la fusion primitive est différente de **d2d1 \_ primitive \_ Blend \_** , le rendu ClearType sera désactivé. Si l’application force explicitement le rendu ClearType dans ces modes, le contexte de dessin sera placé dans un état d’erreur. D2DERR \_ \_ un état incorrect est retourné à partir de [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou de [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

