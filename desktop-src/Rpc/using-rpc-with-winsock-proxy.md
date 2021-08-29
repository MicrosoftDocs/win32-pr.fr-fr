---
title: Utilisation de RPC avec le proxy Winsock
description: Utilisation de RPC avec le proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc841cb1a3fdecf1f0493f27ef9224ec540dcebbbeaacdb7b287102a246c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010647"
---
# <a name="using-rpc-with-winsock-proxy"></a>Utilisation de RPC avec le proxy Winsock

la version de Microsoft Internet Access Server comprenait le Proxy Winsock, une version améliorée de Windows API sockets version 1,1. le Proxy Winsock permet à une application de sockets Windows, exécutée sur un client réseau privé, de se comporter comme si elle était connectée directement à une application de serveur Internet distant. Le serveur proxy Microsoft joue le rôle d’hôte pour cette connexion. Cela signifie que toutes les communications au niveau de l’application sont représentées par un seul ordinateur sécurisé : l’ordinateur de passerelle exécutant Microsoft Proxy Server.

Habituellement, pour les transferts de paquets de datagrammes, la DLL de transport RPC ignore les fonctions [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) et [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fournies dans Wsock32.dll, et communique directement avec le pilote de périphérique sous-jacent. Cela améliore la vitesse des transferts de paquets, mais rend les fonctionnalités du proxy Winsock indisponibles pour l’application.

Chaque fournisseur de protocole réseau doit avoir un GUID associé. La bibliothèque Runtime RPC compare les GUID UDP et IPX aux identificateurs Microsoft connus. S’ils ne correspondent pas, RPC utilise automatiquement Winsock.

Une autre fonctionnalité du proxy Winsock est sa capacité à émuler le protocole de transport TCP sur le transport Novell SPX lorsque TCP n’est pas installé sur l’ordinateur client SPX. Pour utiliser cette fonctionnalité avec les applications RPC, modifiez le registre système sur chaque ordinateur client pour ajouter cette entrée :

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Modifiez le registre sur chaque ordinateur serveur pour ajouter cette entrée :

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Pour plus d’informations sur les protocoles de transport RPC, consultez [spécification de séquences de protocole](specifying-protocol-sequences.md). Pour plus d’informations sur le proxy Winsock, consultez la documentation produit de Microsoft Internet Access Server (en anglais).

Windows 2000 n’implémente pas les entrées de registre **ClientProtocols** et **ServerProtocols** . Microsoft fournit tous les transports bien connus dans le cadre de la bibliothèque Runtime. Par conséquent, ces entrées ne sont pas nécessaires.

 

 