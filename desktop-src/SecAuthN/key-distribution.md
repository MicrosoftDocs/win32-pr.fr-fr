---
description: La technique d’authentification par clé secrète n’explique pas comment le client et le serveur obtiennent la clé de session secrète à utiliser dans les sessions les unes avec les autres.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribution de clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a2968e8b7b978bc7b325d65b4a2acf08e1f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413483"
---
# <a name="key-distribution"></a>Distribution de clés

La technique d’authentification par clé secrète n’explique pas comment le client et le serveur obtiennent la [*clé de session*](../secgloss/s-gly.md) secrète à utiliser dans les sessions les unes avec les autres. S’il s’agit de personnes, elles peuvent respecter le secret et accepter la clé. Toutefois, si le client est un programme exécuté sur une station de travail et que le serveur est un service s’exécutant sur un serveur réseau, cette méthode ne fonctionnera pas.

Un client souhaite communiquer avec de nombreux serveurs et nécessite des clés différentes pour chacun d’eux. Un serveur communique avec de nombreux clients et a besoin de clés différentes pour chacun d’eux. Si chaque client a besoin d’une clé différente pour chaque serveur et que chaque serveur a besoin d’une clé différente pour chaque client, la distribution de clé devient un problème. En outre, la nécessité de stocker et de protéger de nombreuses clés sur de nombreux ordinateurs crée un risque de sécurité énorme.

Le nom du [*protocole Kerberos*](../secgloss/k-gly.md) suggère sa solution au problème de la distribution des clés. Kerberos (ou Cerberus) était une figure dans les Mythology grec classiques, un chien féroce à trois têtes qui a gardé des intrus vivants dans le monde entier. À l’instar de la protection par mythe, le protocole Kerberos comporte trois têtes : un client, un serveur et un tiers de confiance pour effectuer un médiateur entre eux. L’intermédiaire approuvé dans ce protocole est le centre de distribution de clés (KDC).

Le KDC est un service qui s’exécute sur un serveur sécurisé physiquement. Il gère une base de données avec les informations de compte de tous les [*principaux de sécurité*](../secgloss/s-gly.md) dans son domaine. Un domaine est l’équivalent Kerberos d’un domaine dans Windows.

Avec d’autres informations sur chaque principal de sécurité, le KDC stocke une clé de chiffrement connue uniquement du principal et du KDC. Il s’agit de la [*clé principale*](../secgloss/m-gly.md) utilisée pour les échanges entre chaque principal de sécurité et le KDC. Dans la plupart des implémentations du protocole Kerberos, cette clé principale est dérivée à l’aide d’une fonction de [*hachage*](../secgloss/h-gly.md) du mot de passe d’un principal de sécurité.

Lorsqu’un client souhaite créer une connexion sécurisée avec un serveur, le client commence par envoyer une demande au centre de sécurité de l’accès, et non au serveur qu’il souhaite atteindre. Le KDC crée et envoie au client une clé de [*session*](../secgloss/s-gly.md) unique pour le client et un serveur à utiliser pour s’authentifier mutuellement. Le KDC a accès à la clé principale du client et à la clé principale du serveur. Le KDC chiffre la copie du serveur de la clé de session à l’aide de la clé principale du serveur et de la copie du client à l’aide de la clé principale du client.

Le KDC peut jouer son rôle d’intermédiaire approuvé en envoyant la clé de session directement à chaque principal de sécurité impliqué, mais dans la pratique, cette procédure ne fonctionne pas, pour plusieurs raisons. Au lieu de cela, le centre KDC envoie les deux clés de session chiffrées au client. La clé de session du serveur est incluse dans un [ticket de session](session-tickets.md).

 

 
