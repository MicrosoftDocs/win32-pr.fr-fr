---
description: Un processus utilise la fonction CreateFile pour ouvrir un handle vers une ressource de communication.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Descripteurs de ressources de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393087"
---
# <a name="communications-resource-handles"></a>Descripteurs de ressources de communication

Un processus utilise la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle vers une ressource de communication. Par exemple, si vous spécifiez COM1, un handle est ouvert à un port série et LPT1 ouvre un handle vers un port parallèle. Si la ressource spécifiée est actuellement utilisée par un autre processus, **CreateFile** échoue. Tout thread du processus peut utiliser le handle retourné par **CreateFile** pour identifier la ressource dans toutes les fonctions qui accèdent à la ressource.

Lorsque le processus appelle [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir une ressource de communication, il spécifie les attributs suivants :

-   Quel type d’accès en lecture/écriture existe pour la ressource spécifiée.
-   Indique si le handle peut être hérité par les processus enfants.
-   Indique si le handle peut être utilisé dans les opérations d’e/s (asynchrones) avec chevauchement. (Pour obtenir une description des opérations avec chevauchement, consultez [Synchronization](/windows/desktop/Sync/synchronization).)

Lorsque le processus utilise [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir une ressource de communication, il doit spécifier certaines valeurs pour les paramètres suivants :

-   Le paramètre *fdwShareMode* doit être égal à zéro, ouvrant la ressource pour un accès exclusif.
-   Le paramètre *fdwCreate* doit spécifier l' \_ indicateur Open Existing.
-   Le paramètre *hTemplateFile* doit avoir la **valeur null**.

Quand vous utilisez [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle directement sur un appareil, une application doit utiliser les caractères spéciaux « \\ \\ . \\ » pour identifier l’appareil. Par exemple, pour ouvrir un handle pour le pilote A, spécifiez \\ \\ . \\ r : pour le paramètre *lpszName* de **CreateFile**. Le processus appelant peut utiliser le descripteur dans la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) pour envoyer des codes de contrôle à l’appareil.

 

 
