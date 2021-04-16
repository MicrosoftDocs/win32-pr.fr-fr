---
title: Message ACM_PLAY (commctrl. h)
description: Lit un clip AVI dans un contrôle d’animation. Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro animer \_ Play.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464670"
---
# <a name="acm_play-message"></a>\_Message de lecture ACM

Lit un clip AVI dans un contrôle d’animation. Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro [**animer \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Uint** qui spécifie le nombre de relectures du clip avi. La valeur-1 signifie relire indéfiniment le clip.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est l’index de base zéro de la trame dans laquelle la fonction Play commence. La valeur doit être inférieure à 65 536. La valeur zéro signifie que commence par la première image du clip AVI.

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est l’index de base zéro de la trame où la séquence se termine. La valeur doit être inférieure à 65 536. La valeur-1 signifie qu’elle se termine par la dernière image du clip AVI.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Vous pouvez utiliser [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) pour indiquer au contrôle d’animation d’afficher un cadre particulier du clip avi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

