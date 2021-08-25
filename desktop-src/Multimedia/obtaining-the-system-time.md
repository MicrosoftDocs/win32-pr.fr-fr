---
title: Obtention de l’heure système
description: Obtention de l’heure système
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- minuteries multimédias, heure système
- minuteries, heure système
- heure système
- timeGetTime fonction)
- timeGetSystemTime fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806469"
---
# <a name="obtaining-the-system-time"></a>Obtention de l’heure système

En règle générale, avant qu’une application commence à utiliser les services de minuteur multimédia, elle récupère l' *heure système* actuelle. l’heure système correspond à la durée, en millisecondes, depuis le démarrage du système d’exploitation Microsoft Windows. Vous pouvez utiliser la fonction [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) ou [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) pour récupérer l’heure système. Ces deux fonctions sont très similaires : **timeGetTime** retourne l’heure système et **timeGetSystemTime** remplit une structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) avec l’heure système.

 

 