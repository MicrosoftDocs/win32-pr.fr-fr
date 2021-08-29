---
description: Se produit lorsque le contenu du contrôle InkEdit change.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Événement InkEdit. change (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3679b32b633a9983cc239fdf232491ce13b7805c053c9e1c268c84b9932586ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712969"
---
# <a name="inkeditchange-event"></a>InkEdit. change (événement)

Se produit lorsque le contenu du contrôle [InkEdit](inkedit-control-reference.md) change.

## <a name="syntax"></a>Syntaxe


```C++
void Change();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cet événement se produit chaque fois qu’une propriété qui affecte le contenu du contrôle [InkEdit](inkedit-control-reference.md) change.

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IeeChange**.

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

 

 




