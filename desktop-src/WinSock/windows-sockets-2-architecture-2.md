---
description: l’architecture Windowss de sockets 2 (Winsock) est conforme à l’architecture WOSA (Open System architecture) Windows.
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Architecture de sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918944"
---
# <a name="windows-sockets-2-architecture"></a>Windows Architecture de sockets 2

l’architecture Windows sockets 2 est conforme à l’architecture WOSA (Open System architecture) Windows, comme illustré ci-dessous :

![architecture Windows Sockets 2](images/ovrvw2-1.png)

Winsock définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), avec ses fonctions exportées à partir de WS2 \_32.dll et les piles de protocole. par conséquent, la prise en charge de Winsock n’est pas limitée aux piles de protocole TCP/IP, comme c’est le cas pour les sockets de Windows 1,1.

avec l’architecture Windows sockets 2, il n’est pas nécessaire ou souhaitable pour les fournisseurs de pile de fournir leur propre implémentation de WS2 \_32.dll, car un seul ws2 \_32.dll doit fonctionner sur toutes les piles. Les \_32.dll WS2 et les shims de compatibilité doivent être affichés de la même façon qu’un composant du système d’exploitation.

 

 



