---
description: Il existe sept pinceaux de stock logique prédéfinis gérés par l’interface GDI (Graphics Device Interface). Il y a également 21 pinceaux de stock logique prédéfinis gérés par l’interface de gestion de fenêtre (utilisateur).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pinceau boursier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120246"
---
# <a name="stock-brush"></a>Pinceau boursier

Il existe sept pinceaux de stock logique prédéfinis gérés par l’interface GDI (Graphics Device Interface). Il y a également 21 pinceaux de stock logique prédéfinis gérés par l’interface de gestion de fenêtre (utilisateur).

L’illustration suivante montre des rectangles peints à l’aide des sept pinceaux boursiers prédéfinis.

![Illustration montrant sept boîtes : un noir, trois nuances de gris et trois qui apparaissent vides](images/csbru-03.png)

Une application peut récupérer un handle identifiant l’un des sept pinceaux boursiers en appelant la fonction [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , en spécifiant le type de pinceau.

Les 21 actions boursières gérées par l’interface de gestion des fenêtres correspondent aux couleurs des éléments de la fenêtre, tels que les menus, les barres de défilement et les boutons. Une application peut obtenir un handle identifiant l’un de ces pinceaux en appelant la fonction [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) et en spécifiant une valeur de couleur système. Une application peut récupérer la couleur correspondant à un élément de fenêtre particulier en appelant la fonction [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) . Une application peut définir la couleur correspondant à un élément de fenêtre en appelant la fonction [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .

 

 
