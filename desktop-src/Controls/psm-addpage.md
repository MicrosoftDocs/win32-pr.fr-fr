---
title: Message PSM_ADDPAGE (Prsht. h)
description: Ajoute une nouvelle page à la fin d’une feuille de propriétés existante. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE les contrôles de Windows de message
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
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169825"
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

## <a name="remarks"></a>Remarques

La nouvelle page ne doit pas être supérieure à la plus grande page actuellement dans la feuille de propriétés, car la feuille de propriétés n’est pas redimensionnée pour s’ajuster à la nouvelle page.

Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages. Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles. en conséquence, vous ne devez pas utiliser le message de l' \_ PropSheetPageProc PSM dans votre implémentation de [](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou lors de la gestion des notifications et des messages Windows suivants.

-   [PSN \_ appliquer](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_réinitialisation PSN](psn-reset.md)
-   [PSN \_](psn-setactive.md)
-   [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé. Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches. Vous pouvez ensuite modifier la liste des pages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

