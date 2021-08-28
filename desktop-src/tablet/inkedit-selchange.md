---
description: Se produit lorsque la sélection actuelle de texte dans le contrôle InkEdit a changé ou que le point d’insertion a été déplacé.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Événement InkEdit. SelChange (. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712649"
---
# <a name="inkeditselchange-event"></a>Événement InkEdit. SelChange

Se produit lorsque la sélection actuelle de texte dans le contrôle [InkEdit](inkedit-control-reference.md) a changé ou que le point d’insertion a été déplacé.

## <a name="syntax"></a>Syntaxe


```C++
void SelChange();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’événement **SelChange** pour vérifier les différentes propriétés qui fournissent des informations sur la sélection actuelle (par exemple, [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) afin de pouvoir mettre à jour les boutons dans une barre d’outils, par exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




