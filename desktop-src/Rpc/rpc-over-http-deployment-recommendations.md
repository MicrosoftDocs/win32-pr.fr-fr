---
title: Recommandations de déploiement RPC sur HTTP
description: Cette section décrit les meilleures pratiques et les configurations de déploiement recommandées pour obtenir une sécurité et des performances maximales lors de l’utilisation de RPC sur HTTP.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf05808b90c4c0809341a846c4f5aa9684fec27fb26425342ec7e25fa98076b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018399"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Recommandations de déploiement RPC sur HTTP

Cette section décrit les meilleures pratiques et les configurations de déploiement recommandées pour obtenir une sécurité et des performances maximales lors de l’utilisation de RPC sur HTTP. Les différentes configurations mentionnées ici s’appliquent à différentes organisations en fonction de la taille, du budget et des exigences de sécurité. Chaque configuration fournit également des considérations de déploiement utiles pour déterminer celle qui convient le mieux à un scénario donné.

Pour plus d’informations sur les scénarios RPC sur HTTP volumineux, consultez [équilibrage de charge Microsoft RPC](rpc-load-balancing.md).

Les recommandations suivantes s’appliquent à toutes les configurations :

-   utilisez des versions de Windows qui prennent en charge RPC sur HTTP v2.
-   Mettez les services Internet (IIS) sur l’ordinateur qui exécute le proxy RPC en mode IIS 6,0.
-   Interdire l’accès anonyme au répertoire virtuel du proxy RPC.
-   N’activez jamais la clé de Registre AllowAnonymous.
-   Faites de votre RPC sur les clients HTTP à l’aide de **CertificateSubjectField** (pour plus d’informations, consultez [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) ) pour vérifier que le proxy RPC auquel vous vous êtes connecté est le proxy RPC attendu.
-   Configurez la clé de Registre **ValidPorts** pour qu’elle contienne uniquement les ordinateurs auxquels les clients RPC sur http se connecteront.
-   N’utilisez pas de caractères génériques dans la clé **ValidPorts** ; Cela permet de gagner du temps, mais un ordinateur complètement inattendu peut également s’adapter au caractère générique.
-   Utilisez SSL sur les clients RPC sur HTTP. Si les instructions énoncées dans ces sections sont suivies, le client RPC sur HTTP ne pourra pas se connecter sans utiliser SSL.
-   Configurez RPC sur des clients HTTP pour utiliser le chiffrement RPC en plus de l’utilisation de SSL. Si le client RPC sur HTTP ne peut pas accéder au KDC, il peut utiliser uniquement Negotiate et NTLM.
-   Configurez les ordinateurs clients pour qu’ils utilisent NTLMv2. Définissez la clé de Registre **LmCompatibilityLevel** sur 2 ou une version ultérieure. Pour plus d’informations sur la clé **LmCompatibilityLevel** , consultez **msdn.Microsoft.com** .
-   Exécutez une batterie de serveurs Web de machines proxy RPC avec la configuration décrite ci-dessus.
-   Déployez un pare-feu entre Internet et le proxy RPC.
-   Pour des performances optimales, configurez IIS pour envoyer une réponse rapide pour les codes d’erreur sans succès. Étant donné que le consommateur de la réponse IIS est un processus automatisé, il n’est pas nécessaire que des explications conviviales soient envoyées au client. elles seront simplement ignorées par le client RPC sur HTTP.

Les objectifs de base du proxy RPC du point de vue de la sécurité, des performances et de la facilité de gestion sont les suivants :

-   Fournissez un point unique d’entrée pour le trafic RPC sur HTTP dans le réseau serveur. Le fait de disposer d’un point unique d’entrée pour le trafic RPC sur HTTP dans un réseau serveur présente deux avantages principaux. Tout d’abord, puisque le proxy RPC est dirigé vers Internet, la plupart des organisations isolent ces machines dans un réseau spécial appelé réseau de périmètre non approuvé, qui est distinct du réseau d’entreprise normal. Les serveurs d’un réseau de périmètre non approuvé sont soigneusement gérés, configurés et surveillés pour résister aux attaques provenant d’Internet. Moins il y a de machines dans un réseau de périmètre non approuvé, plus il est facile de configurer, gérer, surveiller et maintenir la sécurité. Deuxièmement, étant donné qu’une batterie de serveurs Web unique avec proxys RPC installés peut traiter un nombre quelconque de serveurs RPC sur le réseau d’entreprise, il est logique de séparer le proxy RPC du serveur RPC sur HTTP et de faire en sorte que le proxy RPC réside dans un réseau de périmètre non approuvé. Si le proxy RPC se trouvait sur le même ordinateur que le serveur RPC sur HTTP, les organisations seraient obligées de placer tous leurs serveurs de back end dans un réseau de périmètre non approuvé, ce qui complique grandement la sécurité du réseau de périmètre non approuvé. La séparation du rôle du proxy RPC et du serveur RPC sur HTTP permet aux organisations de maintenir la gestion du nombre d’ordinateurs dans un réseau de périmètre non approuvé, et donc d’en assurer la sécurité.
-   Servir de fusible de sécurité pour le réseau serveur. Le proxy RPC est conçu comme un fusible à la une pour le réseau serveur : en cas de problème sur le proxy RPC, il vient simplement de sortir et protège donc le serveur RPC réel sur HTTP. Si les meilleures pratiques décrites dans cette section ont été suivies jusqu’à présent, le trafic RPC sur HTTP est chiffré avec le chiffrement RPC en plus de SSL. Le chiffrement RPC est présent entre le client et le serveur, et non entre le client et le proxy. Cela signifie que le proxy ne comprend pas et ne peut pas déchiffrer le trafic RPC qu’il reçoit. Il comprend uniquement certaines séquences de contrôle qui lui sont envoyées par le client qui gère l’établissement de la connexion, le contrôle de Flow et d’autres détails de tunneling. Il n’a pas accès aux données que le client RPC sur HTTP envoie au serveur. En outre, le client RPC sur HTTP doit s’authentifier indépendamment auprès du proxy RPC et du serveur RPC sur HTTP. Cela fournit une défense en profondeur. Si l’ordinateur proxy RPC est compromis, en raison d’une erreur de configuration ou d’une violation de la sécurité d’un certain type, les données qui transitent par ce dernier sont toujours sécurisées contre toute falsification. Une personne malveillante qui peut prendre le contrôle du proxy RPC peut au plus interrompre le trafic, mais ne la lit pas ou la falsifie. C’est là que le rôle fusible du proxy RPC entre en lecture, ce qui est plus extensible sans la sécurité du trafic RPC sur HTTP compromis.
-   Distribuez une partie des vérifications d’accès et du déchiffrement entre plusieurs ordinateurs exécutant le proxy RPC dans une batterie de serveurs Web. En fonctionnant correctement dans une batterie de serveurs Web, le proxy RPC permet aux organisations de décharger le déchiffrement SSL et certaines des vérifications d’accès, ce qui libère plus de capacité sur le serveur back end à traiter. L’utilisation d’une batterie de serveurs Web de machines proxy RPC permet également à une organisation d’accroître sa capacité à résister à des attaques par déni de service (DoS) en augmentant la capacité sur ses serveurs frontaux.

Dans les conditions énoncées jusqu’à présent, les organisations ont encore des choix. Chaque organisation a des choix et des compromis entre les désagréments des utilisateurs, la sécurité et les coûts :

-   **utiliser l’authentification de base ou Windows l’authentification intégrée pour l’authentification auprès du Proxy RPC ?** RPC sur HTTP prend actuellement en charge uniquement NTLM : il ne prend pas en charge Kerberos. De même, s’il existe un proxy HTTP ou un pare-feu entre le client RPC sur HTTP et le proxy RPC qui insère le pragma *via* dans l’en-tête http, l’authentification NTLM ne fonctionnera pas. Si ce n’est pas le cas, les organisations peuvent choisir entre l’authentification de base et l’authentification NTLM. L’avantage de l’authentification de base est qu’elle est plus rapide et plus simple et, par conséquent, offre moins de possibilités pour les attaques par déni de service. Mais NTLM est plus sécurisé. En fonction des priorités d’une organisation, il peut choisir de base, NTLM ou permettre à ses utilisateurs de choisir entre les deux. Si un seul est choisi, il est préférable de désactiver l’autre dans le répertoire virtuel RPC proxy pour réduire les risques d’attaques.
-   **Utiliser le même jeu d’informations d’identification pour le proxy RPC et le serveur RPC sur HTTP, ou utiliser des informations d’identification différentes pour chacun ?** Le compromis pour cette décision est entre la commodité de l’utilisateur et la sécurité. Peu d’utilisateurs aiment entrer plusieurs informations d’identification. Toutefois, si une violation de sécurité se produit dans un réseau de périmètre non approuvé, le fait d’avoir des jeux d’informations d’identification distincts pour le proxy RPC et le serveur RPC sur HTTP fournit une protection supplémentaire. Notez que si des informations d’identification distinctes sont utilisées, et qu’un ensemble d’informations d’identification est celui des informations d’identification de domaine de l’utilisateur, il est recommandé d’utiliser les informations d’identification de domaine de l’utilisateur pour le serveur RPC sur HTTP et non pour le proxy RPC.

 

 




