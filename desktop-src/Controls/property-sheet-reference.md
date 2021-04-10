---
title: Feuille de propriétés
description: Cette section contient des informations sur la programmation des éléments utilisés avec les feuilles de propriétés.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c42b7b4c1be7d0dc11613da36f78abbad847d6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941387"
---
# <a name="property-sheet"></a>Feuille de propriétés

Cette section contient des informations sur la programmation des éléments utilisés avec les feuilles de propriétés.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                              | Contenu                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [À propos des feuilles de propriétés](property-sheets.md)       | Une *feuille de propriétés* est une fenêtre qui permet à l’utilisateur d’afficher et de modifier les propriétés d’un élément.<br/>                  |
| [Création d’assistants](wizards.md)                    | Un Assistant est un type de feuille de propriétés qui offre un moyen simple et puissant pour guider les utilisateurs dans une procédure.<br/> |
| [Utilisation des feuilles de propriétés](using-property-sheets.md) | Cette section fournit des détails d’implémentation et un exemple de code pour l’utilisation des feuilles de propriétés.<br/>                     |



 

### <a name="functions"></a>Fonctions



| Rubrique                                                        | Contenu                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Spécifie une fonction de rappel définie par l’application qu’une extension de feuille de propriétés utilise pour ajouter une page à une feuille de propriétés.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Crée une nouvelle page pour une feuille de propriétés.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Détruit une page de feuille de propriétés. Une application doit appeler cette fonction pour les pages qui n’ont pas été passées à la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .<br/>                                                                              |
| [**Feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Crée une feuille de propriétés et ajoute les pages définies dans la structure d’en-tête de la feuille de propriétés spécifiée.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Spécifie une fonction de rappel définie par l’application qu’une feuille de propriétés appelle lorsqu’une page est créée et lorsqu’elle est sur le lieu d’être détruite. Une application peut utiliser cette fonction pour effectuer des opérations d’initialisation et de nettoyage pour la page.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Fonction de rappel définie par l’application que le système appelle lorsque la feuille de propriétés est créée et initialisée.<br/>                                                                                                                        |



 

### <a name="messages"></a>Messages



| Rubrique                                                               | Contenu                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**la \_ ADDPAGE PSM**](psm-addpage.md)                                 | Ajoute une nouvelle page à la fin d’une feuille de propriétés existante. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .<br/>                                                                                                |
| [**\_application PSM**](psm-apply.md)                                     | Simule la sélection du bouton **appliquer** , indiquant qu’une ou plusieurs pages ont été modifiées et que les modifications doivent être validées et enregistrées.<br/>                                                                                                                   |
| [**\_CANCELTOCLOSE PSM**](psm-canceltoclose.md)                     | Envoyé par une application lorsqu’elle a effectué des modifications depuis la dernière notification d' [ \_ application PSN](psn-apply.md) qui ne peut pas être annulée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .<br/> |
| [**PSM \_ modifié**](psm-changed.md)                                 | Informe une feuille de propriétés que les informations d’une page ont été modifiées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .<br/>                                                                                         |
| [**\_ENABLEWIZBUTTONS PSM**](psm-enablewizbuttons.md)               | Active ou désactive tous les boutons standard dans un Assistant Aero. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .<br/>                                                                          |
| [**\_GETCURRENTPAGEHWND PSM**](psm-getcurrentpagehwnd.md)           | Récupère un handle de la fenêtre de la page active d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .<br/>                                                          |
| [**PSM- \_ GETRESULT**](psm-getresult.md)                             | Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Vous pouvez envoyer ce message explicitement ou utiliser la macro [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .<br/>                 |
| [**\_GETTABCONTROL PSM**](psm-gettabcontrol.md)                     | Récupère le handle du contrôle onglet d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .<br/>                                                                                 |
| [**\_HWNDTOINDEX PSM**](psm-hwndtoindex.md)                         | Prend le handle de fenêtre de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .<br/>                                                                  |
| [**\_IDTOINDEX PSM**](psm-idtoindex.md)                             | Prend l’ID de ressource d’une page de feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .<br/>                                                                          |
| [**\_INDEXTOHWND PSM**](psm-indextohwnd.md)                         | Prend l’index d’une page de feuille de propriétés et retourne son handle de fenêtre. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .<br/>                                                                               |
| [**\_INDEXTOID PSM**](psm-indextoid.md)                             | Prend l’index d’une page de feuille de propriétés et retourne son ID de ressource. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .<br/>                                                                                     |
| [**\_INDEXTOPAGE PSM**](psm-indextopage.md)                         | Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .<br/>                                                                       |
| [**\_INSERTPAGE PSM**](psm-insertpage.md)                           | Insère une nouvelle page dans une feuille de propriétés existante. La page peut être insérée à un index spécifié ou après une page spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .<br/>                |
| [**\_ISDIALOGMESSAGE PSM**](psm-isdialogmessage.md)                 | Transmet un message à une boîte de dialogue de feuille de propriétés et indique si la boîte de dialogue a traité le message. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .<br/>                              |
| [**\_PAGETOINDEX PSM**](psm-pagetoindex.md)                         | Prend le handle HPROPSHEETPAGE de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .<br/>                                                          |
| [**\_PRESSBUTTON PSM**](psm-pressbutton.md)                         | Simule la sélection d’un bouton de feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .<br/>                                                                                              |
| [**\_QUERYSIBLINGS PSM**](psm-querysiblings.md)                     | Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .<br/>                                                              |
| [**\_REBOOTSYSTEM PSM**](psm-rebootsystem.md)                       | Indique que le système doit être redémarré pour que les modifications prennent effet. Vous pouvez envoyer le [**message \_ REBOOTSYSTEM PSM**](psm-rebootsystem.md) de manière explicite ou à l’aide de la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .<br/>                        |
| [**\_RECALCPAGESIZES PSM**](psm-recalcpagesizes.md)                 | Recalcule la taille de page d’une feuille de propriétés standard ou d’Assistant après l’ajout ou la suppression de pages. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .<br/>                                     |
| [**\_REMOVEPAGE PSM**](psm-removepage.md)                           | Supprime une page d'une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .<br/>                                                                                                              |
| [**\_RESTARTWINDOWS PSM**](psm-restartwindows.md)                   | Indique que Windows doit être redémarré pour que les modifications prennent effet.<br/>                                                                                                                                                                                         |
| [**\_SETBUTTONTEXT PSM**](psm-setbuttontext.md)                     | Définit le texte d’un bouton dans un Assistant Aero. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .<br/>                                                                                                 |
| [**\_SETCURSEL PSM**](psm-setcursel.md)                             | Active la page spécifiée dans une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .<br/>                                                                                                    |
| [**\_SETCURSELID PSM**](psm-setcurselid.md)                         | Active la page donnée dans une feuille de propriétés en fonction de l’identificateur de ressource de la page. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .<br/>                                                   |
| [**\_SETFINISHTEXT PSM**](psm-setfinishtext.md)                     | Définit le texte du bouton **Terminer** dans un Assistant, affiche et active le bouton et masque les boutons **suivant** et **précédent** . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .<br/>               |
| [**\_SETHEADERBITMAP PSM**](psm-setheaderbitmap.md)                 | Ce message n’est pas implémenté.<br/>                                                                                                                                                                                                                                     |
| [**\_SETHEADERBITMAPRESOURCE PSM**](psm-setheaderbitmapresource.md) | Ce message n’est pas implémenté.<br/>                                                                                                                                                                                                                                     |
| [**\_SETHEADERSUBTITLE PSM**](psm-setheadersubtitle.md)             | Définit le texte du sous-titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .<br/>                                                                        |
| [**\_SETHEADERTITLE PSM**](psm-setheadertitle.md)                   | Définit le texte du titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .<br/>                                                                                 |
| [**\_SETNEXTTEXT PSM**](psm-setnexttext.md)                         | Définit le texte du bouton **suivant** dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .<br/>                                                                                                |
| [**\_SETTITLE PSM**](psm-settitle.md)                               | Définit le titre d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .<br/>                                                                                                                    |
| [**\_SETWIZBUTTONS PSM**](psm-setwizbuttons.md)                     | Active ou désactive les boutons **précédent**, **suivant** et **Terminer** dans un Assistant. Vous pouvez également utiliser la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour envoyer le message.<br/>                                                                          |
| [**\_SHOWWIZBUTTONS PSM**](psm-showwizbuttons.md)                   | Affiche ou masque les boutons dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .<br/>                                                                                                        |
| [**PSM \_ INchangé**](psm-unchanged.md)                             | Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ inchangée**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .<br/>                                                      |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                     | Contenu                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ appliquer](psn-apply.md)                               | Envoyé à chaque page de la feuille de propriétés pour indiquer que l’utilisateur a cliqué sur le bouton OK, fermer ou appliquer et souhaite que toutes les modifications soient prises en compte. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>      |
| [PSN \_ GETOBJECT](psn-getobject.md)                       | Envoyé par une feuille de propriétés pour demander un objet cible de dépôt lorsque le curseur passe sur l’un des boutons du contrôle onglet.<br/>                                                                                                                       |
| [aide de PSN \_](psn-help.md)                                 | Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton aide. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | Avertit une page qu’il va perdre l’activation soit parce qu’une autre page est activée, soit parce que l’utilisateur a cliqué sur le bouton **OK** . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | Indique que l’utilisateur a annulé la feuille de propriétés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | Envoyé par une feuille de propriétés pour permettre à une page de feuille de propriétés de spécifier quel contrôle de boîte de dialogue doit recevoir le focus initial. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>           |
| [\_réinitialisation PSN](psn-reset.md)                               | Avertit une page que la feuille de propriétés va être détruite. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                   |
| [PSN \_](psn-setactive.md)                       | Avertit une page qu’elle va être activée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                   |
| [PSN \_ TRANSLATEACCELERATOR](psn-translateaccelerator.md) | Avertit une feuille de propriétés qu’un message de clavier a été reçu. Elle offre la possibilité d’effectuer une traduction d’accélérateur de clavier privée. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **précédent** dans un Assistant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **Terminer** dans un Assistant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **suivant** dans un Assistant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                          |



 

### <a name="structures"></a>Structures



| Rubrique                                      | Contenu                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Définit le frame et les pages d’une feuille de propriétés.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Définit une page dans une feuille de propriétés.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Contient des informations sur les codes de notification de la feuille de propriétés.<br/> |



 

 

