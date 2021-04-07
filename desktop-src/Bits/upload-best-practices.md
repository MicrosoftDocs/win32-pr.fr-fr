---
title: Télécharger les meilleures pratiques
description: Highloads peut provoquer diverses conditions de délai d’attente du serveur, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028657"
---
# <a name="upload-best-practices"></a>Télécharger les meilleures pratiques

Highloads peut provoquer diverses conditions de délai d’attente du serveur, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative. En outre, un grand nombre de connexions en suspens consommeront plus de ressources serveur et compliqueront la situation. En plus de cela, si l’application principale n’est pas écrite pour gérer les conditions de charge élevée, elle peut se bloquer ou se comporter de façon inappropriée. L’application doit effectuer les étapes suivantes pour limiter la charge sur le serveur principal.

Si l’application serveur n’est pas écrite pour gérer des volumes élevés, des conditions d’expiration peuvent se produire, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative. En outre, un grand nombre de connexions en suspens consommeront plus de ressources serveur.

Lors du test de votre application serveur, testez avec la charge la plus élevée possible. Vous devez utiliser plusieurs ordinateurs clients, chacun avec plusieurs travaux de BITS de premier plan simultanés, et mesurer le débit maximal au niveau du serveur principal. Si vous ne pouvez pas mesurer le débit, vous devrez estimer le débit.

L’application serveur doit résider sur une URL différente de l’URL de téléchargement (voir la propriété IIS de BITS, **BITSServerNotificationURL**).

Il est conseillé de limiter la charge sur le serveur d’applications en fonction des valeurs de débit éprouvées. Vous devez utiliser les propriétés IIS, **MaxBandwidth** et **MaxConnections**, pour limiter la charge sur le serveur d’applications.

 

 




