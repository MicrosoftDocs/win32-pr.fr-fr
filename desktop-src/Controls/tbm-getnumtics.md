---
title: Message TBM_GETNUMTICS (commctrl. h)
description: Récupère le nombre de graduations dans un TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941841"
---
# <a name="tbm_getnumtics-message"></a>\_Message TBM GETNUMTICS

Récupère le nombre de graduations dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si aucun [indicateur de graduation](trackbar-control-styles.md) n’est défini, la valeur 2 est retournée pour les graduations de début et de fin. Si la valeur de [**tbs \_ notiques**](trackbar-control-styles.md) est définie, elle retourne la valeur zéro. Sinon, elle prend la différence entre les valeurs minimale et maximale de la plage, se divise par la fréquence de graduation et ajoute 2.

## <a name="remarks"></a>Notes

Le message **TBM \_ GETNUMTICS** compte toutes les graduations, y compris les première et dernière graduations créées par le TrackBar.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





