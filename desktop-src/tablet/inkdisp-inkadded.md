---
description: Se produit lorsqu’un trait est ajouté à l’objet InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Événement InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522253"
---
# <a name="inkdispinkadded-event"></a>Événement InkDisp. InkAdded

Se produit lorsqu’un trait est ajouté à l’objet [**InkDisp**](inkdisp-class.md) .

## <a name="syntax"></a>Syntaxe


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StrokeIds* \[ dans\]
</dt> <dd>

Tableau d’entiers des informations d’ID de trait pour tous les traits qui ont été ajoutés lorsque cet événement se produit.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si vous utilisez l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) (où [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) est égal à [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) et [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) est égal à [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) et que vous transmettez la gomme sur un trait, vous recevez la séquence d’événements suivante :

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Les événements **InkAdded** et [**InkDeleted**](inkdisp-inkdeleted.md) supplémentaires se produisent parce que le code sous-jacent ajoute un trait invisible interne pour effectuer le suivi de la gomme.

Cette méthode d’événement est définie dans l' \_ interface IInkEvents. L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IEInkAdded.

L’événement **InkAdded** est déclenché même en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkDisp, classe**](inkdisp-class.md)
</dt> <dt>

[**Propriété EditingMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Propriété EraserMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**Événement InkDeleted**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[Référence du contrôle InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

