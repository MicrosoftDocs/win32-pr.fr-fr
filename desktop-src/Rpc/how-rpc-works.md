---
title: Fonctionnement de RPC
description: Les outils RPC s’affichent pour les utilisateurs comme si un client appelle directement une procédure située dans un programme serveur distant.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229158"
---
# <a name="how-rpc-works"></a>Fonctionnement de RPC

Les outils RPC s’affichent pour les utilisateurs comme si un client appelle directement une procédure située dans un programme serveur distant. Le client et le serveur ont chacun leurs propres espaces d’adressage ; autrement dit, chaque a sa propre ressource mémoire allouée aux données utilisées par la procédure. La figure ci-dessous illustre l’architecture RPC.

![architecture RPC](images/prog-a11.png)

Comme le montre l’illustration, l’application cliente appelle une procédure stub locale au lieu du code réel qui implémente la procédure. Les stubs sont compilés et liés à l’application cliente. Au lieu de contenir le code réel qui implémente la procédure distante, le code stub du client :

-   Récupère les paramètres requis à partir de l’espace d’adressage du client.
-   Traduit les paramètres en fonction des besoins dans un format de rapport de non-remise standard pour la transmission sur le réseau.
-   Appelle des fonctions dans la bibliothèque Runtime du client RPC pour envoyer la demande et ses paramètres au serveur.

Le serveur effectue les étapes suivantes pour appeler la procédure distante.

1.  Les fonctions de la bibliothèque Runtime RPC du serveur acceptent la demande et appellent la procédure stub du serveur.
2.  Le stub serveur récupère les paramètres à partir de la mémoire tampon réseau et les convertit du format de transmission réseau au format requis par le serveur.
3.  Le stub serveur appelle la procédure réelle sur le serveur.

La procédure distante s’exécute, générant éventuellement des paramètres de sortie et une valeur de retour. Une fois la procédure distante terminée, une séquence d’étapes similaire retourne les données au client.

1.  La procédure distante retourne ses données au stub serveur.
2.  Le stub serveur convertit les paramètres de sortie au format requis pour la transmission sur le réseau et les retourne aux fonctions de la bibliothèque Runtime RPC.
3.  Les fonctions de la bibliothèque Runtime RPC du serveur transmettent les données sur le réseau à l’ordinateur client.

Le client termine le processus en acceptant les données sur le réseau et en le retournant à la fonction appelante.

1.  La bibliothèque Runtime RPC client reçoit les valeurs de retour de procédure distante et les retourne au stub client.
2.  Le stub client convertit les données de son rapport de non-remise au format utilisé par l’ordinateur client. Le stub écrit des données dans la mémoire du client et retourne le résultat au programme appelant sur le client.
3.  La procédure appelante continue comme si la procédure avait été appelée sur le même ordinateur.

Les bibliothèques Runtime sont fournies en deux parties : une bibliothèque d’importation, qui est liée à l’application et à la bibliothèque Runtime RPC, qui est implémentée en tant que bibliothèque de liens dynamiques (DLL).

L’application serveur contient des appels aux fonctions de la bibliothèque Runtime du serveur qui inscrivent l’interface du serveur et permettent au serveur d’accepter les appels de procédure distante. L’application serveur contient également les procédures distantes spécifiques à l’application qui sont appelées par les applications clientes.

 

 




