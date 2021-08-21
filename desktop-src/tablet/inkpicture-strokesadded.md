---
description: Se produit lorsqu’un ou plusieurs objets IInkStrokeDisp sont ajoutés à la collection InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: InkPicture. StrokesAdded, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5f9418289ac996b2c2248c2cf1696e7d45b4548dbafa4dff9494e76cbedc30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717402"
---
# <a name="inkpicturestrokesadded-event"></a>InkPicture. StrokesAdded, événement

Se produit lorsqu’un ou plusieurs objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) sont ajoutés à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

## <a name="syntax"></a>Syntaxe


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StrokeIds* \[ dans\]
</dt> <dd>

Tableau d’entiers des identificateurs pour chaque objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ajouté lorsque cet événement se produit.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkStrokesEvents** . L’interface **\_ IInkStrokesEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ SEStrokesAdded.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

