---
title: Message TBM_GETPTICS (commctrl. h)
description: Récupère l’adresse d’un tableau qui contient les positions des graduations d’un TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942161"
---
# <a name="tbm_getptics-message"></a>\_Message TBM GETPTICS

Récupère l’adresse d’un tableau qui contient les positions des graduations d’un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’adresse d’un tableau de valeurs **DWORD** . Les éléments du tableau spécifient les positions logiques des graduations de la barre de suivi, à l’exclusion des première et dernière graduations créées par le TrackBar. Les positions logiques peuvent être n’importe laquelle des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

## <a name="remarks"></a>Notes

Le nombre d’éléments dans le tableau est inférieur au nombre de cycles renvoyé par le message [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) . Notez que les valeurs du tableau peuvent inclure des positions en double et peuvent ne pas être dans l’ordre séquentiel. Le pointeur retourné est valide jusqu’à ce que vous modifiiez les graduations de la barre de défilement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





