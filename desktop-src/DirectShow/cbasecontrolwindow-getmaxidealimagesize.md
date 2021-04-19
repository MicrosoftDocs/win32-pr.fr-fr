---
description: La méthode GetMaxIdealImageSize récupère la taille d’image maximale idéale.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Méthode CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541117"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a>Méthode CBaseControlWindow. GetMaxIdealImageSize

La `GetMaxIdealImageSize` méthode récupère la taille d’image idéale maximale.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la largeur idéale maximale, en pixels.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la hauteur maximale idéale, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Différents convertisseurs présentent des restrictions de performances quant à la taille des images qu’ils peuvent afficher. Bien qu’ils doivent toujours fonctionner correctement lorsqu’ils sont invités à afficher des images plus volumineuses que la valeur maximale spécifiée, les convertisseurs peuvent désigner les tailles idéales minimales et maximales par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Cette interface peut être appelée uniquement lorsque le graphique de filtre est suspendu ou en cours d’exécution, car ce n’est pas jusqu’à ce que les ressources soient allouées et que le convertisseur puisse reconnaître ses restrictions. S’il n’existe aucune restriction, le convertisseur remplit les paramètres *pWidth* et *pHeight* avec les dimensions Native Video et retourne S \_ false. S’il existe des restrictions, la largeur et la hauteur restreintes sont entrées, et la fonction membre retourne S \_ OK.

Les dimensions s’appliquent à la taille de la vidéo de destination et non à la taille globale de la fenêtre. Ainsi, lors du calcul de la taille de la fenêtre à définir, comptez pour les styles de fenêtre actuels (par exemple, WS \_ Caption et WS \_ Border).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




