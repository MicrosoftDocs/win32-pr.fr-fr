---
title: Déconnexion en cours
description: Lorsqu’une application cliente RAS démarre une opération de connexion, l’appel de RasDial reçoit un handle de connexion HRASCONN pour identifier la connexion.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101859"
---
# <a name="disconnecting"></a>Déconnexion en cours

Lorsqu’une application cliente RAS démarre une opération de connexion, l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) reçoit un handle de connexion **HRASCONN** pour identifier la connexion. Si le handle retourné n’est pas **null**, le client doit finalement appeler la fonction [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) pour mettre fin à la connexion. Si une erreur se produit pendant l’opération de connexion, le client doit appeler **RasHangUp** même si la connexion n’a jamais été établie.

L’application qui appelle [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) ne doit pas se fermer immédiatement, car le gestionnaire de connexions d’accès à distance a besoin de temps pour terminer correctement la connexion. Au lieu de cela, l’application doit attendre que la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) retourne un \_ handle non valide d’erreur \_ , indiquant que la connexion a été supprimée.

Une application cliente RAS peut avoir besoin de mettre fin à une connexion même si elle n’a pas le descripteur renvoyé par [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Par exemple, l’application qui a appelé **rasdial** peut avoir été quittée après l’établissement de la connexion. Dans ce cas, l’application de déconnexion peut utiliser la fonction [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) pour récupérer toutes les connexions en cours. Pour chaque connexion, **RasEnumConnections** retourne une structure [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) qui contient le descripteur de connexion **HRASCONN** et le nom de l’entrée de l’annuaire téléphonique ou le numéro de téléphone spécifié lors du démarrage de l’opération de connexion. Ces informations peuvent être utilisées pour afficher une liste des connexions à partir desquelles l’utilisateur peut sélectionner la connexion à la fin.

 

 