---
description: Les fonctions GetUpdateRect et GetUpdateRgn récupèrent la région de mise à jour actuelle pour la fenêtre.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Récupération de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28bf72bfcfd28ec0fc9a90485a94e19d0514bb0206de660c11a56d12f33671e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698242"
---
# <a name="retrieving-the-update-region"></a>Récupération de la région de mise à jour

Les fonctions [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) et [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) récupèrent la région de mise à jour actuelle pour la fenêtre. GetUpdateRect récupère le plus petit rectangle (en coordonnées logiques) qui englobe la totalité de la région de mise à jour. GetUpdateRgn récupère la région de mise à jour elle-même. Ces fonctions peuvent être utilisées pour calculer la taille actuelle de la région de mise à jour afin de déterminer où exécuter une opération de dessin.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) récupère également les dimensions du plus petit rectangle qui englobe la région de mise à jour actuelle, en copiant les dimensions dans le membre **rcPaint** de la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Étant donné que **BeginPaint** valide la région de mise à jour, tout appel à [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) et [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immédiatement après un appel à **BeginPaint** retourne une région de mise à jour vide.

 

 



