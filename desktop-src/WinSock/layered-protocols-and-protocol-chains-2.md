---
description: 'Windows Sockets 2 intègre le concept de protocole en couches : un qui implémente uniquement les fonctions de communication de niveau supérieur tout en s’appuyant sur une pile de transport sous-jacente pour l’échange de données réel avec un point de terminaison distant.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocoles et chaînes de protocole en couches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113047"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocoles et chaînes de protocole en couches

Windows Sockets 2 intègre le concept de protocole en couches : un qui implémente uniquement les fonctions de communication de niveau supérieur tout en s’appuyant sur une pile de transport sous-jacente pour l’échange de données réel avec un point de terminaison distant. Un exemple de ce type de protocole superposé est une couche de sécurité qui ajoute un protocole au processus de connexion de socket afin d’effectuer l’authentification et d’établir un schéma de chiffrement. Un tel protocole de sécurité nécessite généralement les services d’un protocole de transport sous-jacent et fiable, tel que TCP ou SPX.

Le terme *protocole de base* fait référence à un protocole, tel que TCP ou SPX, qui est entièrement capable d’effectuer des communications de données avec un point de terminaison distant. Un *protocole en couches* est un protocole qui ne peut pas être autonome, tandis qu’une *chaîne de protocole* est un ou plusieurs protocoles en couche chaînées et ancrés par un protocole de base.

Vous pouvez créer une chaîne de protocole si vous concevez les protocoles superposés pour prendre en charge le SPI Windows Sockets 2 à la fois sur leurs bords supérieurs et inférieurs. Une structure [**spéciale \_ info WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fait référence à la chaîne de protocole dans son ensemble et décrit l’ordre explicite dans lequel les protocoles en couches sont joints. Cela est illustré dans la figure ci-dessous. Étant donné que seuls les protocoles de base et les chaînes de protocole sont directement utilisables par les applications, ils sont les seuls répertoriés lorsque les protocoles installés sont énumérés avec la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

![architecture de protocole en couches](images/ovrvw2-3.png)

 

 
