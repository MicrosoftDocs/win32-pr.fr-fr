---
description: Cette section de référence décrit la configuration de Windows et des messages. En savoir plus sur les éléments d’affichage et les mesures système.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuration (Windows et messages)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406342"
---
# <a name="configuration-windows-and-messages"></a>Configuration (Windows et messages)

Les *éléments d’affichage* sont les parties d’une fenêtre et l’affichage qui s’affichent sur l’écran d’affichage du système. Les *métriques du système* sont les dimensions de différents éléments d’affichage. Les métriques système typiques incluent la largeur de la bordure de la fenêtre, la hauteur de l’icône, et ainsi de suite. Les métriques système décrivent également d’autres aspects du système, par exemple si une souris est installée, si des caractères codés sur deux octets sont pris en charge ou si une version de débogage du système d’exploitation est installée. La fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) récupère la métrique système spécifiée.

Les applications peuvent également récupérer et définir la couleur des éléments de fenêtre tels que les menus, les barres de défilement et les boutons à l’aide des fonctions [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) et [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivement.

La fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) récupère ou définit différents attributs système, tels que l’heure du double-clic, le délai d’attente de l’économiseur d’écran, la largeur de la bordure de la fenêtre et le modèle de bureau. Quand une application utilise **SystemParametersInfo** pour définir un paramètre, la modification a lieu immédiatement. Cette fonction permet également aux applications de mettre à jour le profil utilisateur, de sorte que les modifications apportées au système sont conservées lors du redémarrage du système.

 

 
