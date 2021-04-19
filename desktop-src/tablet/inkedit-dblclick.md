---
description: Se produit lors d’un double-clic sur le contrôle InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Événement InkEdit. DblClick (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528339"
---
# <a name="inkeditdblclick-event"></a>InkEdit. DblClick, événement

Se produit lors d’un double-clic sur le contrôle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void DblClick(
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

> [!Note]  
> Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) . Si l’événement [**Click**](inkedit-click.md) contient du code, l’événement **DblClick** ne se déclenchera jamais.

 

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IeeDblClick**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




