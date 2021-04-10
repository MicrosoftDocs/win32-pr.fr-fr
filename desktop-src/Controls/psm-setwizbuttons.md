---
title: Message PSM_SETWIZBUTTONS (Prsht. h)
description: Active ou désactive les boutons précédent, suivant et terminer dans un Assistant. Vous pouvez également utiliser la \_ macro PropSheet SetWizButtons pour envoyer le message.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104194"
---
# <a name="psm_setwizbuttons-message"></a>\_Message PSM SETWIZBUTTONS

Active ou désactive les boutons **précédent**, **suivant** et **Terminer** dans un Assistant. Vous pouvez également utiliser la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour envoyer le message.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Définissez ce paramètre sur PSWIZBF \_ ELEVATIONREQUIRED pour afficher l’icône avec élévation de privilèges sur les boutons spécifiés dans *lParam*. L’icône avec élévation de privilèges (ou icône de blindage UAC) indique que l’invite d’élévation sera utilisée pour inviter l’utilisateur à approuver ou à fournir des informations d’identification. Pour plus d’informations, consultez [conception d’applications UAC pour Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> L’affichage de l’icône de bouclier UAC est pris en charge uniquement dans AeroWizards (PSH \_ AEROWIZARD).

 

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur qui spécifie les boutons de la feuille de propriétés qui sont activés. Vous pouvez combiner un ou plusieurs des indicateurs suivants.



| Valeur                                                                                                                                                                                 | Signification                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_**</dt> </dl>                               | Active le bouton **précédent** . Si cet indicateur n’est pas défini, le bouton **précédent** s’affiche comme étant désactivé.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Affiche un bouton **Terminer** désactivé.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ terminer**</dt> </dl>                         | Affiche un bouton **Terminer** activé.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ suivant**</dt> </dl>                               | Active le bouton **Suivant**. Si cet indicateur n’est pas défini, le bouton **suivant** s’affiche comme étant désactivé.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si votre gestionnaire de notifications utilise [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) pour envoyer un message **PSM \_ SETWIZBUTTONS** , ne faites rien qui affectera le focus de la fenêtre tant que le gestionnaire ne sera pas retourné. Par exemple, si vous appelez [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immédiatement après avoir utilisé **PostMessage** pour envoyer des **\_ SETWIZBUTTONS PSM**, la boîte de message reçoit le focus. Étant donné que les messages publiés ne sont pas remis tant qu’ils n’atteignent pas le début de la file d’attente de messages, le message **\_ SETWIZBUTTONS PSM** n’est pas remis tant que l’Assistant n’a pas perdu le focus sur la boîte de message. Par conséquent, la feuille de propriétés ne sera pas en mesure de définir correctement le focus pour les boutons.

Si vous envoyez le \_ message SETWIZBUTTONS PSM lors de la gestion de la notification [ \_ SetActive PSN](psn-setactive.md) , utilisez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) au lieu de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . Dans le cas contraire, le système ne met pas à jour les boutons correctement. Si vous utilisez la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour envoyer ce message, celui-ci sera publié. À tout moment, vous pouvez utiliser **SendMessage** pour envoyer des **\_ SETWIZBUTTONS PSM**.

Les assistants affichent trois ou quatre boutons sous chaque page. Ce message est utilisé pour spécifier les boutons qui sont activés. Les assistants s' **affichent** normalement, **annulent** et un bouton **suivant** ou **Terminer** . En général, vous activez uniquement le bouton **suivant** pour la page d’accueil, **suivant** et **précédent** pour les pages intérieures, et en **arrière** et en **fin** pour la page de fin. Le bouton **Annuler** est toujours activé. Normalement, la définition de PSWIZB \_ Finish ou PSWIZB \_ DISABLEDFINISH remplace le bouton **suivant** par un bouton **Terminer** . Pour afficher les boutons **suivant** et **Terminer** simultanément, définissez l' \_ indicateur PSH WIZARDHASFINISH dans le membre **dwFlags** de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) de l’Assistant lorsque vous créez l’Assistant. Chaque page affiche ensuite les quatre boutons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

