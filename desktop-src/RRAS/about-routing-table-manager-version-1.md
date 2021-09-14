---
title: À propos du gestionnaire de tables de routage version 1
description: Le gestionnaire de tables de routage est un référentiel central d’informations de routage pour tous les protocoles de routage qui fonctionnent sous le service Routage et accès distant (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Routage et accès à distance service RRAS, gestionnaire de tables de routage version 1
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 1, décrit
- Gestionnaire de routage de la version 1 RRAS
- Gestionnaire de table de routage version 1 RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009170"
---
# <a name="about-routing-table-manager-version-1"></a>À propos du gestionnaire de tables de routage version 1

**Windows Server 2003 :** cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les nouvelles applications doivent utiliser l’API du gestionnaire de table de routage version 2.

Le gestionnaire de tables de routage est un référentiel central d’informations de routage pour tous les protocoles de routage qui fonctionnent sous le service Routage et accès distant (RRAS). Le gestionnaire de tables de routage fournit des informations de routage à tous les composants concernés, tels que les protocoles de routage, les agents de gestion et les agents de surveillance. Le gestionnaire de tables de routage détermine également le meilleur itinéraire vers chaque réseau de destination connu des protocoles de routage. Il détermine cet itinéraire en fonction des priorités de protocole de routage et des métriques associées aux itinéraires. Notez que l’administrateur peut configurer des priorités de protocole de routage. Le gestionnaire de tables de routage transmet ensuite les informations les plus adaptées aux redirecteurs et les achemine vers les protocoles de routage.

Chaque protocole de routage appelle [**RtmRegisterClient**](rtmregisterclient.md) pour s’inscrire auprès du gestionnaire de tables de routage. **RtmRegisterClient** retourne un handle qui est utilisé par le protocole de routage pour ajouter ou supprimer des entrées d’itinéraire. **RtmRegisterClient** permet également au protocole de routage d’inscrire un objet d’événement auprès du gestionnaire de tables de routage. Le gestionnaire de table de routage signale cet objet d’événement pour notifier le protocole de routage des modifications apportées aux meilleures informations de routage. Tous les autres composants peuvent obtenir des informations stockées dans le gestionnaire de tables de routage par le biais de l’énumération d’itinéraire.

 

 




