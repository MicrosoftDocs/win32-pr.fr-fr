---
description: Le \_ message WM SPOOLERSTATUS est envoyé à partir du gestionnaire d’impression chaque fois qu’un travail est ajouté ou supprimé de la file d’attente du gestionnaire d’impression.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Message WM_SPOOLERSTATUS (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115686"
---
# <a name="wm_spoolerstatus-message"></a>\_Message WM SPOOLERSTATUS

Le message **WM \_ SPOOLERSTATUS** est envoyé à partir du gestionnaire d’impression chaque fois qu’un travail est ajouté ou supprimé de la file d’attente du gestionnaire d’impression.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur PR \_ JOBSTATUS.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie le nombre de travaux restant dans la file d’attente du gestionnaire d’impression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Ce message est fourni à titre d’information uniquement. Ce message est un avis et n’a pas de sémantique de remise garantie. Les applications ne doivent pas supposer qu’elles recevront un \_ message WM SPOOLERSTATUS pour chaque modification de l’état du spouleur.

Le \_ message WM SPOOLERSTATUS n’est pas pris en charge après Windows XP. Pour être averti des modifications apportées à l’état de la file d’attente à l’impression, vous pouvez utiliser [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) et [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Messages d’API du spouleur d’impression](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

