---
title: Initialisation du point d’accès du protocole EAP
description: Lors de l’initialisation, le point d’accès interroge le registre pour les protocoles d’authentification installés.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ff650df29a446527224d8160b4080a252d525d26d32efedae254755ac9514a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984429"
---
# <a name="access-point-initialization-of-eap"></a>Initialisation du point d’accès du protocole EAP

Lors de l’initialisation, le point d’accès interroge le registre pour les protocoles d’authentification installés. Le point d’accès appelle ensuite la fonction exportée [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) pour chaque protocole d’authentification. La fonction **RasEapGetInfo** reçoit un paramètre unique de type [**PPP \_ EAP \_ info**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). Le point d’accès utilise le membre **dwEapTypeId** de cette structure pour spécifier le protocole d’authentification. Notez qu’une seule DLL peut prendre en charge plusieurs protocoles. Si **RasEapGetInfo** retourne une valeur autre qu' **aucune \_ erreur**, le point d’accès suppose que le protocole d’authentification n’est pas disponible.

Au retour de [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) , la structure d' [**\_ \_ informations EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contient des pointeurs vers les fonctions [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))et [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) dans la dll EAP. Le service AP utilise ces fonctions pour interagir avec le protocole d’authentification. Le point d’accès appelle immédiatement **RasEapInitialize** pour chaque protocole d’authentification, pour l’initialiser. Lorsque le service s’arrête, il appelle à nouveau **RasEapInitialize** , cette fois avec le paramètre *FInitialize* défini sur **false** pour indiquer que le protocole d’authentification doit s’arrêter.

 

 