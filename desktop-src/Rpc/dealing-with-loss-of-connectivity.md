---
title: Gestion de la perte de connectivité
description: Gestion de la perte de connectivité
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8e7a8088cfe09a4c4026c16cc3dc5ea36b3430
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009160"
---
# <a name="dealing-with-loss-of-connectivity"></a>Gestion de la perte de connectivité

Une fois qu’un appel RPC est terminé, la connexion n’est pas fermée. elle est marquée comme étant libre. Par conséquent, le serveur peut descendre ou la connectivité réseau peut être perdue pendant ou entre les appels, tandis qu’une connexion est située dans le pool. En matière de stratégie, le temps d’exécution RPC réessaye ces appels uniquement si les deux conditions suivantes sont remplies :

-   Le serveur ne peut pas exécuter l’appel ou l’appel est idempotent.
-   Le client peut implémenter les nouvelles tentatives de manière efficace.

Les paragraphes suivants développent et clarifient les deux conditions.

Un appel idempotent est un appel qui peut être exécuté plusieurs fois sur le serveur sans effets secondaires indésirables. Par exemple, un appel RPC qui interroge le solde de la Banque pour un compte donné est idempotent. Si cet appel est exécuté deux fois en raison d’une perte de connectivité, aucun dommage n’est fait. Un autre exemple d’appel idempotent est la modification de l’adresse d’un client dans une base de données. L’exécution double est correcte, car la deuxième exécution remplace simplement l’adresse déjà actuelle par la même adresse. Une opération telle que « soustraire 50 dollars du compte XYZ » n’est pas idempotent. La perte de connectivité réseau ne doit pas aboutir à plusieurs exécutions d’un tel appel.

Pour être sécurisé, le temps d’exécution RPC traite tous les appels comme non-idempotent. L' \[ \] attribut idempotent n’est pas pris en charge pour [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp)et est ignoré. Par conséquent, la première condition de la liste précédente est réduite au *serveur qui ne peut pas exécuter l’appel*.

Dans de nombreux cas, le temps d’exécution RPC ne peut pas déterminer de façon concluant que l’appel n’a pas déjà été exécuté sur le serveur. Dans ce cas, le client ne réessaiera pas d’exécuter l’appel.

Les exemples suivants illustrent le moment où la durée d’exécution RPC ne réessaye pas un appel :

-   Un serveur est redémarré.

    Un simple appel RPC non sécurisé est effectué sur une interface sur laquelle aucun appel précédent n’a été effectué après le redémarrage. Dans la mesure où aucun appel n’a été effectué sur cette interface, le temps d’exécution RPC tente d’abord de négocier l’utilisation de l’interface. Il envoie un paquet à l’aide d’une connexion dans le pool. Étant donné que le serveur a été redémarré et que la connexion n’est plus valide, une erreur est retournée. Étant donné que l’exécution RPC côté client n’a pas encore commencé à envoyer les données pour l’appel réel, le client détermine que le serveur n’a peut-être pas pu être exécuté sur ces données. Par conséquent, il ferme la connexion et recherche une autre connexion dans le pool. S’il ne trouve pas de connexion, il ouvre une nouvelle connexion et tente à nouveau de négocier l’utilisation de l’interface. Si cela se déroule correctement, l’appel est effectué (c’est-à-dire, une nouvelle tentative est effectuée, car l’échec a été détecté avant le démarrage de l’appel).

-   Un appel RPC avec la sécurité au niveau de la confidentialité (chiffrement) est établi sur une connexion avec un contexte de sécurité déjà négocié.

    Pour garantir des performances optimales, le temps d’exécution RPC chiffre le paquet marshalé en ligne (sur les données de texte en clair). Si la tentative d’envoi des données échoue, l’exécution RPC ne peut pas réessayer l’appel, car les données de texte en clair ont été remplacées par les données chiffrées et ne peuvent pas rechiffrer les données avec un nouveau contexte de sécurité. Par conséquent, aucune nouvelle tentative n’est effectuée.

-   L’envoi d’un fragment non-premier échoue.

    Aucune nouvelle tentative n’est effectuée, car le temps d’exécution RPC peut choisir d’ignorer le contenu du premier fragment une fois qu’il est terminé et n’a aucun moyen de réessayer d’envoyer le premier fragment.

-   La demande RPC est envoyée.

    Le serveur abandonne la connexion. Aucune nouvelle tentative n’est effectuée, car RPC ne peut pas déterminer si le serveur a reçu l’appel et a démarré son exécution.

Si le serveur utilise un point de terminaison dynamique, RPC ne résoudra pas le point de terminaison pendant les nouvelles tentatives. Cela signifie que si un serveur est arrêté et remis en service, il peut résider sur un point de terminaison différent, et RPC ne résoudra pas en toute transparence le point de terminaison lorsqu’un appel est retenté. Pour forcer la rérésolution du point de terminaison, le client RPC doit appeler [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) avant de réessayer un appel.

Dans la plupart des cas, si un client RPC peut déterminer si un appel est idempotent ou s’il conserve les données que RPC rejette, il peut choisir de générer un mécanisme de nouvelle tentative sur RPC.

> [!Note]  
> Si le serveur est un cluster et que les différents nœuds du cluster exécutent des versions différentes du logiciel serveur, une nouvelle tentative RPC peut débarquer l’appel sur un autre nœud du cluster en cas de basculement, et éventuellement sur une autre version du serveur. Dans de tels scénarios de déploiement, assurez-vous que le client ne s’appuie pas sur une version particulière du logiciel serveur pour exécuter un appel donné. Si c’est le cas, le client doit créer un mécanisme par-dessus RPC qui détecte et gère ces conditions.

 

 

 