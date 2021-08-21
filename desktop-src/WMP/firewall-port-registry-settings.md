---
title: Paramètres du registre du Port du pare-feu
description: Paramètres du registre du Port du pare-feu
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Lecteur Windows Media, paramètres de registre du port de pare-feu
- Lecteur Windows Media, paramètres du registre de port
- Lecteur Windows Media, registre
- Registre, paramètres de port de pare-feu
- Registre, paramètres de port
- registre, paramètres pour Lecteur Windows Media
- paramètres de Registre du port du pare-feu
- paramètres du registre de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140f55a4008a03c2b3bc4184e2eca92129a5e30dc69f0871da856b4555daec73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576766"
---
# <a name="firewall-port-registry-settings"></a>Paramètres du registre du Port du pare-feu

Lecteur Windows Media place des entrées dans le registre afin que les pare-feu puissent déterminer s’il faut ouvrir ou fermer les ports utilisés par le partage de bibliothèque multimédia.

**Entrée de Registre AcceptedEULA**

Lecteur Windows Media utilise l’entrée de registre suivante pour indiquer si l’utilisateur a accepté le contrat de licence utilisateur final (cluf).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



La valeur 1 indique que l’utilisateur a accepté le contrat de licence. La valeur 0 indique que l’utilisateur n’a pas accepté le contrat de licence.

**Entrée de Registre WMPNSSFirewallPortsOpen**

Lecteur Windows Media utilise l’entrée de registre suivante pour indiquer si l’utilisateur a choisi de partager sa bibliothèque multimédia avec d’autres ordinateurs sur un réseau privé.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



La valeur 1 indique que l’utilisateur a choisi de partager la bibliothèque. La valeur 0 indique que l’utilisateur a choisi de ne pas partager la bibliothèque.

**Ports associés au partage de bibliothèque multimédia**

sur Windows Vista, si l’entrée de registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.



| Port          | Protocol                  | Process                         | Sens            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | RTSP TCP                  | wmpnetwk.exe                    | entrant et sortant |
| 8554-8558   | RTSP TCP                  | wmpnetwk.exe                    | entrant et sortant |
| 5004, 5005    | PROTOCOLE RTCP/RTP UDP              | wmpnetwk.exe                    | entrant et sortant |
| 50004-50013 | PROTOCOLE RTCP/RTP UDP              | wmpnetwk.exe                    | entrant et sortant |
| 1900          | SSDP UDP                  | SSDPsrv dans svchost.exe          | entrant et sortant |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost dans svchost.exe | Vers l’intérieur de la ville              |
| 10280-10284 | Enregistrement UDP WMDRM-ND | wmpnetwk.exe                    | entrant et sortant |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | Vers l’intérieur de la ville              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | entrant et sortant |



 

sur Windows Vista, si l’entrée de registre **AcceptedEULA** a la valeur 1, les ports suivants doivent être ouverts.



| Port          | Protocol       | Process                         | Sens            |
|---------------|----------------|---------------------------------|----------------------|
| Tous les ports UDP | RTP UDP, MSB   | wmplayer.exe, n’importe quel sous-réseau        | Vers l’intérieur de la ville              |
| 1900          | SSDP UDP       | SSDPsrv/UPnPHost dans svchost.exe | entrant et sortant |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | Vers l’intérieur de la ville              |



 

sur Microsoft Windows XP, si l’entrée de registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.



| Port          | Protocol                  | Process                         | Sens            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | SSDP UDP                  | SSDPsrv dans svchost.exe          | entrant et sortant |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost dans svchost.exe | Vers l’intérieur de la ville              |
| 10280-10284 | Enregistrement UDP WMDRM-ND | wmpnetwk.exe                    | entrant et sortant |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | Vers l’intérieur de la ville              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




