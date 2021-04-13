---
description: Veillez à prendre en compte toutes les différences entre l’ordonnancement d’octets utilisé pour stocker des entiers par l’architecture de l’hôte et l’ordre des octets utilisé sur le câble par les protocoles de transport individuels.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Classement des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484953"
---
# <a name="byte-ordering"></a>Classement des octets

Veillez à prendre en compte toutes les différences entre l’ordonnancement d’octets utilisé pour stocker des entiers par l’architecture de l’hôte et l’ordre des octets utilisé sur le câble par les protocoles de transport individuels. Toute référence à une adresse ou à un numéro de port transmis à ou à partir d’une routine Windows Sockets doit se trouver dans l’ordre de réseau (Big-endian) pour le protocole utilisé. Dans le cas d’IP, cela comprend l’adresse IP et les paramètres de port d’une structure [**sockaddr**](sockaddr-2.md) (mais pas le paramètre de *\_ famille Sin* ).

Un certain nombre de systèmes UNIX fonctionnent sur des unités centrales qui représentent des entiers dans l’ordre d’octet (Big-endian) réseau. Par conséquent, la nécessité de convertir des entiers de l’ordre d’octet de l’hôte en ordre d’octet réseau peut être ignorée sans causer de problèmes, même si cela n’est pas recommandé pour la portabilité.

En revanche, l’ordre des octets utilisé pour représenter les entiers par la plupart des processeurs® Intel est Little-endian. Il devient donc obligatoire que les entiers soient convertis de l’ordre d’octet de l’hôte en ordre d’octet réseau, avant d’être utilisés dans les structures et les fonctions Winsock Sockets.

Prenons l’exemple d’une application qui contacte normalement un serveur sur le port TCP correspondant au service de temps, mais qui fournit un mécanisme permettant à l’utilisateur de spécifier un autre port. Le numéro de port renvoyé par [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) est déjà dans l’ordre du réseau, qui est le format requis pour construire une adresse afin qu’aucune traduction ne soit requise. Toutefois, si l’utilisateur choisit d’utiliser un autre port, entré sous la forme d’un entier, l’application doit la convertir de l’hôte en ordre de réseau TCP/IP (à l’aide de la fonction [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) ou [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) avant de l’utiliser pour construire une adresse. À l’inverse, si l’application devait afficher le numéro du port dans une adresse (retourné par [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) par exemple), le numéro de port doit être converti de l’ordre réseau à l’ordinateur hôte (à l’aide de la fonction [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) ou [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) avant de pouvoir être affiché.

Étant donné que les commandes d’octet Intel et Internet sont différentes, les conversions décrites dans les précédentes sont inévitables. Les enregistreurs d’applications doivent utiliser les fonctions de conversion standard fournies dans le cadre de Winsock plutôt que d’écrire leur propre code de conversion dans la mesure où les futures implémentations de Winsock sont susceptibles de s’exécuter sur des systèmes dont l’ordre des hôtes est identique à l’ordre des octets du réseau. Seules les applications qui utilisent les fonctions de conversion standard entre l’hôte et l’ordre des octets du réseau sont susceptibles d’être portables.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



