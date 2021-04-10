---
description: Cette section décrit les fonctions, les structures de données et les contrôles de protocole TCP/IP (Transmission Control Protocol/Internet Protocol).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP annexe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201823"
---
# <a name="winsock-tcpip-annex"></a>Winsock TCP/IP annexe

Cette section décrit les fonctions, les structures de données et les contrôles de protocole TCP/IP (Transmission Control Protocol/Internet Protocol).



| Élément          | Description                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nom (s) de protocole | TCP, UDP                                                                                                                                    |
| Description      | Fournit des services de transport sur la couche de mise en réseau IP : UDP pour les datagrammes non fiables, TCP pour les flux d’octets orientés connexion fiables. |
| Famille d’adresses   | **AF \_ INET**, **AF \_ inet6**                                                                                                                 |
| Fichier d’en-tête      | *Ws2tcpip. h*                                                                                                                                |



 

Deux types de services de transport de base sont proposés : les datagrammes non fiables (UDP) et les flux d’octets (TCP) fiables basés sur les connexions. En outre, un socket brut est éventuellement pris en charge. Les sockets bruts permettent à une application de communiquer via des protocoles autres que TCP et UDP tels que ICMP. Les sockets bruts sont pris en charge sur les familles d’adresses **AF \_ inet** et **AF \_ inet6** avec certaines limitations.

Cette section décrit les extensions de Winsock qui sont spécifiques aux protocoles TCP/IP. Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique lors de l’utilisation de TCP/IP.

 

 



