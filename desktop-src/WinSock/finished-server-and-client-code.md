---
description: Exécution de l’exemple de code complet du client TCP/IP et de l’application serveur.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Exécution de l’exemple de code du client et du serveur Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008280"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Exécution de l’exemple de code du client et du serveur Winsock

Cette section contient le code source complet pour les applications clientes et serveur TCP/IP :

-   [Code client Winsock complet](complete-client-code.md)
-   [Compléter le code du serveur Winsock](complete-server-code.md)

L’application serveur doit être démarrée avant le démarrage de l’application cliente.

Pour exécuter le serveur, compilez le code source complet du serveur et exécutez le fichier exécutable. L’application serveur écoute sur le port TCP 27015 pour qu’un client se connecte. Une fois qu’un client se connecte, le serveur reçoit des données du client et renvoie (envoie) les données reçues au client. Lorsque le client arrête la connexion, le serveur arrête le socket client, ferme le socket et se ferme.

Pour exécuter le client, compilez le code source complet du client et exécutez le fichier exécutable. L’application cliente exige que le nom de l’ordinateur ou de l’adresse IP de l’ordinateur sur lequel l’application serveur s’exécute est passé en tant que paramètre de ligne de commande lors de l’exécution du client. Si le client et le serveur sont exécutés sur l’ordinateur d’exemple, le client peut être démarré comme suit :

**localhost du client**

Le client tente de se connecter au serveur sur le port TCP 27015. Une fois que le client se connecte, le client envoie des données au serveur et reçoit toutes les données renvoyées par le serveur. Le client ferme ensuite le socket et s’arrête.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



