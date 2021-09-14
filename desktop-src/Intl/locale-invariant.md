---
description: paramètres régionaux \_ INvariants
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240179"
---
# <a name="locale_invariant"></a>paramètres régionaux \_ INvariants

**Windows XP :** Paramètres régionaux utilisés pour les fonctions au niveau du système d’exploitation qui requièrent des résultats cohérents et indépendants des paramètres régionaux. Par exemple, les paramètres régionaux indifférent sont utilisés lorsqu’une application compare des chaînes de caractères à l’aide de la fonction [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et attend un résultat cohérent, quels que soient les paramètres régionaux de l’utilisateur. Les paramètres des paramètres régionaux invariants sont similaires à ceux de l’anglais (États-Unis), mais ne doivent pas être utilisés pour afficher des données mises en forme. En règle générale, une application n’utilise pas d' \_ invariant de paramètres régionaux, car elle s’attend à ce que les résultats d’une action dépendent des règles régissant chacun des paramètres régionaux individuels. La valeur de la \_ variable locale INVARIANT est 0x007F.

 

 
