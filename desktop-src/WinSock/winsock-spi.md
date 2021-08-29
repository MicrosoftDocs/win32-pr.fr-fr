---
description: Windows Interface du fournisseur de services (SPI) de Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec29ad26d97b62c884d2944b31d54c94ea1f61b02f74de28c6ff4c84acc6a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051327"
---
# <a name="winsock-spi"></a>SPI Winsock

L’interface du fournisseur de services Winsock, ou Winsock SPI, est une discipline spécifique de Winsock utilisée pour créer des fournisseurs. les fournisseurs de transport tels que les piles de protocoles TCP/IP ou IPX/SPX utilisent le SPI Winsock, de même que les fournisseurs d’espaces de noms tels que le système de noms de domaine (DNS) d’Internet.

La programmation réseau traditionnelle, telle que l’activation des applications pour communiquer sur le réseau, ne nécessite pas l’utilisation d’interfaces Winsock SPI. Utilisez à la place des interfaces [Winsock](winsock-reference.md) standard.

 

Le SPI Winsock utilise la Convention d’affectation de noms de préfixe de fonction suivante.



| Préfixe | Signification                          | Description                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Windows Fournisseur de services de Sockets | Points d’entrée du fournisseur de services de transport           |
| WPU    | Windows Appel du fournisseur de Sockets  | Ws2 \_32.dll points d’entrée pour les fournisseurs de services    |
| WSC    | Windows Configuration des sockets    | WS2 \_32.dll points d’entrée pour les applets d’installation |
| LECTEURS    | Fournisseur d’espace de noms               | Points d’entrée du fournisseur d’espaces de noms                   |



 

 

 



