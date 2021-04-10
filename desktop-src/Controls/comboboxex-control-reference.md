---
title: Contrôle ComboBoxEx
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a926ccf2f9f5b5bb68e040731d6b9d8e37ee8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953615"
---
# <a name="comboboxex-control"></a>Contrôle ComboBoxEx

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles ComboBoxEx.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                | Contenu                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [À propos des contrôles ComboBoxEx](comboboxex-controls.md) | Les contrôles ComboBoxEx sont des contrôles de zone de liste déroulante qui fournissent une prise en charge native des images d’élément.<br/> |
| [Utilisation des contrôles ComboBoxEx](using-comboboxex.md)    | Cette section contient des exemples de code et des informations sur l’utilisation des contrôles ComboBoxEx.<br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                                   | Contenu                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Supprime un élément d’un contrôle ComboBoxEx. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Obtient le handle du contrôle de zone de liste déroulante enfant. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx. Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le style de [**\_ liste déroulante CBS**](combo-box-styles.md) . <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | Obtient les styles étendus en cours d’utilisation pour un contrôle ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | Obtient le handle d’une liste d’images assignée à un contrôle ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | Obtient des informations sur les éléments d’un élément ComboBoxEx donné.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Obtient l’indicateur de format de caractère UNICODE pour le contrôle. <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Détermine si l’utilisateur a modifié le texte d’un contrôle d’édition ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Insère un nouvel élément dans un contrôle ComboBoxEx. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Ce message n’est pas implémenté. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Ce message n’est pas implémenté. <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | Définit des styles étendus dans un contrôle ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | Définit une liste d’images pour un contrôle ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Définit les attributs d’un élément dans un contrôle ComboBoxEx. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Définit l’indicateur de format de caractère UNICODE pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Définit le style visuel d’un contrôle ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                      | Contenu                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Envoyé lorsque l’utilisateur active la liste déroulante ou clique dans la zone d’édition du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Envoyé lorsqu’un élément a été supprimé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Envoyé lorsque l’utilisateur a terminé une opération dans la zone d’édition ou a sélectionné un élément dans la liste déroulante du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | Envoyé pour récupérer des informations d’affichage sur un élément de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Envoyé lorsqu’un nouvel élément a été inséré dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Avertit la fenêtre parente d’un contrôle ComboBoxEx que le contrôle définit le curseur en réponse à un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Structures



| Rubrique                                    | Contenu                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contient des informations sur un élément dans un contrôle ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contient des informations utilisées avec le code de notification [CBEN \_ DRAGBEGIN](cben-dragbegin.md) . <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contient des informations sur la conclusion d’une opération de modification dans un contrôle ComboBoxEx. Cette structure est utilisée avec le code de notification [CBEN \_ ENDEDIT](cben-endedit.md) . <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contient des informations spécifiques aux éléments ComboBoxEx à utiliser avec les codes de notification. <br/>                                                                                               |



 

### <a name="constants"></a>Constantes



| Rubrique                                                                        | Contenu                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Styles étendus de contrôle ComboBoxEx](comboboxex-control-extended-styles.md) | Prendre en charge les styles étendus répertoriés dans cette section, ainsi que la plupart des styles de contrôle de zone de liste modifiable standard.<br/> |



 

 

