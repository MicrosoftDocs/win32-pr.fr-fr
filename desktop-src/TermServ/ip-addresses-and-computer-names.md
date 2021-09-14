---
title: Adresses IP et noms d’ordinateurs
description: Il est déconseillé de supposer que le nom d’ordinateur ou l’ adresse IP affectée à l’ordinateur sont associés à un seul utilisateur, étant donné que plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de Session Bureau à distance.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118633"
---
# <a name="ip-addresses-and-computer-names"></a>Adresses IP et noms d’ordinateurs

Plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Par conséquent, il n’est pas possible de supposer que le nom de l’ordinateur ou l’adresse IP affectée à l’ordinateur sont associés à un seul utilisateur. cela diffère d’un environnement de Windows d’un seul utilisateur, dans lequel un seul utilisateur est connecté à la fois.

Les applications qui utilisent le nom d’ordinateur ou l’adresse IP pour la licence ou comme moyen d’identifier une itération de l’application sur le réseau ne fonctionneront pas correctement dans un environnement Services Bureau à distance, car le nom d’ordinateur ou l’adresse IP du serveur peut être associé à de nombreux utilisateurs.

Dans un environnement de Services Bureau à distance, chaque terminal client ou émulateur de terminal possède une adresse IP et un nom d’ordinateur distincts. Pour récupérer l’adresse IP et le nom d’ordinateur d’un client, appelez la fonction [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) . Les autres fonctions qui récupèrent ces adresses réseau et noms d’ordinateurs récupèrent le nom et l’adresse du serveur hôte de session Bureau à distance. Par exemple, la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) retourne le nom d’ordinateur du serveur.

 

 