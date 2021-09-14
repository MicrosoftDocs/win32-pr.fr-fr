---
title: Paramètre de contraste élevé
description: Le paramètre contraste élevé indique si l’utilisateur souhaite un contraste élevé entre les couleurs utilisées pour les visuels de premier plan et d’arrière-plan.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095545"
---
# <a name="high-contrast-parameter"></a>Paramètre de contraste élevé

Le paramètre contraste élevé indique si l’utilisateur souhaite un contraste élevé entre les couleurs utilisées pour les visuels de premier plan et d’arrière-plan.

L’utilisateur contrôle la définition du paramètre de contraste élevé à l’aide de la facilité d’accès dans le panneau de configuration, ou d’une autre application pour la personnalisation de l’environnement. Les applications utilisent les indicateurs **SPI \_ GETHIGHCONTRAST** et **SPI \_ SETHIGHCONTRAST** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de contraste élevé.

Pendant l’initialisation et lors du traitement des messages [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) , les applications doivent déterminer l’état du paramètre de contraste élevé. Pour effectuer cette détermination, les applications doivent appeler [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec l’indicateur **SPI \_ GETHIGHCONTRAST** pour obtenir une structure [**HIGHCONTRAST**](/windows/win32/api/winuser/ns-winuser-highcontrasta) . Si le jeu de bits **HCF \_ HIGHCONTRASTON** est défini pour le membre **DwFlags** de la structure **HIGHCONTRAST** , la fonctionnalité de contraste élevé est activée et les applications doivent effectuer les opérations suivantes :

-   Mappez toutes les couleurs à une seule paire de couleurs de premier plan et d’arrière-plan. Utilisez la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) pour déterminer les couleurs de premier plan et d’arrière-plan appropriées, à l’aide d’une combinaison de **Color \_ WINDOWTEXT** et Color **\_ Window** ou d’une combinaison de **Color \_ BTNTEXT** et **Color \_ BTNFACE**. La fonction **GetSysColor** retourne les couleurs sélectionnées par l’utilisateur via le panneau de configuration.
-   Omettez les images bitmap qui seraient généralement affichées derrière le texte. Ces images sont visuellement gênantes pour un utilisateur qui a besoin d’un contraste élevé.
-   Les images qui seraient généralement dessinées dans plusieurs couleurs doivent être dessinées à l’aide des couleurs de premier plan et d’arrière-plan sélectionnées pour le texte.

En outre, les applications utilisent les indicateurs **SPI \_ GETDISABLEOVERLAPPEDCONTENT** et **SPI \_ SETDISABLEOVERLAPPEDCONTENT** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de contenu Overlapped. Les fonctionnalités d’affichage telles que les images d’arrière-plan, les arrière-plans texturés, les repères d’eau sur les documents, la fusion alpha et la transparence peuvent réduire le contraste entre le premier plan et l’arrière-plan, ce qui rend plus difficile les utilisateurs avec une acuité visuelle réduite pour voir les objets à l’écran. Cet indicateur permet aux applications de déterminer si un contenu avec chevauchement a été désactivé

 

 