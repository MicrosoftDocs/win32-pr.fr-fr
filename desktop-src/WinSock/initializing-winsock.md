---
description: Tous les processus (applications ou dll) qui appellent des fonctions Winsock doivent initialiser l’utilisation de la DLL Windows Sockets avant d’effectuer d’autres appels de fonctions Winsock. Cela permet également de s’assurer que Winsock est pris en charge sur le système.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Initialisation de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526158"
---
# <a name="initializing-winsock"></a>Initialisation de Winsock

Tous les processus (applications ou dll) qui appellent des fonctions Winsock doivent initialiser l’utilisation de la DLL Windows Sockets avant d’effectuer d’autres appels de fonctions Winsock. Cela permet également de s’assurer que Winsock est pris en charge sur le système.

**Pour initialiser Winsock**

1.  Créez un objet [**wsadata,**](/windows/desktop/api/winsock/ns-winsock-wsadata) appelé wsadata,.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Appelez [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) et retournez sa valeur sous la forme d’un entier et recherchez les erreurs.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

La fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) est appelée pour initier l’utilisation de WS2 \_32.dll.

La structure [**wsadata,**](/windows/desktop/api/winsock/ns-winsock-wsadata) contient des informations sur l’implémentation de Windows Sockets. Le paramètre MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) envoie une demande pour la version 2,2 de Winsock sur le système et définit la version passée comme la version la plus récente de prise en charge de Windows Sockets que l’appelant peut utiliser.

Étape suivante pour un client : [création d’un socket pour le client](creating-a-socket-for-the-client.md)

Étape suivante pour un serveur : [création d’un socket pour le serveur](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Création d’une application Winsock de base](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



