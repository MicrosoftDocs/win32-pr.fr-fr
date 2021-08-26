---
title: Message PSM_INSERTPAGE (Prsht. h)
description: Insère une nouvelle page dans une feuille de propriétés existante. La page peut être insérée à un index spécifié ou après une page spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11c81869b1ca575efa960fc00eea09536ca4b6b2f43a5e637c5dc6a9d7632983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985661"
---
# <a name="psm_insertpage-message"></a>\_Message PSM INSERTPAGE

Insère une nouvelle page dans une feuille de propriétés existante. La page peut être insérée à un index spécifié ou après une page spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Où la page doit être insérée. Affectez la valeur **null** à ce paramètre pour faire de la nouvelle page la première page. Pour spécifier l’emplacement où la nouvelle page doit être insérée, vous pouvez passer un index ou le handle HPROPSHEETPAGE d’une page existante.



| Valeur                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>index</dt> </dl>            | Si le paramètre *wParam* est inférieur à MAXUSHORT (l’entier Short non signé le plus grand), *wParam* spécifie l’index de base zéro de la nouvelle page. Par exemple, pour faire de la page insérée la troisième page sur la feuille de propriétés, affectez la valeur 2 à *wParam* . Pour en faire la première page, affectez la valeur 0 à *wParam* . Si *wParam* a une valeur supérieure au nombre de pages et inférieure à MAXUSHORT, la page est ajoutée.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Si vous définissez le paramètre *wParam* sur le handle HPROPSHEETPAGE d’une page existante, la nouvelle page est insérée après celle-ci.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la page à insérer. La page doit d’abord être créée par un appel à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si la page a été correctement insérée, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Les pages après le point d’insertion sont décalées vers la droite pour s’adapter à la nouvelle page.

La feuille de propriétés n’est pas redimensionnée pour s’ajuster à la nouvelle page. Ne rendez pas la nouvelle page plus grande que la page la plus grande de la feuille de propriétés.

Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages. Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles. en conséquence, vous ne devez pas utiliser le \_ message PSM INSERTPAGE dans votre implémentation de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou pendant la gestion des notifications et des messages Windows suivants.

-   [PSN \_ appliquer](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_réinitialisation PSN](psn-reset.md)
-   [PSN \_](psn-setactive.md)
-   [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé. Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches. Vous pouvez ensuite modifier la liste des pages.

Les notifications suivantes sont également affectées par la modification de la feuille de propriétés.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Vous pouvez ajouter ou supprimer des pages en réponse à ces notifications, à condition que vous reveniez (via DWL \_ MSGRESULT) une valeur différente de zéro pour spécifier la nouvelle page souhaitée. Notez, toutefois, que si vous insérez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

