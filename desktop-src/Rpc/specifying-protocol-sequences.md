---
title: Spécification de séquences de protocole
description: Les applications serveur doivent sélectionner une ou plusieurs séquences de protocole à utiliser lors de la communication avec le client sur le réseau. Le choix des séquences de protocole dépend du réseau. Consultez interprétation des informations de liaison et sélection d’une séquence de protocole.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a700299e3d2bd98fa5fb0aaebea25e907d85afb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413509"
---
# <a name="specifying-protocol-sequences"></a>Spécification de séquences de protocole

Les applications serveur doivent sélectionner une ou plusieurs séquences de protocole à utiliser lors de la communication avec le client sur le réseau. Le choix des séquences de protocole dépend du réseau. Consultez [interprétation des informations de liaison](interpreting-binding-information.md) et [sélection d’une séquence de protocole](selecting-a-protocol-sequence.md).

Votre programme serveur peut permettre aux clients de se connecter à l’aide de n’importe quelle séquence de protocole prise en charge par le réseau. Pour ce faire, appelez [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) et transmettez RPC \_ C PROTSEQ Max admises \_ \_ \_ \_ default comme premier paramètre. Toutefois, il ne s’agit pas de l’approche recommandée. Au lieu de cela, l’utilisation de **Ncalrpc** pour les appels locaux et **ncacn \_ IP \_ TCP** ou **ncacn \_ http** pour les appels distants est généralement suffisante. Les réseaux hétérogènes sont rares et pratiquement tous les réseaux prennent en charge TCP/IP.

Si vous souhaitez que votre client limite l’allocation de port pour les points de terminaison dynamiques à une plage de ports spécifique, appelez [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) à la place. Cette fonction est spécifique à Microsoft RPC et est extrêmement utile pour les appels de procédure distante qui passent par un pare-feu. Elle utilise un paramètre supplémentaire pour passer des indicateurs de contrôle d’allocation de port à la fonction. Consultez [configuration du Registre pour les allocations de port et la liaison sélective](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

Vous pouvez spécifier des séquences de protocole et des informations de point de terminaison dans votre fichier MIDL lorsque vous développez les interfaces du serveur. Si vous le faites, votre serveur doit utiliser [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) pour inscrire toutes les séquences de protocole et les informations de point de terminaison associées fournies dans le fichier IDL. En outre, il existe une fonction [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) correspondante qui permet également au serveur de passer l’allocation de port – indicateurs de contrôle.

Si vous souhaitez configurer vos programmes client et serveur pour qu’ils communiquent avec une séquence de protocole spécifiée, l’application serveur doit appeler [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Pour obtenir la liste complète des séquences de protocole RPC Microsoft, consultez la section sur les [constantes de séquence de protocole](protocol-sequence-constants.md).

Microsoft RPC fournit également [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) pour permettre aux applications de sélectionner des séquences de protocoles spécifiques et de contrôler l’allocation de port dynamique.

En plus des protocoles orientés connexion, Microsoft RPC prend également en charge les protocoles de datagramme (sans connexion). Les protocoles orientés connexion sont recommandés. les protocoles de datagramme ont des ensembles de fonctionnalités différents de ceux des protocoles orientés connexion et ne doivent être utilisés que si un développeur de système distribué requiert une fonctionnalité disponible uniquement dans les protocoles de datagramme. Voici quelques-unes des fonctionnalités disponibles lors de l’utilisation des protocoles de datagramme :

-   Les datagrammes prennent en charge les protocoles de transport UDP et sans connexion IPX.
-   Étant donné qu’il n’est pas nécessaire d’établir et de maintenir une connexion, le protocole RPC du datagramme requiert moins de ressources.
-   Les datagrammes permettent une liaison plus rapide.
-   Comme avec RPC orienté connexion, les appels RPC de datagramme sont par défaut *nonidempotent*. Cela signifie que l’appel est garanti ne pas être exécuté plusieurs fois. Toutefois, une fonction peut être marquée en tant que idempotent dans le fichier IDL, indiquant à RPC qu’il est inoffensif d’exécuter la fonction plusieurs fois en réponse à une demande client unique. Cela permet à l’exécution de conserver un État moins faible sur le serveur. Notez qu’un appel idempotent est exécuté à nouveau uniquement dans de rares circonstances sur un réseau instable.
-   Le datagramme RPC prend en charge l’attribut IDL de [diffusion](/windows/desktop/Midl/broadcast) . La diffusion permet à un client d’envoyer des messages à plusieurs serveurs en même temps. Cela permet au client de localiser l’un des serveurs disponibles sur le réseau ou de contrôler plusieurs serveurs simultanément. Notez que la diffusion du datagramme est valide uniquement dans le lien local, et ne franchit généralement pas de routeurs. Les appels de diffusion sont implicitement idempotent. Si l’appel contient \[ **des** \] paramètres out, seule la première réponse du serveur est retournée. Une fois qu’un serveur répond, tous les RPC ultérieurs sur ce handle de liaison sont envoyés à ce serveur uniquement, y compris les appels avec l’attribut Broadcast. Pour envoyer une autre diffusion, créez un nouveau handle de liaison ou appelez [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) sur le handle existant.
-   Le datagramme RPC prend en charge l’attribut IDL [peut-être](/windows/desktop/Midl/maybe) . Cela permet au client d’envoyer un appel au serveur sans attendre une réponse ou une confirmation. L’appel ne peut pas contenir de paramètres de \[ **sortie** \] . Les appels à l’aide des appels peuvent être implicitement idempotent. **\[ \]**

 

 