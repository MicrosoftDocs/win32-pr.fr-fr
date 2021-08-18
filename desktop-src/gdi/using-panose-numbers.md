---
description: Les fichiers de polices TrueType incluent des nombres Panose, que les applications peuvent utiliser pour choisir une police qui correspond précisément à leurs spécifications.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Utilisation de nombres Panose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037457"
---
# <a name="using-panose-numbers"></a>Utilisation de nombres Panose

Les fichiers de polices TrueType incluent des nombres Panose, que les applications peuvent utiliser pour choisir une police qui correspond précisément à leurs spécifications. Le système PANOSE classe les visages par 10 attributs différents. Pour plus d’informations sur ces attributs, consultez [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Une structure **Panose** fait partie de la structure [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (dont les valeurs sont remplies en appelant la fonction [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).

Les attributs Panose sont évalués individuellement sur une échelle. Les valeurs résultantes sont concaténées pour produire un nombre. Étant donné ce nombre pour une police et une mesure mathématique pour mesurer les distances dans l’espace Panose, une application peut déterminer les voisins les plus proches.

 

 



