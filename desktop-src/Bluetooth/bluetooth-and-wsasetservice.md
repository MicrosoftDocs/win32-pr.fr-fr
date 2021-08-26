---
title: Bluetooth et WSASetService
description: Bluetooth utilise la fonction WSASetService pour inscrire ou supprimer une instance de service dans l’espace de noms Bluetooth (NS \_ BTH) à partir du registre.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth et WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671e43636de67cee1e1c3c945a3647b5db59e7b0dd22b6eefd70b51f4977c31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004169"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth et WSASetService

Bluetooth utilise la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour inscrire ou supprimer une instance de service dans l’espace de noms Bluetooth (NS \_ BTH) à partir du registre. Le handle retourné par cette opération ne peut être utilisé que pour supprimer le service.

Bluetooth a deux moyens de publier des services à l’aide de la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   l’application peut faire en sorte que le système publie un simple Bluetooth enregistrement de service SDP, construit à partir des membres standard de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   l’application peut faire en sorte que le système publie sa propre Bluetooth enregistrement SDP en passant une structure de [**\_ \_ SERVICE d’ensemble BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) dans le membre **lpBlob** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Il s’agit d’une approche plus complexe.

> [!Note]  
> Les enregistrements SDP publiés par [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) ne sont pas conservés une fois que le processus qui les a publiés s’est arrêté.

 

l’utilisation de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) avec Bluetooth présente les exigences suivantes :

-   Le paramètre *lpqsRegInfo* est l’adresse de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) à inscrire.
-   Le paramètre *essOperation* est une énumération qui contient l’une des opérations répertoriées dans le tableau suivant.



| Valeur                  | Description                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| \_Registre RNRSERVICE   | démarre la publication du service sur les radios distantes qui interrogent à l’aide du protocole SDP Bluetooth. |
| \_désinscription RNRSERVICE | Non valide. Retourne une erreur.                                                               |
| RNRSERVICE \_ Supprimer     | Arrête la publication du service.                                                             |



 

> [!Note]  
> Les handles de service détectés pendant un appel [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) sont incompatibles avec l’opération de suppression de RNRSERVICE \_ .

 

-   Le paramètre *dwControlFlags* est réservé et doit être égal à zéro.

pour plus d’informations et pour obtenir la liste des options de socket Bluetooth, consultez options de socket [et de Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 