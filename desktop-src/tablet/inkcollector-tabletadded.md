---
description: Événement InkCollector. TabletAdded-se produit lorsqu’un IInkTablet est ajouté au système.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Événement InkCollector. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220057"
---
# <a name="inkcollectortabletadded-event"></a>Événement InkCollector. TabletAdded

Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajouté au système.

## <a name="syntax"></a>Syntaxe


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Tablette* \[ dans\]
</dt> <dd>

Objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été ajouté au système.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletAdded.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkCollector (classe)**](inkcollector-class.md)
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




