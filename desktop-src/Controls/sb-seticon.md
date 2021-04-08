---
title: Message SB_SETICON (commctrl. h)
description: Définit l’icône d’un composant dans une barre d’État.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843997"
---
# <a name="sb_seticon-message"></a>\_Message SB SETICON

Définit l’icône d’un composant dans une barre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la partie qui recevra l’icône. Si ce paramètre a la valeur-1, la barre d’État est supposée être une barre d’état simple.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de l’icône à définir. Si cette valeur est **null**, l’icône est supprimée de la partie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

La barre d’État ne détruit pas l’icône. Il incombe à l’application appelante d’effectuer le suivi et de détruire les icônes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





