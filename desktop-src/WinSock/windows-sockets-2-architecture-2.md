---
description: L’architecture Windows Sockets 2 (Winsock) est conforme à l’architecture WOSA (Windows Open System Architecture).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architecture Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114299"
---
# <a name="windows-sockets-2-architecture"></a>Architecture Windows Sockets 2

L’architecture Windows Sockets 2 est conforme à l’architecture WOSA (Windows Open System Architecture), comme illustré ci-dessous :

![architecture Windows Sockets 2](images/ovrvw2-1.png)

Winsock définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), avec ses fonctions exportées à partir de WS2 \_32.dll et les piles de protocole. Par conséquent, la prise en charge de Winsock n’est pas limitée aux piles de protocole TCP/IP, comme c’est le cas pour Windows Sockets 1,1.

Avec l’architecture Windows Sockets 2, il n’est pas nécessaire ou souhaitable pour les fournisseurs de pile de fournir leur propre implémentation de WS2 \_32.dll, car un même WS2 \_32.dll doit fonctionner sur toutes les piles. Les \_32.dll WS2 et les shims de compatibilité doivent être affichés de la même façon qu’un composant du système d’exploitation.

 

 



