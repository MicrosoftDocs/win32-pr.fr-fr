---
description: L’événement InkPicture. CursorOutOfRange se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: InkPicture. CursorOutOfRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086567"
---
# <a name="inkpicturecursoroutofrange-event"></a>InkPicture. CursorOutOfRange, événement

Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.

## <a name="syntax"></a>Syntaxe


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorOutOfRange** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICECursorOutOfRange.

L’événement **CursorOutOfRange** est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Événement CursorInRange**](inkpicture-cursorinrange.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




