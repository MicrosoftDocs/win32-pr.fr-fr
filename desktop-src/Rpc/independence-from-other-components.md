---
title: Indépendance par rapport aux autres composants
description: Les données d’erreur étendues sont utiles même lorsque le serveur ou l’application par le biais duquel la chaîne transmise ne reconnaît pas les données d’erreur étendues ou ne les tire pas parti. Les approches recommandées pour ces situations sont fournies à la fin de cette section.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Indépendance par rapport aux autres composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940253"
---
# <a name="independence-from-other-components"></a>Indépendance par rapport aux autres composants

Les données d’erreur étendues sont utiles même lorsque le serveur ou l’application par le biais duquel la chaîne transmise ne reconnaît pas les données d’erreur étendues ou ne les tire pas parti. Les approches recommandées pour ces situations sont fournies à la fin de cette section.

Les données d’erreur étendues sont particulièrement utiles lorsque les applications ou les serveurs qui utilisent RPC tirent parti des informations d’erreur étendues. Lorsque vous examinez un \_ code d’erreur RPC S \_ \* et que les serveurs ou applications impliqués ne mettent pas à disposition des données d’erreur étendues, envisagez les approches suivantes :

-   Jetez un espion.

    Reproduisez le scénario tout en effectuant la détection. La détection du câble contiendra les données d’erreur étendues.

-   Examinez-le à partir du débogueur.

    Si la détection du problème ne fonctionne pas, car l’appel est local ou parce que l’erreur provient localement, attachez un débogueur au processus qui retourne l’erreur et placez un point d’arrêt immédiatement après l’appel RPC qui a généré l’erreur. Souvent, RPC indique des erreurs en levant des exceptions. par conséquent, si vous recherchez l’erreur 1825 (erreur s de l’appel RPC \_ s \_ \_ \_ ), activez l’exception 1825 et, lorsque le débogueur s’arrête sur cette exception, examinez les informations d’erreur étendues pour le thread.

 

 




