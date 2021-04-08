---
title: Paramètres de Registre du port du pare-feu
description: Paramètres de Registre du port du pare-feu
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, paramètres de Registre du port de pare-feu
- Lecteur Windows Media, paramètres de Registre du port
- Lecteur Windows Media, registre
- Registre, paramètres de port de pare-feu
- Registre, paramètres de port
- Registre, paramètres pour le lecteur Windows Media
- paramètres de Registre du port du pare-feu
- paramètres du registre de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839449"
---
# <a name="firewall-port-registry-settings"></a>Paramètres de Registre du port du pare-feu

Le lecteur Windows Media place des entrées dans le registre afin que les pare-feu puissent déterminer s’il faut ouvrir ou fermer les ports utilisés par le partage de bibliothèque multimédia.

**Entrée de Registre AcceptedEULA**

Le lecteur Windows Media utilise l’entrée de Registre suivante pour indiquer si l’utilisateur a accepté le contrat de licence utilisateur final (CLUF).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



La valeur 1 indique que l’utilisateur a accepté le contrat de licence. La valeur 0 indique que l’utilisateur n’a pas accepté le contrat de licence.

**Entrée de Registre WMPNSSFirewallPortsOpen**

Le lecteur Windows Media utilise l’entrée de Registre suivante pour indiquer si l’utilisateur a choisi de partager sa bibliothèque multimédia avec d’autres ordinateurs sur un réseau privé.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



La valeur 1 indique que l’utilisateur a choisi de partager la bibliothèque. La valeur 0 indique que l’utilisateur a choisi de ne pas partager la bibliothèque.

**Ports associés au partage de bibliothèque multimédia**

Sur Windows Vista, si l’entrée de Registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.



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



 

Sur Windows Vista, si l’entrée de Registre **AcceptedEULA** a la valeur 1, les ports suivants doivent être ouverts.



| Port          | Protocol       | Process                         | Sens            |
|---------------|----------------|---------------------------------|----------------------|
| Tous les ports UDP | RTP UDP, MSB   | wmplayer.exe, n’importe quel sous-réseau        | Vers l’intérieur de la ville              |
| 1900          | SSDP UDP       | SSDPsrv/UPnPHost dans svchost.exe | entrant et sortant |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | Vers l’intérieur de la ville              |



 

Sur Microsoft Windows XP, si l’entrée de Registre **WMPNSSFirewallPortsOpen** a la valeur 1, les ports suivants doivent être ouverts.



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

 

 




