---
description: Se produit après la suppression des objets IInkStrokeDisp de la propriété Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: InkPicture. StrokesDeleted, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b2d4f0be69adf6c9c44f3eadec250d8cba3ebb8935bde5c06cd026e478da3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717358"
---
# <a name="inkpicturestrokesdeleted-event"></a>InkPicture. StrokesDeleted, événement

Se produit après la suppression des objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .

## <a name="syntax"></a>Syntaxe


```C++
void StrokesDeleted();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Il n’y a aucune donnée d’événement.

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOEStrokesDeleted.

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

 

 




