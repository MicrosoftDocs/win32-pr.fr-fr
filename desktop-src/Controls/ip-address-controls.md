---
title: À propos des contrôles d’adresse IP
description: Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce537b3b3a92846961e95321889d106a61a81e14bfa4cbc4edd93da5c8c033ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435592"
---
# <a name="about-ip-address-controls"></a>À propos des contrôles d’adresse IP

Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible. Ce contrôle permet également à l’application d’obtenir l’adresse sous forme numérique plutôt que sous forme de texte.

-   [À propos des contrôles d’adresse IP](#about-ip-address-controls)
-   [Création d’un contrôle d’adresse IP](#creating-an-ip-address-control)
-   [Une adresse IP contrôle-t-elle un contrôle d’édition ?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>À propos des contrôles d’adresse IP

Windows Internet Explorer version 4,0 introduit le contrôle d’adresse IP, un nouveau contrôle similaire à un contrôle d’édition qui permet à l’utilisateur d’entrer une adresse numérique au format IP (Internet Protocol). Ce format se compose de champs à 4 3 chiffres. Chaque champ est traité individuellement. les numéros de champ sont de base zéro et se déroulent de gauche à droite, comme illustré dans cette figure.

![Diagramme montrant des valeurs dans chacun des quatre champs d’un contrôle d’adresse IP](images/ipa-scrn.png)

Le contrôle permet d’entrer uniquement du texte numérique dans chacun des champs. Une fois trois chiffres entrés dans un champ donné, le focus clavier est automatiquement déplacé vers le champ suivant. Si le remplissage du champ entier n’est pas requis par l’application, l’utilisateur peut entrer moins de trois chiffres. Par exemple, si le champ ne doit contenir que le nombre vingt-un, tapez « 21 » et appuyez sur la touche pour que l’utilisateur passe au champ suivant.

La plage par défaut de chaque champ est comprise entre 0 et 255, mais l’application peut définir la plage sur n’importe quelle valeur comprise entre ces limites et le message [**IPM \_ SetRange**](ipm-setrange.md) .

> [!Note]  
> Le contrôle d’adresse IP est implémenté dans la version 4,71 et les versions ultérieures de Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Création d’un contrôle d’adresse IP

Avant de créer un contrôle d’adresse IP, appelez [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avec l’indicateur des **\_ \_ classes Internet ICC** défini dans le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

Utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle d’adresse IP. Le nom de classe du contrôle est [**WC \_ IPAddress**](common-control-window-classes.md), qui est défini dans commctrl. h. Il n’existe pas de styles spécifiques à un contrôle d’adresse IP. Toutefois, étant donné qu’il s’agit d’un contrôle enfant, utilisez le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) au minimum.

## <a name="is-an-ip-address-control-an-edit-control"></a>Une adresse IP contrôle-t-elle un contrôle d’édition ?

Un contrôle d’adresse IP n’est pas un contrôle d’édition et ne répond pas aux \_ messages em. Toutefois, il envoie à la fenêtre propriétaire les notifications de contrôle d’édition suivantes par le biais du message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . Notez que le contrôle d’adresse IP enverra également \_ des notifications IPN privées par le biais du message [**WM \_ Notify**](wm-notify.md) .



|     Notification                              |     Raison de la notification                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [en \_ SetFocus](en-setfocus.md)   | Envoyé lorsque le contrôle d’adresse IP obtient le focus clavier.                                                                                                                                              |
| [en \_ KILLFOCUS](en-killfocus.md) | Envoyé lorsque le contrôle d’adresse IP perd le focus clavier.                                                                                                                                              |
| [en \_ modification](en-change.md)       | Envoyé lorsqu’un champ du contrôle d’adresse IP change. À l’instar de la notification en [ \_ modification](en-change.md) d’un contrôle d’édition standard, cette notification est reçue après la mise à jour de l’écran. |



 

 

 