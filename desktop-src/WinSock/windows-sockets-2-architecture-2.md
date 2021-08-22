---
description: l’architecture Windowss de sockets 2 (Winsock) est conforme à l’architecture WOSA (Open System architecture) Windows.
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Architecture de sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569152"
---
# <a name="windows-sockets-2-architecture"></a>Windows Architecture de sockets 2

l’architecture Windows sockets 2 est conforme à l’architecture WOSA (Open System architecture) Windows, comme illustré ci-dessous :

![architecture Windows Sockets 2](images/ovrvw2-1.png)

Winsock définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), avec ses fonctions exportées à partir de WS2 \_32.dll et les piles de protocole. par conséquent, la prise en charge de Winsock n’est pas limitée aux piles de protocole TCP/IP, comme c’est le cas pour les sockets de Windows 1,1.

avec l’architecture Windows sockets 2, il n’est pas nécessaire ou souhaitable pour les fournisseurs de pile de fournir leur propre implémentation de WS2 \_32.dll, car un seul ws2 \_32.dll doit fonctionner sur toutes les piles. Les \_32.dll WS2 et les shims de compatibilité doivent être affichés de la même façon qu’un composant du système d’exploitation.

 

 



