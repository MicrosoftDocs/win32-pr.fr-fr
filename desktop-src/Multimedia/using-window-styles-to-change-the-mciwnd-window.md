---
title: Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd
description: Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369215"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Utilisation de styles de fenêtre pour modifier la fenêtre MCIWnd

Comme pour n’importe quelle fenêtre, vous pouvez modifier l’apparence et le comportement d’une fenêtre MCIWnd en choisissant parmi les styles de fenêtre standard spécifiés avec la fonction [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . En outre, vous pouvez choisir parmi plusieurs autres styles de fenêtre spécifiques aux fenêtres MCIWnd. Avec ces styles, votre application peut modifier ces fenêtres MCIWnd des manières suivantes :

-   Modifiez la taille de la fenêtre.
-   Masquer ou afficher des contrôles.
-   Émettre des messages de notification.
-   Affichez les informations dans la barre de titre.

Vous pouvez définir des styles de fenêtre en les spécifiant dans la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , ou vous pouvez utiliser la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) pour modifier le style d’une fenêtre MCIWnd existante. Vous pouvez également interroger une fenêtre MCIWnd pour ses styles actuels à l’aide de la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .

Pour obtenir la liste des styles de fenêtre spécifiques à MCIWnd, consultez [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 