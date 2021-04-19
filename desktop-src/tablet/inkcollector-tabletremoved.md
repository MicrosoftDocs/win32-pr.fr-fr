---
description: Se produit lorsqu’un IInkTablet est supprimé du système.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Événement InkCollector. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec723a6752f79a1a1d56d318d49ec3d025919d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513399"
---
# <a name="inkcollectortabletremoved-event"></a>Événement InkCollector. TabletRemoved

Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimé du système.

## <a name="syntax"></a>Syntaxe


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TabletId* \[ dans\]
</dt> <dd>

Valeur de type long qui a été utilisée comme ID de l’objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletRemoved.

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
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




