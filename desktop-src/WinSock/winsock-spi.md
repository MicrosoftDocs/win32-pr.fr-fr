---
description: L’interface du fournisseur de services (SPI) de Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517895"
---
# <a name="winsock-spi"></a>SPI Winsock

L’interface du fournisseur de services Winsock, ou Winsock SPI, est une discipline spécifique de Winsock utilisée pour créer des fournisseurs. les fournisseurs de transport tels que les piles de protocoles TCP/IP ou IPX/SPX utilisent le SPI Winsock, de même que les fournisseurs d’espaces de noms tels que le système de noms de domaine (DNS) d’Internet.

La programmation réseau traditionnelle, telle que l’activation des applications pour communiquer sur le réseau, ne nécessite pas l’utilisation d’interfaces Winsock SPI. Utilisez à la place des interfaces [Winsock](winsock-reference.md) standard.

 

Le SPI Winsock utilise la Convention d’affectation de noms de préfixe de fonction suivante.



| Préfixe | Signification                          | Description                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Fournisseur de services Windows Sockets | Points d’entrée du fournisseur de services de transport           |
| WPU    | Appel du fournisseur de sockets Windows  | Ws2 \_32.dll points d’entrée pour les fournisseurs de services    |
| WSC    | Configuration de Windows Sockets    | WS2 \_32.dll points d’entrée pour les applets d’installation |
| LECTEURS    | Fournisseur d’espace de noms               | Points d’entrée du fournisseur d’espaces de noms                   |



 

 

 



