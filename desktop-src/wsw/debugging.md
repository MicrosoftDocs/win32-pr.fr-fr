---
title: débogage (Services Web Windows)
description: Un ensemble de fonctions est uniquement disponible dans la version DEBUG et est conçu pour le test et le débogage.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Débogage de services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838679"
---
# <a name="debugging-windows-web-services"></a>débogage (Services Web Windows)

Un ensemble de fonctions est uniquement disponible dans la version DEBUG et est conçu pour le test et le débogage.


Un certain nombre de fonctions et de variables d’environnement sont disponibles uniquement en mode débogage. Ils peuvent être utilisés pour faciliter le test et le débogage.

-   La définition de WsTimeout = 0 entraîne l’infiniisation de tous les délais d’attente. Cela est utile lorsque vous exécutez pas à pas le débogueur pendant des opérations sensibles au temps.
-   La définition de WsFailCount a le même effet que l’appel de WsSetAutoFail.
-   WsFlags vous permet de définir différents indicateurs qui modifient le comportement d’exécution. La syntaxe est WsFlags = a, b, c. Les indicateurs pris en charge sont ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest et ModifySignatureValue.

Les fonctions suivantes sont utilisées avec le débogage :

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




