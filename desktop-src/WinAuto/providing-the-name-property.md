---
title: Fourniture de la propriété Name
description: Les développeurs de serveurs doivent se préoccuper de la création de contrôles prédéfinis et communs pour s’assurer que Microsoft Active Accessibility peut exposer la propriété Name du contrôle.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93205430f3063b993c49a7145658d7748aac0e697257789c31ac0653d6189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052547"
---
# <a name="providing-the-name-property"></a>Fourniture de la propriété Name

Les développeurs de serveurs doivent se préoccuper de la création de contrôles prédéfinis et communs pour s’assurer que Microsoft Active Accessibility peut exposer la [propriété Name](name-property.md) du contrôle. Selon le type de contrôle, le texte de la propriété Name provient de l’un des éléments suivants :

-   Texte de la fenêtre du contrôle (ou légende)
-   Texte statique qui étiquette le contrôle

Pour rechercher le texte de la fenêtre du contrôle, Microsoft Active Accessibility envoie le message [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) au contrôle. Ce texte correspond au paramètre text de l’instruction de définition de ressource du contrôle. Pour certains contrôles, tels que les boutons, il s’agit du même texte que celui qui est affiché avec le contrôle. Pour les autres contrôles, tels que les barres d’outils, ce texte n’est pas affiché. Par conséquent, les développeurs de serveurs doivent fournir un texte explicite dans l’instruction de définition de ressource du contrôle pour aider les utilisateurs des utilitaires clients à identifier le contrôle.

Pour Rechercher l’étiquette du contrôle, Microsoft Active Accessibility recherche un contrôle de texte statique en appelant [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) à l’aide de l' \_ indicateur GW HWNDPREV. La recherche est interrompue si un contrôle de texte statique est trouvé ou si un contrôle avec les styles de fenêtre WS TABSTOP a été rencontré \_ \| \_ . Cet ordre de recherche correspond à l’ordre de tabulation inverse sur une boîte de dialogue. Les développeurs de serveurs doivent observer l’ordre de tabulation lors de la création de contrôles afin qu’un contrôle de texte statique précède immédiatement le contrôle qu’il étiquette.

Pour plus d’informations sur les techniques utilisées par Microsoft Active Accessibility pour exposer la [propriété Name](name-property.md), consultez Référence des éléments de l' [interface utilisateur](user-interface-element-reference.md).

 

 