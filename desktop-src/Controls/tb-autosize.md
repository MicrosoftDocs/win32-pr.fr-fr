---
title: Message TB_AUTOSIZE (commctrl. h)
description: Entraîne le redimensionnement d’une barre d’outils.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519313"
---
# <a name="tb_autosize-message"></a>\_Message de REdimensionnement automatique to

Entraîne le redimensionnement d’une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Une application envoie le message de **\_ taille automatique to** après avoir entraîné la modification de la taille d’une barre d’outils en définissant la taille du bouton ou de la bitmap, ou en ajoutant des chaînes pour la première fois.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





