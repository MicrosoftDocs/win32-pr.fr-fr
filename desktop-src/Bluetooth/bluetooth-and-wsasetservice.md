---
title: Bluetooth et WSASetService
description: Bluetooth utilise la fonction WSASetService pour inscrire ou supprimer une instance de service au sein de l’espace de noms Bluetooth (NS \_ BTH) à partir du Registre.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Bluetooth WSASetService
- Bluetooth et Bluetooth WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463210"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth et WSASetService

Bluetooth utilise la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour inscrire ou supprimer une instance de service au sein de l’espace de noms Bluetooth (NS \_ BTH) à partir du Registre. Le handle retourné par cette opération ne peut être utilisé que pour supprimer le service.

Bluetooth offre deux moyens de publier des services à l’aide de la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   L’application peut demander au système de publier un enregistrement de service SDP Bluetooth simple, construit à partir de membres standard dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   L’application peut faire en sorte que le système publie son propre enregistrement SDP Bluetooth en passant une structure de [**\_ \_ service d’ensemble BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) dans le membre **lpBlob** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Il s’agit d’une approche plus complexe.

> [!Note]  
> Les enregistrements SDP publiés par [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) ne sont pas conservés une fois que le processus qui les a publiés s’est arrêté.

 

L’utilisation de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) avec Bluetooth présente les exigences suivantes :

-   Le paramètre *lpqsRegInfo* est l’adresse de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) à inscrire.
-   Le paramètre *essOperation* est une énumération qui contient l’une des opérations répertoriées dans le tableau suivant.



| Valeur                  | Description                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| \_Registre RNRSERVICE   | Démarre la publication du service sur les radios distantes qui interrogent à l’aide du protocole SDP Bluetooth. |
| \_désinscription RNRSERVICE | Non valide. Retourne une erreur.                                                               |
| RNRSERVICE \_ Supprimer     | Arrête la publication du service.                                                             |



 

> [!Note]  
> Les handles de service détectés pendant un appel [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) sont incompatibles avec l’opération de suppression de RNRSERVICE \_ .

 

-   Le paramètre *dwControlFlags* est réservé et doit être égal à zéro.

Pour plus d’informations et pour obtenir la liste des options de Socket Bluetooth, consultez [options Bluetooth et Socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 