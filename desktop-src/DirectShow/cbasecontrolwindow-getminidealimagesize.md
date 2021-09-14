---
description: La méthode GetMinIdealImageSize récupère la taille d’image minimale idéale.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Méthode CBaseControlWindow. GetMinIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923892"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>Méthode CBaseControlWindow. GetMinIdealImageSize

La `GetMinIdealImageSize` méthode récupère la taille d’image minimale idéale.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la largeur minimale idéale, en pixels.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la hauteur minimale idéale, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Différents convertisseurs présentent des restrictions de performances quant à la taille des images qu’ils peuvent afficher. Bien qu’ils doivent toujours fonctionner correctement lorsqu’ils sont invités à afficher des images plus volumineuses que la valeur maximale spécifiée, les convertisseurs peuvent désigner les tailles idéales minimales et maximales par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Cette interface peut être appelée uniquement lorsque le graphique de filtre est suspendu ou en cours d’exécution, car ce n’est pas jusqu’à ce que les ressources soient allouées et que le convertisseur puisse reconnaître ses restrictions. S’il n’existe aucune restriction, le convertisseur remplit les paramètres *pWidth* et *pHeight* avec les dimensions Native Video et retourne S \_ false. S’il existe des restrictions, la largeur et la hauteur restreintes sont entrées, et la fonction membre retourne S \_ OK.

Les dimensions s’appliquent à la taille de la vidéo de destination et non à la taille globale de la fenêtre. Ainsi, lors du calcul de la taille de la fenêtre à définir, comptez pour les styles de fenêtre actuels (par exemple, WS \_ Caption et WS \_ Border).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




