---
title: Sécurité RPC sur HTTP
description: RPC sur HTTP offre trois types de sécurité en plus de la sécurité RPC standard, ce qui entraîne la protection du trafic RPC sur HTTP une seule fois par RPC, puis la protection par le mécanisme de tunneling fourni par RPC sur HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527cf5ff74120c41606d83a248e355a6ea46d9d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413581"
---
# <a name="rpc-over-http-security"></a>Sécurité RPC sur HTTP

RPC sur HTTP offre trois types de sécurité en plus de la sécurité RPC standard, ce qui entraîne la protection du trafic RPC sur HTTP une seule fois par RPC, puis la protection par le mécanisme de tunneling fourni par RPC sur HTTP. Pour obtenir une description des mécanismes de sécurité RPC standard, consultez [sécurité](security.md). Le mécanisme de tunneling RPC sur HTTP s’ajoute à la sécurité RPC normale de la manière suivante :

-   Fournit la sécurité via IIS (disponible pour RPC sur HTTP v2 uniquement).
-   Fournit le chiffrement SSL et la vérification du proxy RPC (authentification mutuelle). Également disponible dans RPC sur HTTP v2 uniquement.
-   Fournit des restrictions sur le niveau de proxy RPC qui dicte les ordinateurs sur le réseau serveur autorisés à recevoir des appels RPC sur HTTP.

Chacune de ces trois fonctionnalités de sécurité est décrite plus en détail dans les sections suivantes.

## <a name="iis-authentication"></a>Authentification IIS

RPC sur HTTP peut tirer parti du mécanisme d’authentification normal d’IIS. Le répertoire virtuel pour le proxy RPC peut être configuré à l’aide du nœud RPC sous le site Web par défaut dans le composant logiciel enfichable MMC IIS :

![Capture d’écran montrant le nœud RPC sous le site Web par défaut dans le composant logiciel enfichable MMC IIS.](images/rpc-http-1.png)

IIS peut être configuré pour désactiver l’accès anonyme et exiger l’authentification du répertoire virtuel pour le proxy RPC. Pour ce faire, cliquez avec le bouton droit sur le nœud RPC et sélectionnez **Propriétés**. Sélectionnez l’onglet **sécurité de répertoire** , puis cliquez sur le bouton **modifier** dans le groupe **authentification et Access Control** , comme illustré ici :

![Capture d’écran montrant la boîte de dialogue Propriétés RPC.](images/rpc-http-2.png)

Bien que vous puissiez utiliser RPC sur HTTP même lorsque le répertoire virtuel RPC proxy autorise l’accès anonyme, Microsoft recommande vivement de désactiver l’accès anonyme à ce répertoire virtuel pour des raisons de sécurité. au lieu de cela, pour RPC sur HTTP, activez l’authentification de base, Windows l’authentification intégrée ou les deux. n’oubliez pas que seul RPC sur HTTP v2 est en mesure de s’authentifier auprès du Proxy rpc nécessitant une authentification de base ou intégrée Windows. RPC sur HTTP v1 ne sera pas en mesure de se connecter si **l’interdiction de l’accès anonyme** est désactivée. étant donné que RPC sur HTTP v2 est l’implémentation la plus sûre et la plus robuste, l’utilisation d’une version de Windows qui la prend en charge améliore la sécurité de vos installations.

> [!Note]  
> Par défaut, le répertoire virtuel du proxy RPC est marqué pour autoriser l’accès anonyme. Toutefois, le proxy RPC pour RPC sur HTTP v2 rejette les requêtes qui ne sont pas authentifiées par défaut.

 

## <a name="traffic-encryption"></a>Chiffrement du trafic

RPC sur HTTP peut chiffrer le trafic entre le client RPC sur HTTP et le proxy RPC avec SSL. Le trafic entre le proxy RPC et le serveur RPC sur HTTP est chiffré à l’aide de mécanismes de sécurité RPC normaux et n’utilise pas SSL (même si SSL entre le client et le proxy RPC est choisi). Cela est dû au fait que cette partie du trafic transite au sein du réseau d’une organisation et derrière un pare-feu.

Le trafic entre le client RPC sur HTTP et le proxy RPC, qui transite généralement via Internet, peut être chiffré avec SSL en plus du mécanisme de chiffrement choisi pour RPC. Dans ce cas, le trafic sur la partie Internet de l’itinéraire est doublement chiffré. Le chiffrement du trafic via le proxy RPC fournit une défense secondaire, si le proxy RPC ou d’autres ordinateurs du réseau de périmètre sont compromis. Étant donné que le proxy RPC ne peut pas déchiffrer la couche de chiffrement secondaire, le proxy RPC n’a pas accès aux données envoyées. pour plus d’informations, consultez [Recommandations de déploiement de RPC sur HTTP](rpc-over-http-deployment-recommendations.md) . Le chiffrement SSL est disponible uniquement avec RPC sur HTTP v2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Restriction des appels RPC sur HTTP à certains ordinateurs

La configuration de la sécurité IIS est basée sur les plages de ports et les ordinateurs autorisés. La possibilité d’utiliser RPC sur HTTP est contrôlée par deux entrées de Registre sur l’ordinateur exécutant IIS et le proxy RPC. La première entrée est un indicateur qui active la fonctionnalité de proxy RPC. La seconde est une liste facultative d’ordinateurs sur lesquels le proxy peut transférer les appels RPC.

Par défaut, un client qui contacte le proxy RPC pour tunnel RPC sur les appels HTTP ne peut pas accéder aux processus du serveur RPC, à l’exception des processus du serveur RPC sur HTTP qui s’exécutent sur le même ordinateur que le proxy RPC. Si l’indicateur activé n’est pas défini ou est défini sur une valeur zéro, IIS désactive le proxy RPC. Si l’indicateur activé est défini et défini sur une valeur différente de zéro, un client peut se connecter aux serveurs RPC sur HTTP sur l’ordinateur exécutant IIS. Pour permettre au client d’effectuer un tunnel vers un processus serveur RPC sur un autre ordinateur, vous devez ajouter une entrée de Registre à la liste des serveurs RPC sur HTTP de l’ordinateur IIS.

Les serveurs RPC ne peuvent pas accepter RPC sur les appels HTTP à moins qu’ils n’aient spécifiquement demandé à l’écoute RPC sur HTTP.

L’exemple suivant montre comment configurer le registre pour permettre aux clients de se connecter à des serveurs via Internet :

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

L’entrée **ValidPorts** est une \_ entrée reg SZ contenant la liste des ordinateurs auxquels le proxy RPC IIS est autorisé à transférer les appels RPC, ainsi que les ports qu’il doit utiliser pour se connecter aux serveurs RPC. L' \_ entrée reg SZ prend la forme suivante : Rosco : 593 ; Rosco : 2000-8000 ; données \* : 4000-8000.

Dans cet exemple, IIS peut transférer RPC sur les appels HTTP vers le serveur « Rosco » sur les ports 593 et 2000 à 8000. Il peut également envoyer des appels à n’importe quel serveur dont le nom commence par « Data ». Il se connecte sur les ports 4000 à 8000. En outre, avant de transférer le trafic vers un port donné sur le serveur RPC sur HTTP, le proxy RPC effectue un échange de paquets spécial avec le service RPC qui écoute sur ce port afin de vérifier qu’il est disposé à accepter les demandes sur HTTP.

Pour obtenir un exemple basé sur ces exemples de paramètres, si un service RPC écoute le port 4500 sur le serveur « données1 », mais n’a pas appelé l’une des fonctions [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) avec _ * ncacn \_ http * *, il rejette la requête. Ce comportement offre une protection supplémentaire pour les serveurs qui écoutent sur un port ouvert en raison d’une erreur de configuration. à moins que le serveur n’ait spécifiquement demandé à écouter sur le protocole RPC sur HTTP, il ne recevra pas les appels provenant de l’extérieur du pare-feu.

Les entrées de la clé **ValidPorts** doivent correspondre exactement au serveur RPC sur http demandé par le client (il ne respecte pas la casse). Pour simplifier le traitement, le proxy RPC n’effectue pas la canonisation du nom fourni par le client RPC sur HTTP. Par conséquent, si le client demande rosco.microsoft.com et que dans **ValidPorts** contient Rosco uniquement, le proxy RPC ne correspondra pas aux noms, même si les deux noms peuvent faire référence au même ordinateur. En outre, si l’adresse IP de Rosco est 66.77.88.99, et que le client demande 66.77.88.99, mais que la clé **ValidPorts** contient Rosco uniquement, le proxy RPC refuse la connexion. Si un client peut demander le serveur RPC sur HTTP par son nom ou par une adresse IP, insérez-le dans la clé **ValidPorts** .

> [!Note]  
> Bien que RPC soit activé pour IPv6, le proxy RPC ne prend pas en charge les adresses IPv6 dans la clé **ValidPorts** . Si IPv6 est utilisé pour connecter le proxy RPC et le serveur RPC sur HTTP, seuls les noms DNS peuvent être utilisés.

 

IIS lit les entrées de Registre **Enabled** et **ValidPorts** au démarrage. En outre, RPC sur HTTP relit le contenu de la clé **ValidPorts** environ toutes les 5 minutes. Si l’entrée **ValidPorts** est modifiée, les modifications sont implémentées dans un délai de 5 minutes.

**RPC sur http v1 :** Le service WEB doit être arrêté et redémarré à l’aide d’Internet Service Manager pour connaître les nouvelles valeurs des entrées de Registre à implémenter.

 

 




