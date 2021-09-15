---
title: Utilisation de Bluetooth
description: cette section décrit les tâches liées à l’écriture d’applications basées sur des Windows pour Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414019"
---
# <a name="using-bluetooth"></a>Utilisation de Bluetooth

cette section décrit les tâches liées à l’écriture d’applications basées sur des Windows pour Bluetooth.

Bluetooth fournit des définitions de programmation dans les fichiers Ws2bth. h et BluetoothAPIs. h. Le fichier Bthsdpdef. h doit être inclus avant BluetoothAPIs. h. le fichier Ws2bth. h doit être inclus après Winsock2. h pour utiliser Bluetooth sockets. Liez uniquement à bthprops. lib et évitez la liaison à irprops. lib. Irprops. lib est fourni à des fins de compatibilité descendante uniquement. Bthprops. lib est disponible dans le kit de développement logiciel (SDK) Windows Vista. vous pouvez utiliser le kit de développement logiciel (SDK) Windows Vista pour développer des applications pour Windows XP avec Service Pack 2 (SP2). le kit de développement logiciel (SDK) Windows Vista est disponible dans le [centre de téléchargement](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Tous les mécanismes standard synchrones et superposés pour lire et écrire des données qui sont actuellement prises en charge avec d’autres familles d’adresses fonctionnent correctement avec la famille d’adresses de la vue \_ BTH.

le kit de développement logiciel (SDK) contient un exemple de code qui illustre une application simple Bluetooth utilisant le protocole Winsock 2,2 et RFCOMM. le code source de l’exemple se trouve dans l’emplacement d’installation du kit de développement logiciel (sdk) sous C : \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ samples \\ NetDs \\ winsock \\ Bluetooth.

Cette section décrit les rubriques suivantes.



| Section                                                                                      | Contenu                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth programmation avec des sockets Windows](bluetooth-programming-with-windows-sockets.md) | explique comment utiliser des interfaces Windows sockets pour implémenter un réseau Bluetooth. |



 

 

 




