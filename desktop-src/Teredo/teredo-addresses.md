---
title: Adresses Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'En savoir plus sur : adresses Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354135"
---
# <a name="teredo-addresses"></a>Adresses Teredo

Une adresse Teredo se compose des éléments suivants :

-   **Préfixe Teredo**

    Les 32 premiers bits sont pour le préfixe Teredo, qui est le même pour toutes les adresses Teredo. Windows XP et Windows Server 2003 utilisaient initialement le préfixe Teredo 3FFE : 831F ::/32. le préfixe défini pour teredo dans RFC 4380 est 2001 ::/32 et est le préfixe utilisé par teredo dans Windows Vista et Windows Server 2008. les ordinateurs exécutant Windows XP et Windows Server 2003 utilisent le préfixe Teredo 2001 ::/32 quand ils sont mis à jour avec le Bulletin de sécurité Microsoft MS06-064.

-   **Adresse IPv4 du serveur Teredo**

    Les 32 bits suivants contiennent l’adresse IPv4 publique du serveur Teredo qui a aidé à configurer cette adresse Teredo. Pour plus d’informations, consultez « Configuration initiale des clients Teredo » dans cet article.

-   **Indicateurs**

    Les 16 bits suivants pour sont réservés aux indicateurs Teredo. pour les clients Teredo Windows XP, le seul indicateur défini est le bit de poids fort connu sous le nom d’indicateur de cône. L’indicateur conique est défini lorsque le client Teredo se trouve derrière un périphérique NAT conique. Déterminer si le NAT connecté à Internet est un périphérique NAT conique se produit pendant la configuration initiale du client Teredo. Pour plus d’informations, consultez « Configuration initiale des clients Teredo » dans cet article.

    pour les clients Teredo Windows Vista et Windows Server 2008, les bits inutilisés dans le champ flags fournissent un niveau de protection contre les analyses d’adresses par des utilisateurs malveillants. les 16 bits dans le champ flags pour les clients Teredo Windows Vista et Windows Server 2008 se composent des éléments suivants : CRAAAAUG AAAAAAAA. Le bit C est pour l’indicateur de cône. Le bit R est réservé pour une utilisation ultérieure. Le bit U est destiné à l’indicateur Universal/local (défini sur 0). Le bit G est l’indicateur individuel/groupe (défini sur 0). Les bits A sont définis sur un nombre de 12 bits généré de manière aléatoire. En utilisant un nombre aléatoire pour les bits A, un utilisateur malveillant qui a déterminé le reste de l’adresse Teredo en capturant l’échange de la configuration initiale des paquets entre le client Teredo et le serveur Teredo devra essayer jusqu’à 4 096 (212) adresses différentes pour déterminer l’adresse d’un client Teredo au cours d’une analyse d’adresse.

-   **Port externe masqué**

    Les 16 bits suivants stockent une version masquée du port UDP externe correspondant à tout le trafic Teredo pour ce client Teredo. Lorsque le client Teredo envoie son paquet initial à un serveur Teredo, le port UDP source du paquet est mappé par le NAT à un port UDP externe différent. Le client Teredo gère ce mappage de port afin qu’il reste dans la table de traduction de l’interface NAT. Par conséquent, tout le trafic Teredo de l’hôte utilise le même port UDP mappé externe. Le port UDP externe est déterminé par le serveur Teredo à partir du port UDP source du paquet initial entrant envoyé par le client Teredo et renvoyé au client Teredo.

    Le port externe est masqué par XORing le port externe avec la fonction 0xFFFF. Par exemple, la version masquée du port externe 5000 au format hexadécimal est EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). Le masquage du port externe empêche les NAT de traduire le port externe dans la charge utile des paquets qu’ils transfèrent.

-   **Adresse externe masquée**

    Les 32 derniers bits stockent une version masquée de l’adresse IPv4 externe correspondant à tout le trafic Teredo pour ce client Teredo. Tout comme le port externe, lorsque le client Teredo envoie son paquet initial à un serveur Teredo, l’adresse IP source du paquet est mappée par le NAT à une autre adresse externe (publique). Le client Teredo gère ce mappage d’adresses afin qu’il reste dans la table de traduction de l’interface NAT. Par conséquent, tout le trafic Teredo de l’hôte utilise la même adresse IPv4 publique externe et mappée. L’adresse IPv4 externe est déterminée par le serveur Teredo à partir de l’adresse IPv4 source du paquet initial entrant envoyé par le client Teredo et renvoyée au client Teredo.

    L’adresse externe est masquée par XORing l’adresse externe avec 0xFFFFFFFF. Par exemple, la version masquée de l’adresse IPv4 publique 131.107.0.1 au format hexadécimal à deux-points est 7C94 : FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). Le masquage de l’adresse externe empêche les traducteurs d’adresses utilisateur de traduire l’adresse externe dans la charge utile des paquets qu’ils transfèrent.

 

 




