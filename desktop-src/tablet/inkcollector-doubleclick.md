---
description: Se produit lors d’un double-clic sur l’objet InkCollector ou InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Événement InkCollector. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862094"
---
# <a name="inkcollectordoubleclick-event"></a>Événement InkCollector. DoubleClick

Se produit lors d’un double-clic sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Syntaxe


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEDblClick.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkCollector (classe)**](inkcollector-class.md)
</dt> </dl>

 

 




