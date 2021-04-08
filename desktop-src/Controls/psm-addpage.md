---
title: Message PSM_ADDPAGE (Prsht. h)
description: Ajoute une nouvelle page à la fin d’une feuille de propriétés existante. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844030"
---
# <a name="psm_addpage-message"></a>Message de la \_ ADDPAGE PSM

Ajoute une nouvelle page à la fin d’une feuille de propriétés existante. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la page à ajouter. La page doit avoir été créée par un appel précédent à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La nouvelle page ne doit pas être supérieure à la plus grande page actuellement dans la feuille de propriétés, car la feuille de propriétés n’est pas redimensionnée pour s’ajuster à la nouvelle page.

Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages. Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles. En conséquence, vous ne devez pas utiliser le message de l' \_ PROPSHEETPAGEPROC PSM dans votre implémentation de [](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou lors de la gestion des notifications et des messages Windows suivants.

-   [PSN \_ appliquer](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_réinitialisation PSN](psn-reset.md)
-   [PSN \_](psn-setactive.md)
-   [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

Si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé. Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches. Vous pouvez ensuite modifier la liste des pages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

