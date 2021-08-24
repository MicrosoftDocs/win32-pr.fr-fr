---
description: Se produit avant la suppression des traits de la propriété Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: InkOverlay. StrokesDeleting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85e01eabc46e8e9cc4ca844ae8f5efa8b58e83fdee2724792a3856445b7dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712669"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Événement InkOverlay. StrokesDeleting

Se produit avant la suppression des traits de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .

## <a name="syntax"></a>Syntaxe


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Traits* \[ dans\]
</dt> <dd>

Collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) supprimée lorsque l’événement **StrokesDeleting** est déclenché.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEStrokesDeleting.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[**Propriété Ink, \[ classe InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

