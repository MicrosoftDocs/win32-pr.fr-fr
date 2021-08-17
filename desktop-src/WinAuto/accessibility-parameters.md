---
title: Paramètres d’accessibilité
description: Le système gère un ensemble de paramètres d’accessibilité qui indiquent si l’utilisateur a des besoins ou des préférences spécifiques qui requièrent que les applications modifient leur comportement par défaut.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a289162366f5d69c501ffbea55108167324c11a1c865184105afd587f36bcfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327787"
---
# <a name="accessibility-parameters"></a>Paramètres d’accessibilité

Le système gère un ensemble de paramètres d’accessibilité qui indiquent si l’utilisateur a des besoins ou des préférences spécifiques qui requièrent que les applications modifient leur comportement par défaut. L’utilisateur contrôle l’état de ces paramètres, généralement à l’aide de la facilité d’accès du panneau de configuration. Les applications du panneau de configuration ou d’autres programmes qui permettent à l’utilisateur de personnaliser l’environnement peuvent utiliser la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour définir les paramètres d’accessibilité.

Si un utilisateur modifie ces paramètres, le panneau de configuration envoie le message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) . Les applications doivent répondre à ce message et utiliser [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour déterminer l’état des paramètres d’accessibilité. Lorsqu’un paramètre d’accessibilité est activé, l’application doit modifier son interface utilisateur, si nécessaire, pour s’adapter aux préférences de l’utilisateur.

Windows prend en charge les paramètres d’accessibilité suivants.



| Paramètre                                                                    | Description                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contraste élevé](high-contrast-parameter.md)                                 | Indique que les applications doivent fournir un contraste élevé entre les visuels de premier plan et d’arrière-plan.                                                                            |
| [Préférences du clavier](keyboard-preference-parameter.md)                     | Indique que les applications doivent afficher les interfaces de clavier qui seraient normalement masquées.                                                                                 |
| [Lecteur d’écran](screen-reader-parameter.md)                                 | Indique que les applications doivent fournir des informations textuelles dans les situations où elles présenteront autrement les informations sous forme graphique.                                     |
| [Afficher les sons (et l’indicateur de description audio)](showsounds-parameter.md) | Indique que les applications doivent également fournir une alerte ou un signal visuel lorsqu’il utilise le son pour transmettre des informations importantes ou fournir une description audio pour les éléments visuels. |
| [Animation de la zone cliente](client-area-animation.md)                           | Indique que les applications doivent respecter les préférences de l’utilisateur pour afficher l’animation dans la zone cliente.                                                                       |
| [Durée du message](message-duration.md)                                     | Indique que les applications qui fournissent des notifications contextuelles doivent surveiller les indicateurs sur la durée du message et ajuster leur durée de notification.                                  |



 

Les paramètres système suivants sont utiles pour les applications d’accessibilité. Pour plus d’informations, consultez fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .



| Groupe de paramètres      | Paramètre                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Paramètres du Bureau   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Paramètres d'entrée     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, SPI GETMOUSEHOVERTIME, SPI GETMOUSEHOVERWIDTH, SPI GETMOUSESPEED, SPI \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ GETMOUSETRAILS, \_ SPI GETSNAPTODEFBUTTON, SPI GETWHEELSCROLLLINES, SPI SETDOUBLECLICKTIME, SPI SETDOUBLECLKHEIGHT, SPI SETDOUBLECLKWIDTH, SPI SETKEYBOARDCUES, SPI SETKEYBOARDDELAY, SPI SETKEYBOARDPREF, SPI SETKEYBOARDSPEED, SPI SETMOUSE, SPI SETMOUSEHOVERHEIGHT, SPI SETMOUSEHOVERTIME, SPI SETMOUSEHOVERWIDTH, SPI SETMOUSESPEED, SPI SETMOUSETRAILS |
| Paramètres d’effet de l’interface utilisateur | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Paramètres de fenêtre    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos des fonctionnalités d’accessibilité Windows](about-windows-accessibility-features.md)
</dt> </dl>

 

 