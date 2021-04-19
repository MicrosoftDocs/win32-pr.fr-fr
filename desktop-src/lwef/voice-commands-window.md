---
title: Fenêtre commandes vocales
description: Fenêtre commandes vocales
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511279"
---
# <a name="voice-commands-window"></a>Fenêtre commandes vocales

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La fenêtre commandes vocales affiche les commandes vocales actives actuellement disponibles pour le caractère. La fenêtre s’affiche lorsque la commande ouvrir la fenêtre commandes est sélectionnée ou que la propriété [**visible**](visible-property.md) de l’objet [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) est définie sur **true**. Si le moteur de reconnaissance vocale n’a pas encore été chargé, l’interrogation ou la définition de cette propriété entraîne l’échec de l’initialisation du moteur par Microsoft Agent. Si l’utilisateur désactive la reconnaissance vocale, la fenêtre peut toujours s’afficher ; Toutefois, il inclura un message texte qui informe l’utilisateur que la reconnaissance vocale est actuellement désactivée.

Les commandes du client d’entrée-actif s’affichent dans la fenêtre commandes vocales en fonction des paramètres de la [**légende**](caption-property.md) [**vocale**](voice-property.md)et de la propriété **vocale** répertoriés sous le [**VoiceCaption**](voicecaption-property.md) de leur collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

**Figure 1. Fenêtre commandes vocales**

La fenêtre commandes vocales s’affiche lorsque la commande ouvrir la fenêtre commandes est sélectionnée. Les commandes du client d’entrée-actif s’affichent dans la fenêtre commandes vocales en fonction des paramètres de [**légende**](caption-property.md) [**vocal**](voice-property.md)et de propriété **vocale** répertoriés sous **voix** de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

La fenêtre commandes vocales répertorie également le [**VoiceCaption**](voicecaption-property.md) de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) pour les autres clients du caractère, et les commandes vocales suivantes générées par le serveur pour l’interaction générale sous l’entrée commandes globales :



| Légende vocale                       | Grammaire vocale                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ouvrir la \| fenêtre fermer les commandes vocales | (ouvrir \| afficher) \[ \] fenêtre commandes \[ \] \| que puis-je prononcer \[ maintenant\] <br/> bascule avec : <br/> fermer \[ la \] \[ fenêtre commandes\] <br/> |
| Masquer                                | cuir \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Commandes globales                     | \[afficher les \] \[ \] commandes globales                                                                                                                          |



 

\* Un caractère est répertorié ici uniquement s’il est actuellement visible.

\*\* Tous les caractères chargés sont répertoriés.

En parlant, la commande vocale pour la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) d’un autre client bascule vers ce client et la fenêtre commandes vocales affiche les commandes de ce client. Aucune autre entrée n’est développée. De même, si l’utilisateur change de caractères, la fenêtre commandes vocales change pour afficher les commandes de son client d’entrée-actif. Si le client est déjà en entrée-actif, l’une de ses commandes vocales n’a aucun effet. (Toutefois, si l’utilisateur réduit la sous-arborescence du client actif à l’aide de la souris, le fait de parler du nom du client réaffiche la sous-arborescence du client).

Si un client possède des commandes vocales, mais pas de paramètre [**vocal**](voice-property.md) pour son objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (ou aucune [**légende**](caption-property.md) **vocale**), l’arborescence affiche « (commande non définie) » comme entrée parente, mais uniquement quand ce client est actif en entrée et que le client a des commandes dans sa collection qui ont des paramètres de **légende** et de **voix** .

Le serveur affiche automatiquement les commandes du client courant d’entrée-actif et, si nécessaire, fait défiler la fenêtre pour afficher le nombre de commandes du client le plus possible, en fonction de la taille de la fenêtre. Si le caractère n’a pas d’entrées client, l’entrée commandes globales est développée.

Si l’utilisateur parle de « commandes globales », la fenêtre commandes vocales affiche toujours les entrées de sous-arborescence associées. S’ils sont déjà affichés, la commande n’a aucun effet.

Bien que vous puissiez également afficher ou masquer la fenêtre commandes vocales à partir du code de votre application à l’aide de la propriété [**visible**](visible-property.md) , vous ne pouvez pas modifier la taille ou l’emplacement de la fenêtre de commandes vocales. Le serveur gère les propriétés de la fenêtre commandes vocales en fonction de l’interaction de l’utilisateur avec la fenêtre. Son emplacement initial est immédiatement adjacent à l’icône de la barre des tâches du caractère.

La fenêtre commandes vocales est incluse dans l’ordre des fenêtres ALT + TAB. Cela permet à un utilisateur de basculer vers la fenêtre pour faire défiler, redimensionner ou repositionner la fenêtre à l’aide du clavier.

-   [Info-bulle d’écoute](the-listening-tip.md)
-   [La fenêtre Options de caractères avancés](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

