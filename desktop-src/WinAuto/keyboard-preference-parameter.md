---
title: Paramètre de préférence du clavier
description: Le paramètre de préférence clavier indique que l’utilisateur s’appuie sur le clavier au lieu de la souris, de sorte que les applications doivent afficher les interfaces de clavier qui seraient autrement masquées.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010698"
---
# <a name="keyboard-preference-parameter"></a>Paramètre de préférence du clavier

Le paramètre de préférence clavier indique que l’utilisateur s’appuie sur le clavier au lieu de la souris, de sorte que les applications doivent afficher les interfaces de clavier qui seraient autrement masquées.

L’utilisateur contrôle la définition du paramètre de préférence clavier à l’aide de l’option Options d’ergonomie du panneau de configuration, ou d’une autre application pour la personnalisation de l’environnement. Les applications utilisent les indicateurs **SPI \_ GETKEYBOARDPREF** et **SPI \_ SETKEYBOARDPREF** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de préférence de clavier.

en outre, sur Windows 2000, les utilisateurs peuvent définir un paramètre qui indique si les touches d’accès de menu sont toujours soulignées. Les applications utilisent les indicateurs **SPI \_ GETMENUUNDERLINES** et **SPI \_ SETMENUUNDERLINES** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de soulignement de menu.

Quand une application reçoit un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) pour le paramètre de la préférence du clavier ou du menu de soulignement, il est recommandé que l’application appelle [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour mettre à jour les informations pour les deux paramètres.

Notez que **SPI \_ GETMENUUNDERLINES** est identique à **SPI \_ GETKEYBOARDCUES**, et que **SPI \_ SETMENUUNDERLINES** est identique à **SPI \_ SETKEYBOARDCUES**.

 

 