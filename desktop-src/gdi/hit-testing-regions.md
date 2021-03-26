---
description: Une application effectue un test de positionnement sur les régions pour déterminer les coordonnées de la position actuelle du curseur.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Régions de test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202035"
---
# <a name="hit-testing-regions"></a>Régions de test de positionnement

Une application effectue un test de positionnement sur les régions pour déterminer les coordonnées de la position actuelle du curseur. Il transmet ensuite ces coordonnées, ainsi qu’un handle identifiant la région à la fonction [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . Les coordonnées du curseur peuvent être récupérées en traitant les différents messages de la souris, tels que [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) et [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md). La valeur de retour pour PtInRegion indique si la position du curseur se trouve dans la région donnée.

 

 
