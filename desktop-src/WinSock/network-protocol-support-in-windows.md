---
description: La suite de protocoles Internet est le protocole réseau dominant utilisé dans les réseaux d’entreprise et sur Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Prise en charge du protocole réseau Winsock dans Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484928"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Prise en charge du protocole réseau Winsock dans Windows

La suite de protocoles Internet est le protocole réseau dominant utilisé dans les réseaux d’entreprise et sur Internet. La suite de protocoles Internet représente une vaste collection de protocoles réseau en couches. La suite de protocoles Internet est souvent appelée TCP/IP, basée sur deux des protocoles les plus importants inclus dans la suite : le protocole IP (Internet Protocol) et le protocole TCP (Transmission Control Protocol).

IPv6 et IPv4 représentent les deux versions disponibles du protocole Internet. TCP est l’un des nombreux services réseau importants souvent appelés protocoles IP qui fonctionnent sur des réseaux IPv6 et IPv4. Le protocole UDP (User Datagram Protocol) et le protocole ICMP (Internet Control Message Protocol) sont d’autres protocoles IP importants utilisés sur des réseaux IPv6 et IPv4. Il existe un certain nombre d’autres protocoles IP qui peuvent être utilisés sur des réseaux IPv6 et IPv4.

Windows Sockets considère chaque suite de protocole réseau comme une famille d’adresses unique. Le protocole IPv6 est donc considéré comme la famille d’adresses **\_ inet6** et le protocole IPv4 sont considérés comme la famille d’adresses d' **\_ inet AF** . Les protocoles IPv6 et IPv4 prennent en charge l’utilisation de différents protocoles IP en couche tels que TCP, UDP et ICMP.

Les sockets Windows ont été initialement conçus pour ajouter la prise en charge de IPv4 à Windows. Toutefois, l’interface de programmation Windows Sockets a été conçue à partir du début avec la possibilité de prendre en charge d’autres suites de protocoles réseau. Au fil du temps, les versions de Windows et les sockets Windows associés ont inclus une prise en charge native pour d’autres suites de protocoles réseau (IPX/SPX et AppleTalk, par exemple). La prise en charge d’autres protocoles réseau était également disponible pour les versions de Windows en tant que logiciels tiers des fournisseurs.

Avant la croissance et la popularité d’Internet, plusieurs autres suites de protocoles réseau étaient utilisées dans les environnements réseau, en particulier pour les intranets locaux. Le choix d’une suite de protocoles réseau était souvent basé sur la taille du réseau ou l’expertise de l’équipe de mise en réseau informatique. Avec la connectivité Internet mondiale d’aujourd’hui qui relie même les plus petits réseaux au reste du monde, l’expertise en matière de mise en réseau dans IPv6 et IPv4 est essentielle pour les professionnels du réseau. Par conséquent, d’autres suites de protocoles réseau précédemment importantes sont désormais utilisées avec une utilisation très limitée et sont devenues ignoré. La prise en charge native de ces suites de protocoles réseau ignoré, souvent appelées protocoles réseau hérités, a été supprimée des versions récentes de Microsoft Windows. La prise en charge de certains de ces protocoles hérités peut être disponible en tant que logiciel tiers des fournisseurs (ATM avec matériel réseau ATM, par exemple).

Le tableau suivant identifie la prise en charge native de Windows pour les suites de protocoles réseau courantes. 

| Protocole réseau                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>                 | Pris en charge<br/>                 | Non pris en charge (voir les remarques)<br/> |
| IPv4<br/>                  | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>                 | Pris en charge<br/>                 | Pris en charge<br/>                 |
| NetBIOS (voir les remarques) <br/>  | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>                 | Pris en charge<br/>                 | Pris en charge<br/>                 |
| IrDA (voir les remarques)<br/>      | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>                 | Pris en charge<br/>                 | Pris en charge<br/>                 |
| Bluetooth (voir les notes)<br/> | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>     | Pris en charge<br/>                 | Pris en charge<br/>                 | Non pris en charge<br/>             |
| IPX/SPX<br/>               | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/> | Pris en charge<br/>                 | Pris en charge<br/>                 | Pris en charge<br/>                 |
| AppleTalk<br/>             | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/> | Pris en charge<br/>                 | Pris en charge<br/>                 | Pris en charge<br/>                 |
| DLS<br/>                   | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge (voir les remarques)<br/> | Non pris en charge (voir les remarques)<br/> | Pris en charge<br/>                 |
| ATM<br/>                   | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/> | Pris en charge (voir les remarques)<br/>     | Pris en charge (voir les remarques)<br/>     | Pris en charge (voir les remarques)<br/>     |
| Protocole<br/>               | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/> | Non pris en charge<br/>             | Non pris en charge<br/>             | Pris en charge (voir les remarques)<br/>     |



 

**IPv6 sur Windows 2000 :** Le protocole IPv6 est pris en charge sur Windows 2000 avec Service Pack 1 (SP1) et versions ultérieures avec la version préliminaire de la technologie Microsoft IPv6 pour Windows 2000.

**NetBIOS :** Le protocole NetBIOS est couramment utilisé par les services d’attribution de noms sur Windows. NetBIOS peut utiliser plusieurs suites de protocoles réseau, notamment IP (NetBIOS sur TCP/IP), IPX/SPX et NetBEUI. Winsock prend en charge NetBIOS sur TCP/IP (appelez couramment NetBT) uniquement sur les versions 32 bits de Windows 7, Windows Server 2008 et Windows Vista. Winsock prend en charge NetBIOS sur TCP/IP et NetBIOS à l’aide d’IPX sur Windows Server 2003 et Windows XP. Winsock prend en charge NetBIOS sur TCP/IP, NetBIOS à l’aide d’IPX et NetBIOS à l’aide de NetBEUI sur Windows 2000.

**IrDA :** Le protocole IrDA (Infrared Data Association) est pris en charge si un port infrarouge et un pilote sont installés sur l’ordinateur.

**Bluetooth :** La prise en charge de Winsock pour Bluetooth en tant que suite de protocole réseau comprend les profils réseau personnel Bluetooth et accès réseau à distance (DUN). La prise en charge de Bluetooth dans Windows comprend également l’utilisation du périphérique d’interface utilisateur Bluetooth (HID) et d’autres profils pour la connexion aux claviers, appareils de pointage et autres périphériques d’entrée qui ne sont pas liés aux protocoles réseau.

**DLC sur windows 2003 et Windows XP :** Le protocole DLC (Data Link Control) est pris en charge sur Windows Server 2003 et Windows XP lorsque le pilote DLC inclus avec Microsoft Host Integration Server 2006, Host Integration Server 2004 ou Host Integration Server 2000 est installé.

**ATM sur windows 2003, Windows XP et windows 2000 :** Le protocole ATM (Asynchronous Transfer Mode) est pris en charge sur Windows Server 2003, Windows XP et Windows 2000 lorsqu’une carte réseau ATM est installée. Le protocole d’adresse IP classique sur ATM (parfois abrégé en « CLIP/ATM ») est défini dans le [document RFC 2225](https://tools.ietf.org/html/rfc2225) et dans les documents associés publiés par l’IETF. Windows Server 2003, Windows XP et Windows 2000 fournissent une implémentation complète de cette norme.

**NetBEUI sur Windows 2000 :** Le protocole NetBEUI n’est pas directement pris en charge par Windows Sockets. Toutefois, le protocole NetBIOS qui peut utiliser plusieurs protocoles réseau prend en charge l’utilisation du protocole NetBEUI sur Windows 2000.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations techniques de référence sur ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[Version préliminaire de la technologie IPv6 pour Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[IrDA](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Prise en charge NDIS 5,0 et ATM dans Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
