---
description: Exemple d’échange de paquets de protocole SMB Microsoft entre un client et un serveur.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: scénario de Exchange de paquets de protocole SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a03e2f75b00aa93e629b3e698631c5efde4694
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009908"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>scénario de Exchange de paquets de protocole SMB Microsoft

Cette rubrique fournit un exemple d’échange de paquets de protocole SMB Microsoft entre un client et un serveur. Les étapes suivantes sont une vue d’ensemble du processus :

1.  Le client et le serveur établissent une session NetBIOS.
2.  Le client et le serveur négocient le dialecte du protocole SMB Microsoft.
3.  Le client ouvre une session sur le serveur.
4.  Le client se connecte à un partage sur le serveur.
5.  Le client ouvre un fichier sur le partage.
6.  Le client lit à partir du fichier.

Tout d’abord, une connexion TCP en duplex intégral est établie par le client avec le serveur. Ensuite, le client génère et envoie un paquet de demande de session NetBIOS sur la connexion TCP. Si le paquet a été mis en forme correctement, le serveur retourne alors un paquet qui contient un message confirmant que la session a été établie. Après cela, le client envoie les premiers paquets du protocole SMB Microsoft au serveur.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paquet 1 : SMB \_ com \_ Negotiate**<br/> **Direction :** Client à serveur<br/> **Description :** Le client demande que le serveur négocie le dialecte du protocole SMB Microsoft. Une liste de chaînes identifiant les dialectes que le client peut utiliser est incluse dans le paquet.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Paquet 2 : SMB \_ com \_ Negotiate**<br/> **Direction :** Serveur à client<br/> **Description :** Le serveur répond à la demande du client pour identifier le dialecte du protocole SMB Microsoft qui sera utilisé dans la session. Le paquet retourné comprend également une chaîne aléatoire de 8 octets qui sera utilisée à l’étape suivante pour authentifier le client pendant le processus d’ouverture de session.<br/>                                                                                                                                                                                                                                   |
| **Paquet 3 : \_ configuration de \_ session com SMB \_ \_ ANDX**<br/> **Direction :** Client à serveur<br/> **Description :** Ce paquet inclut des informations sur les fonctionnalités du client, ce qui signifie que ce paquet doit être envoyé même si le serveur a implémenté uniquement la sécurité au niveau du partage.<br/> **Paquet 3 : \_ configuration de \_ session com SMB \_ \_ ANDX**<br/> **Direction :** Serveur à client<br/> **Description :** Si la stimulation/réponse est acceptée par le serveur, un UID valide est inclus dans le paquet renvoyé au client. Si elle n’est pas acceptée, le serveur renvoie un code d’erreur dans ce paquet et refuse l’accès.<br/> |
| **Paquet 4 : connexion de l' \_ arborescence com SMB \_ \_ \_ ANDX**<br/> **Direction :** Client à serveur<br/> **Description :** Le client demande l’accès au partage. Le paquet contient le chemin d’accès complet du partage au format UNC.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Paquet 5 : connexion de l' \_ arborescence com SMB \_ \_ \_ ANDX**<br/> **Direction :** Serveur à client<br/> **Description :** Si l’accès au partage est accordé, le serveur retourne l’ID d’arborescence 16 bits (TID) qui correspond au partage dans ce paquet. Si le partage n’existe pas ou si l’utilisateur ne dispose pas des informations d’identification suffisantes pour accéder au partage, le serveur renvoie un code d’erreur dans ce paquet et refuse l’accès au partage.<br/>                                                                                                                                                                                                 |
| **Paquet 6 : \_ \_ ANDX Open com \_ ouvert**<br/> **Direction :** Client à serveur<br/> **Description :** Le client demande au serveur d’ouvrir un fichier sur le partage accessible pour le compte du client. Ce paquet contient le nom du fichier à ouvrir.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Paquet 7 : \_ \_ ANDX Open com \_ ouvert**<br/> **Direction :** Serveur à client<br/> **Description :** Si l’accès au fichier est accordé, le serveur retourne l’ID du fichier demandé. Si le fichier n’existe pas ou si l’utilisateur ne dispose pas des informations d’identification suffisantes pour accéder au fichier, le serveur renvoie un code d’erreur dans ce paquet et refuse l’accès au fichier.<br/>                                                                                                                                                                                                                                                  |
| **Paquet 8 : \_ lecture de \_ \_ ANDX SMB com**<br/> **Direction :** Client à serveur<br/> **Description :** Le client demande au serveur de lire les données du fichier ouvert pour le compte du client et de renvoyer ces données au client. L’ID de fichier obtenu par le client lors de l’ouverture du fichier est inclus dans ce paquet afin d’identifier le fichier ouvert à partir duquel le serveur doit lire les données.<br/>                                                                                                                                                                                                                   |
| **Paquet 9 : \_ lecture de \_ \_ ANDX SMB com**<br/> **Direction :** Serveur à client<br/> **Description :** Le serveur retourne les données de fichier demandées dans ce paquet. Une erreur est peu probable, car l’accès au serveur, au partage et au fichier a été accordé. Cela peut toutefois se produire dans certains cas : par exemple, si l’accès à un partage est modifié entre l’ouverture du fichier et l’heure à laquelle il est lu.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> si vous implémentez un CIFS qui ne prend pas en charge les notifications de modification, Windows ne peut pas conserver un handle en attente dans le système de fichiers et la connexion SMB peut disparaître sans préavis.

 

 

 




