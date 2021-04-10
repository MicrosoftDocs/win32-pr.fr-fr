---
title: Connexions de réseau privé virtuel
description: Le service d’accès à distance (RAS) prend en charge les connexions de réseau privé virtuel (VPN) en plus des connexions d’accès à distance conventionnelles qui utilisent protocole PPP (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f5fc0b80a6eb00e7587e941eea39c056a11d14
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031354"
---
# <a name="virtual-private-network-connections"></a>Connexions de réseau privé virtuel

Le service d’accès à distance (RAS) prend en charge les connexions de réseau privé virtuel (VPN) en plus des connexions d’accès à distance conventionnelles qui utilisent protocole PPP (PPP). Dans une connexion VPN, les paquets VPN sont encapsulés dans les paquets IP et envoyés sur un réseau IP comme Internet. Par conséquent, l’accès à un réseau IP est requis pour établir une connexion VPN. Si l’ordinateur client dispose d’une connexion Always on à un réseau IP, par exemple une connexion à un réseau local IP, le client peut établir la connexion VPN à l’aide d’un appel unique à la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

Si l’ordinateur client ne dispose pas d’une connexion Always on à un réseau IP, deux appels à [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sont requis pour établir la connexion VPN. Le premier appel établit une connexion d’accès à distance au réseau IP ; le deuxième appel établit la connexion VPN.

Le membre **szLocalPhoneNumber** de la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) pour la connexion VPN doit contenir le nom DNS ou l’adresse IP du serveur VPN de destination.

Chaque connexion nécessite une entrée [d’annuaire téléphonique](ras-phone-books.md) distincte. Le premier appel à [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) spécifie l’entrée de l’annuaire téléphonique pour le réseau IP. Le deuxième appel spécifie l’entrée de l’annuaire téléphonique pour le VPN.

La fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) prend un pointeur vers une structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) comme paramètre. Cette structure spécifie les informations d’authentification à utiliser pour le réseau spécifié par l’entrée de l’annuaire téléphonique. Les informations d’identification requises pour accéder au réseau IP sont généralement différentes de celles du VPN. Le premier appel à **rasdial** doit spécifier des informations d’identification pour le réseau IP. Le deuxième appel doit spécifier des informations d’identification pour le VPN.

Si la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) est réussie, elle retourne un handle pour la connexion. Utilisez ce handle dans un appel à [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) pour mettre fin à la connexion.

Dans le scénario précédent, les deux appels à [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) retournent des handles de connexion distincts pour le réseau IP et le VPN. L’appel de [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) avec le descripteur pour la connexion VPN met fin à la connexion VPN, mais laisse la connexion au réseau IP intacte.

 

 