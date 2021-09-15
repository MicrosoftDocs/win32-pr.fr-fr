---
description: Se produit lorsqu’un ou plusieurs traits sont supprimés de la collection InkStrokes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Événement InkStrokes. StrokesRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412280"
---
# <a name="inkstrokesstrokesremoved-event"></a>Événement InkStrokes. StrokesRemoved

Se produit lorsqu’un ou plusieurs traits sont supprimés de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

## <a name="syntax"></a>Syntaxe


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StrokeIds* \[ dans\]
</dt> <dd>

Tableau d’entiers des identificateurs pour chaque objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) supprimé lorsque cet événement se produit.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l' \_ interface IInkEvents. L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ SEStrokesRemoved.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Supprimer la méthode \[ InkStrokes collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**InkDisp, classe**](inkdisp-class.md)
</dt> </dl>

 

