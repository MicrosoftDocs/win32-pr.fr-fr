---
description: L’événement InkOverlay. TabletAdded-se produit lorsqu’un IInkTablet est ajouté au système.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: InkOverlay. TabletAdded, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23086ed2b2238a142a1b7f3116eb2cb86ba14ad90f758a9c15052f5b520be347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967088"
---
# <a name="inkoverlaytabletadded-event"></a>Événement InkOverlay. TabletAdded

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

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletAdded.

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

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




