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
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525088"
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

 

 




