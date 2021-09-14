---
title: Message TBM_GETTICPOS (commctrl. h)
description: Récupère la position physique actuelle d’une graduation dans un TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116429"
---
# <a name="tbm_getticpos-message"></a>\_Message TBM GETTICPOS

Récupère la position physique actuelle d’une graduation dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro identifiant une graduation. Les positions des première et dernière graduations ne sont pas directement disponibles par le biais de ce message.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la distance, en coordonnées clientes, à partir de la gauche ou du haut de la zone cliente du TrackBar jusqu’à la graduation spécifiée. La valeur de retour est la coordonnée x de la graduation pour un TrackBar horizontal ou la coordonnée y pour un TrackBar vertical. Si *wParam* n’est pas un index valide, la valeur de retour est-1.

## <a name="remarks"></a>Notes

Étant donné que les première et dernière graduations ne sont pas disponibles par le biais de ce message, les index valides sont décalés par rapport à leur position de graduation sur le TrackBar. Si la différence entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) et [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) est inférieure à deux, alors il n’y a pas d’index valide et ce message échoue.

L’exemple suivant illustre la relation entre les graduations sur un TrackBar, les graduations disponibles dans ce message et leurs index de base zéro.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





