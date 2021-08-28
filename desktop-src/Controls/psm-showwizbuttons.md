---
title: Message PSM_SHOWWIZBUTTONS (Prsht. h)
description: Affiche ou masque les boutons dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bbad4d6f0ce8a084709c04110d093e4d79b806226bdc1fa651278b4054fa8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088479"
---
# <a name="psm_showwizbuttons-message"></a>\_Message PSM SHOWWIZBUTTONS

Affiche ou masque les boutons dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Une ou plusieurs des valeurs suivantes qui spécifient les boutons de la feuille de propriétés à afficher. Si une valeur de bouton est incluse à la fois dans ce paramètre et dans *lParam*, elle est affichée.



| Valeur                                                                                                                                                                                 | Signification                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_**</dt> </dl>                               | Bouton **précédent** .<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ Annuler**</dt> </dl>                         | Bouton **Annuler** .<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Bouton **Terminer** .<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ terminer**</dt> </dl>                         | Bouton **Terminer** .<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ suivant**</dt> </dl>                               | Bouton **suivant** .<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ afficher**</dt> </dl>                               | Définit uniquement cet indicateur (défini comme zéro) pour masquer tous les boutons spécifiés dans *lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**\_restauration PSWIZB**</dt> </dl>                      | Non implémenté.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Une ou plusieurs des valeurs utilisées dans *wParam*, en spécifiant les boutons affectés par cet appel. Si une valeur de bouton apparaît dans ce paramètre mais pas dans *wParam*, le bouton est masqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les assistants affichent trois ou quatre boutons sous chaque page. Ce message est utilisé pour spécifier les boutons à afficher. Les assistants s' **affichent** normalement, **annulent** et un bouton **suivant** ou **Terminer** . Le bouton **Annuler** est toujours visible.

En règle générale, définissez **PSWIZB \_ Finish** ou **PSWIZB \_ DISABLEDFINISH** pour remplacer le bouton **Next** par un bouton **Finish** . Pour afficher les boutons **suivant** et **Terminer** simultanément, définissez l’indicateur **PSH \_ WIZARDHASFINISH** dans le membre **dwFlags** de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) lorsque vous créez l’Assistant. Chaque page affiche ensuite les quatre boutons suivants : **précédent**, **suivant**, **Annuler** et **Terminer**.

Si vous utilisez la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) pour envoyer ce message, celui-ci sera publié. À tout moment, vous pouvez utiliser [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour envoyer des **\_ SHOWWIZBUTTONS PSM**.

Si votre gestionnaire de notifications utilise [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) pour envoyer un message **PSM \_ SHOWWIZBUTTONS** , ne faites rien qui affectera le focus de la fenêtre tant que le gestionnaire ne sera pas retourné. Par exemple, si vous appelez [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immédiatement après avoir utilisé **PostMessage** pour envoyer des **\_ SHOWWIZBUTTONS PSM**, la boîte de message reçoit le focus. Étant donné que les messages publiés ne sont pas remis tant qu’ils n’atteignent pas le début de la file d’attente de messages, le message **\_ SHOWWIZBUTTONS PSM** n’est pas remis tant que l’Assistant n’a pas perdu le focus sur la boîte de message. Par conséquent, la feuille de propriétés ne sera pas en mesure de définir correctement le focus pour les boutons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

