---
title: Message TDM_UPDATE_ICON (commctrl. h)
description: Actualise l’icône d’une boîte de dialogue de tâche.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116053"
---
# <a name="tdm_update_icon-message"></a>\_Message d’icône de mise à jour TDM \_

Actualise l’icône d’une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Indique l’élément d’icône à mettre à jour. Ce paramètre doit avoir l’une des valeurs suivantes :



| Valeur                                                                                                                                                                   | Signification                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**TDIE \_ icône \_ main**</dt> </dl>       | Icône principale.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**pied de page de l' \_ icône TDIE \_**</dt> </dl> | Icône de pied de page.<br/> |



 

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne (PCWSTR) ou handle vers une icône (HICON) à afficher. Si *lParam* a la valeur **null**, aucune icône n’est affichée, quelle que soit la valeur de *wParam*.

Si la valeur de *wParam* est TDIE \_ Icon \_ main et que l' \_ indicateur de main TDF use \_ HICON \_ est défini sur le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche, *lParam* doit contenir un handle vers une icône (HICON) à afficher.

Si la valeur de *wParam* est le \_ pied de page de l’icône TDIE \_ et que l' \_ indicateur de pied de page TDF use \_ HICON \_ est défini sur le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche, *lParam* doit contenir un handle vers une icône (HICON) à afficher.

Si les \_ indicateurs TDF utilisent les \_ \_ \_ indicateurs de pied de page HICON main ou TDF use \_ HICON ne \_ sont **pas** définis sur le membre **DwFlags** , *lParam* doit pointer vers une chaîne Unicode terminée par le caractère null (PCWSTR) qui contient un identificateur de ressource valide passé par la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . L’icône s’affiche en fonction de la valeur de *wParam*: si la valeur est TDIE \_ icône \_ main, l’icône s’affiche dans l’en-tête ; si la valeur est TDIE \_ icône pied de \_ page, l’icône s’affiche dans le pied de page. La ressource doit être à partir du module de ressources de l’application (spécifié dans le membre **HINSTANCE** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ), ou si **HINSTANCE** a la **valeur null**, à partir du module de ressources du système (imageres.dll). Pour identifier une ressource système, utilisez un identificateur système valide passé par la macro **MAKEINTRESOURCE** ou l’une des valeurs prédéfinies suivantes de commctrl. h :



| Valeur                                                                                                                                                                            | Signification                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_icône d’erreur TD \_**</dt> </dl>                   | Icône de signe stop.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**\_icône d’avertissement TD \_**</dt> </dl>             | Icône de point d’exclamation.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**\_icône d’informations TD \_**</dt> </dl> | Lettre minuscule « i » dans une icône de cercle.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**\_icône de bouclier TD \_**</dt> </dl>                | Icône de bouclier de sécurité.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

La disposition de la boîte de dialogue de tâche avec l’icône peut échouer et ne pas être reflétée dans la valeur de retour. Une valeur de retour de S \_ OK reflète uniquement que la boîte de dialogue de tâche a reçu le message et a tenté de le traiter. Si la disposition de la boîte de dialogue de tâche échoue, la boîte de dialogue se ferme et un code **HRESULT** est retourné au niveau de la fonction de rappel inscrite. Pour plus d’informations sur la syntaxe de la fonction de rappel, consultez [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Si la boîte de dialogue de tâche est créée sans pied de page (autrement dit, les membres de pied de page appropriés de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche ont la **valeur null**) et que ce message est envoyé, un pied de page n’est pas ajouté dynamiquement à la boîte de dialogue de tâche. Il en va de même pour l’envoi de ce message afin de mettre à jour une icône d’en-tête lorsqu’une boîte de dialogue de tâche est créée sans en-tête. Pour ajouter un en-tête ou un pied de page au moment de l’exécution, utilisez la fonctionnalité de [**\_ \_ page de navigation TDM**](tdm-navigate-page.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

