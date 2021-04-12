---
description: Décrit le processus d’une opération d’e/s réseau sous Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Description d’une opération d’e/s réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319297"
---
# <a name="description-of-a-network-io-operation"></a>Description d’une opération d’e/s réseau

La figure suivante illustre le processus d’une opération d’e/s réseau sous Windows.

![opération d’e/s réseau sous Windows](images/fig4.png)

Quand une application appelle une fonction d’e/s de fichier pour accéder à un fichier sur un ordinateur distant, les événements suivants se produisent :

-   La requête d’e/s est interceptée par un [redirecteur réseau](network-redirectors.md), également appelé simplement redirecteur, sur l’ordinateur local. Cela est représenté dans l’illustration précédente par la flèche pleine entre l’application et le redirecteur du client.
-   Le redirecteur construit un paquet de données contenant toutes les informations sur la demande et l’envoie au serveur où se trouve le fichier. Cela est illustré dans la figure précédente par la flèche pleine entre le redirecteur du client et le redirecteur du serveur.
-   Le redirecteur sur le serveur reçoit le paquet du client, authentifie l’accès au fichier requis par la requête d’e/s et, s’il est authentifié, exécute la demande pour le compte du client. Si ce n’est pas le cas, il renvoie un code d’erreur au redirecteur sur le client. Cela est représenté dans l’illustration précédente par la flèche pleine courbée entre le redirecteur du serveur et le fichier.
-   Lorsque la requête a été exécutée, le redirecteur sur le serveur envoie toutes les données résultant de la demande d’e/s au redirecteur sur le client, ainsi qu’une notification de réussite. Cela est illustré dans la figure précédente par la flèche en pointillés entre le serveur et le redirecteur du client.
-   Le redirecteur sur le client reçoit le paquet du serveur et transmet les données du paquet à l’application, ainsi qu’une notification de réussite. Cela est illustré dans la figure précédente par la flèche pointillée entre le redirecteur du client et l’application.

Windows peut utiliser divers protocoles réseau pour effectuer une opération d’e/s réseau, notamment le [protocole SMB Microsoft et la vue d’ensemble du protocole CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) et NFS.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Différences dans les e/s locales et réseau](differences-in-local-and-network-i-o.md)<br/> | Différences entre les e/s locales et les e/s réseau sur Windows.<br/> |
| [Redirecteurs réseau](network-redirectors.md)<br/>                                   | Décrit les fonctionnalités d’un redirecteur réseau.<br/>      |



 

 

 




