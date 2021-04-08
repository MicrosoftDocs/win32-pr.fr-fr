---
title: Message PSM_REMOVEPAGE (Prsht. h)
description: Supprime une page d'une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844025"
---
# <a name="psm_removepage-message"></a>\_Message PSM REMOVEPAGE

Supprime une page d'une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la page à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle HPROPSHEETPAGE de la page à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Une application peut spécifier l’index ou le descripteur, ou les deux. Si les deux sont spécifiés, *lParam* est prioritaire.

L’envoi de **\_ REMOVEPAGE PSM** détruit la page de la feuille de propriétés qui est supprimée.

Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages. Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles. En conséquence, vous ne devez pas utiliser le message **PSM \_ REMOVEPAGE** dans votre implémentation de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou pendant la gestion des notifications et des messages Windows suivants.

-   [PSN \_ appliquer](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_réinitialisation PSN](psn-reset.md)
-   [PSN \_](psn-setactive.md)
-   [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

Si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé. Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches. Vous pouvez ensuite modifier la liste des pages.

Les notifications suivantes sont également affectées par la modification de la feuille de propriétés.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Vous pouvez ajouter ou supprimer des pages en réponse à ces notifications, à condition que vous reveniez (via DWL \_ MSGRESULT) une valeur différente de zéro pour spécifier la nouvelle page souhaitée. Notez, toutefois, que si vous supprimez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

