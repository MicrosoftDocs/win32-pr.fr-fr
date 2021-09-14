---
description: fournisseurs de services de Transport et Windows sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Fournisseurs de services de transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237120"
---
# <a name="transport-service-providers"></a>Fournisseurs de services de transport

Un fournisseur de services de transport donné prend en charge un ou plusieurs protocoles. Par exemple, un fournisseur TCP/IP fournit, au minimum, les protocoles TCP et UDP, tandis qu’un fournisseur IPX/SPX peut fournir IPX, SPX et SPX II. Chaque protocole pris en charge par un fournisseur particulier est décrit par une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) , et l’ensemble total de ces structures peut être considéré comme le catalogue des protocoles installés. Les applications peuvent récupérer le contenu de ce catalogue (pour plus d’informations, consultez [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)et [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)), et en examinant les structures d' **\_ informations de WSAPROTOCOL** disponibles, Découvrez les attributs de communication associés à chaque protocole.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocoles en couches et chaînes de protocole dans l’index SPI

Windows Les sockets 2 prennent en charge le concept de protocole en couches. Un protocole en couches est un protocole qui implémente uniquement les fonctions de communication de niveau supérieur, tout en s’appuyant sur une pile de transport sous-jacente pour l’échange réel de données avec un point de terminaison distant. Un exemple d’un tel protocole en couches est une couche de sécurité qui ajoute le protocole au processus d’établissement de la connexion afin d’effectuer l’authentification et d’établir un schéma de chiffrement convenu mutuellement. Un tel protocole de sécurité nécessite généralement les services d’un protocole de transport Reliable sous-jacent, tel que TCP ou SPX. Le terme protocole de base fait référence à un protocole tel que TCP ou SPX qui est entièrement capable d’effectuer des communications de données avec un point de terminaison distant, et le terme protocole à couches est utilisé pour décrire un protocole qui ne peut pas être autonome. Une chaîne de protocole est ensuite définie comme un ou plusieurs protocoles superposés chaînées et ancrés par un protocole de base.

Cette chaîne de protocoles en couches et de protocoles de base en chaînes peut être obtenue en organisant les protocoles en couches afin de prendre en charge le SPI Winsock à la fois sur leurs bords supérieurs et inférieurs. Une structure [**d' \_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) spéciale est créée, qui fait référence à la chaîne de protocole dans son ensemble et qui décrit l’ordre explicite dans lequel les protocoles en couches sont joints. Cela est illustré dans le graphique suivant.

![chaîne de protocole](images/ovrvw2-3.png)

 

 
