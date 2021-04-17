---
title: TBN_RESTORE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours de restauration. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Contrôles Windows de code de notification TBN_RESTORE
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466219"
---
# <a name="tbn_restore-notification-code"></a>TBN le \_ Code de notification de restauration

Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours de restauration. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application doit retourner zéro en réponse au premier code de notification de **\_ restauration TBN** reçu au début du processus de restauration pour continuer à restaurer les informations du bouton. Si l’application retourne une valeur différente de zéro, le processus de restauration est annulé.

## <a name="remarks"></a>Notes

L’application recevra ce code de notification une fois au démarrage du processus de restauration et une fois pour chaque bouton. Ce code de notification vous donne la possibilité d’extraire les informations du flux de données que vous avez enregistré précédemment. Si vous n’avez enregistré aucune information, ignorez le code de notification. Pour plus d’informations sur la façon de gérer **TBN \_ Restore**, consultez Personnalisation de la [barre d’outils](toolbar-controls-overview.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





