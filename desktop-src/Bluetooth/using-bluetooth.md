---
title: Utilisation de Bluetooth
description: Cette section décrit les tâches liées à l’écriture d’applications Windows pour Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734532"
---
# <a name="using-bluetooth"></a>Utilisation de Bluetooth

Cette section décrit les tâches liées à l’écriture d’applications Windows pour Bluetooth.

Bluetooth fournit des définitions de programmation dans les fichiers Ws2bth. h et BluetoothAPIs. h. Le fichier Bthsdpdef. h doit être inclus avant BluetoothAPIs. h. Le fichier Ws2bth. h doit être inclus après Winsock2. h pour utiliser les sockets Bluetooth. Liez uniquement à bthprops. lib et évitez la liaison à irprops. lib. Irprops. lib est fourni à des fins de compatibilité descendante uniquement. Bthprops. lib est disponible dans le kit de développement logiciel (SDK) Windows Vista. Vous pouvez utiliser le kit de développement logiciel (SDK) Windows Vista pour développer des applications pour Windows XP avec Service Pack 2 (SP2). Le kit de développement logiciel (SDK) Windows Vista est disponible dans le [Centre de téléchargement](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Tous les mécanismes standard synchrones et superposés pour lire et écrire des données qui sont actuellement prises en charge avec d’autres familles d’adresses fonctionnent correctement avec la famille d’adresses de la vue \_ BTH.

Le kit de développement logiciel (SDK) contient un exemple de code qui illustre une application Bluetooth simple utilisant le protocole Winsock 2,2 et RFCOMM. Le code source de l’exemple se trouve dans l’emplacement d’installation du kit de développement logiciel (SDK) sous C : \\ Program Files \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.

Cette section décrit les rubriques suivantes.



| Section                                                                                      | Content                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Programmation Bluetooth avec Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Explique comment utiliser les interfaces Windows Sockets pour implémenter un réseau Bluetooth. |



 

 

 




