---
title: Bluetooth programmation avec des sockets Windows
description: cette section décrit comment utiliser des structures et des fonctions Windows sockets pour programmer une application Bluetooth.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, tâches
- Windows Sockets
- programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230735"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth programmation avec des sockets Windows

cette section décrit comment utiliser des structures et des fonctions Windows sockets pour programmer une application Bluetooth. vous trouverez des informations de référence complètes sur les éléments de l’API Windows sockets dans [Windows sockets](/windows/desktop/WinSock/windows-sockets-start-page-2). cette section fournit uniquement des informations spécifiques Bluetooth pour chaque élément de programmation Windows sockets.

vous pouvez également télécharger l’exemple de [connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) pour obtenir un exemple complet.

comme pour la programmation d’applications de Windows sockets, la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) doit être appelée pour initier la fonctionnalité de sockets Windows et activer les Bluetooth.

les rubriques suivantes fournissent des conseils pour l’utilisation de Windows fonctions et de structures de sockets avec l’API Microsoft Bluetooth :



| Rubrique                                                                                            | Description                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth et accepter](bluetooth-and-accept.md)                                                 | Bluetooth utilise la fonction [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) pour activer les tentatives de connexion entrante sur un socket.<br/>                                                                                                                                                                                                  |
| [Bluetooth et lier](bluetooth-and-bind.md)                                                     | Bluetooth utilise la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) pour établir une liaison à un socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth et objet BLOB](bluetooth-and-blob.md)                                                     | Bluetooth utilise la structure d' [**objets BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) pour transmettre ou recevoir des données spécifiques au transport vers la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) lors des appels aux fonctions [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* . <br/>             |
| [Bluetooth et se connecter](bluetooth-and-connect.md)                                               | Bluetooth utilise la fonction [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) pour se connecter à un appareil Bluetooth cible, à l’aide d’un socket Bluetooth créé précédemment.<br/>                                                                                                                                                              |
| [Bluetooth et getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | La fonction [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) permet de traduire le nom d’hôte en adresse pour les transports basés sur IP.<br/>                                                                                                                                                                                   |
| [Bluetooth et getpeername](bluetooth-and-getpeername.md)                                       | utilisé pour récupérer l’adresse Bluetooth de l’homologue Bluetooth appareil.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth et getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth utilise la fonction [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) pour récupérer l’adresse de l’appareil serveur et le numéro de port alloués à un socket par le biais d’un appel précédent à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth et getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth utilise la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pour interroger différents paramètres associés au canal du serveur ou à la connexion. <br/>                                                                                                                                                           |
| [Bluetooth et écouter, sélectionner et opération closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth utilise les fonctions [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)et [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sans aucune modification de la programmation standard Windows sockets.<br/>                                                                                                   |
| [Bluetooth et opérations de lecture ou d’écriture](bluetooth-and-read-or-write-operations.md)             | Détaille les opérations de lecture et d’écriture Winsock prises en charge.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth et setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth utilise la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir différents paramètres associés au canal du serveur ou à la connexion.<br/>                                                                                                                                                              |
| [Bluetooth et arrêt](bluetooth-and-shutdown.md)                                             | Bluetooth utilise la fonction [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) pour se déconnecter de la radio distante.<br/>                                                                                                                                                                                                             |
| [Bluetooth et socket](bluetooth-and-socket.md)                                                 | Bluetooth utilise la fonction [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) pour créer un socket pour les connexions entrantes ou sortantes.<br/>                                                                                                                                                                                               |
| [Options de Bluetooth et de Socket](bluetooth-and-socket-options.md)                                 | Décrit en détail les options de socket prises en charge par Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth et WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | utilisé pour convertir une adresse d’appareil Bluetooth en chaîne, qui est à son tour fournie à la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) via la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) lors de la récupération des informations de service de l’appareil.<br/>                                           |
| [Bluetooth et WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour interroger les appareils et découvrir les services.<br/>                                                                                                                                                                         |
| [Bluetooth et WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth utilise la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) pour faire correspondre les requêtes spécifiées dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth et WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth utilise la fonction [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) pour terminer une requête lancée dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), et peut-être étendue dans les appels suivants à [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth et WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | La structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) est utilisée dans les opérations, notamment la consultation des appareils, la consultation des services et la définition du service.<br/>                                                                                                                                                                |
| [Bluetooth et WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth utilise la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour inscrire ou supprimer une instance de service dans l’espace de noms Bluetooth (NS \_ BTH) à partir du registre.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

