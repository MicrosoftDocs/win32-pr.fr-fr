---
title: Spécification des points de terminaison
description: Spécifiant des points de terminaison connus et dynamiques dans l’appel de procédure distante (RPC).
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 373fb2818dd14670f5a939aa524c81fcdb05e20b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413514"
---
# <a name="specifying-endpoints"></a>Spécification des points de terminaison

Un point de terminaison est une adresse spécifique au réseau d’un processus serveur pour les appels de procédure distante. Le nom réel du point de terminaison dépend de la séquence de protocole utilisée. Par exemple, les ports TCP, UDP et HTTP use. Les canaux nommés utilisent un nom de canal nommé. Les applications client/serveur peuvent utiliser un point de terminaison connu ou dynamique. Cette section présente les techniques que les programmes serveur utilisent pour spécifier des points de terminaison connus et dynamiques. Les informations sont présentées dans les rubriques suivantes :

-   [Spécification des points de terminaison connus](#specifying-well-known-endpoints)
-   [Spécification des points de terminaison dynamiques](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>Spécification des points de terminaison connus

Lorsque votre serveur utilise un point de terminaison connu, il peut inclure les données de point de terminaison dans le cadre de son entrée de base de données de service de noms. Si c’est le cas, le handle de liaison du client contient une adresse de serveur complète qui inclut le point de terminaison connu lorsque le client importe le handle de liaison à partir de l’entrée de serveur.

Votre programme serveur peut également spécifier des points de terminaison connus en même temps qu’il spécifie des séquences de protocole. Appelez la fonction [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) . La différence entre les deux est que la dernière fonction a un paramètre supplémentaire que votre serveur peut utiliser pour contrôler l’allocation de port dynamique.

Si votre programme serveur spécifie ses informations de point de terminaison de cette manière, il doit également appeler la fonction [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) pour inscrire le point de terminaison dans le mappage de point de terminaison. Même si le point de terminaison est toujours le même, le client peut utiliser le mappage de point de terminaison pour rechercher le serveur.

À l’instar des séquences de protocole, une application peut spécifier des informations de point de terminaison dans son fichier IDL. Dans ce cas, il doit inscrire à la fois les séquences de protocole et les points de terminaison en appelant la fonction [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) ou [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) . Dans ce cas, le client a accès aux informations de point de terminaison par le biais de la spécification d’interface dans le fichier IDL. Par conséquent, il n’est pas nécessaire d’appeler la fonction [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) .

## <a name="specifying-dynamic-endpoints"></a>Spécification des points de terminaison dynamiques

Un point de terminaison dynamique est un point de terminaison que l’ordinateur hôte du serveur affecte lorsque l’exécution du serveur commence. La plupart des applications serveur utilisent des points de terminaison dynamiques pour éviter tout conflit avec d’autres programmes sur le nombre limité de ports disponibles sur le système de l’ordinateur hôte du serveur. Toutefois, les programmes qui utilisent des canaux nommés ou la séquence de protocole [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) ont un espace de noms de point de terminaison très élevé. Ils bénéficient moins des points de terminaison dynamiques que les programmes utilisant d’autres transports.

Les programmes serveur inscrivent des points de terminaison dynamiques dans une base de données de mappage de point de terminaison. Si vous souhaitez que le serveur utilise n’importe quel point de terminaison disponible, appelez [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex), [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) ou [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex). Cela définit la bibliothèque Runtime RPC pour utiliser la totalité ou une ou plusieurs séquences de protocole valides avec des points de terminaison dynamiques. Le serveur doit ensuite appeler [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) pour obtenir un ensemble de handles de liaison valides. Le serveur passe l’ensemble de handles de liaison, ou vecteur de liaison, à la fonction [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) pour inscrire tous les points de terminaison appropriés dans le mappage de point de terminaison. Pour chaque appel que votre serveur effectue vers **RpcEpRegister**, il doit y avoir un appel correspondant à [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) pour libérer la mémoire utilisée par le vecteur de liaison.

Notez que les programmes serveur peuvent utiliser la fonction [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) au lieu de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister). Les programmes utilisent généralement **RpcEpRegisterNoReplace** quand plusieurs copies d’un programme serveur doivent s’exécuter sur un système hôte serveur.

Les fonctions [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) et [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) ajoutent les interfaces du serveur et les descripteurs de liaison à la base de données du mappeur du point de terminaison. Lorsque le client effectue un appel de procédure distante à l’aide d’un handle partiellement lié, la bibliothèque Runtime du client demande au mappeur de point de terminaison de l’ordinateur serveur le point de terminaison d’une instance de serveur compatible. La bibliothèque cliente fournit l’UUID de l’interface, la séquence de protocole et, le cas échéant, l’UUID de l’objet dans le handle de liaison du client. Le mappeur de point de terminaison recherche une entrée de base de données qui correspond aux informations du client. L’UUID de l’interface client/serveur, la version principale de l’interface et la séquence de protocole doivent correspondre exactement. En outre, la version mineure de l’interface du serveur doit être supérieure ou égale à la version mineure du client.

Si tous les tests réussissent, le mappeur de point de terminaison retourne le point de terminaison valide et la bibliothèque Runtime cliente met à jour le point de terminaison dans le handle de liaison.

Les points de terminaison dynamiques sont automatiquement purgés de la base de données du mappeur de point de terminaison lorsque le processus serveur s’arrête. Vous pouvez supprimer le point de terminaison de la base de données du mappeur de point de terminaison avant de quitter le programme serveur à l’aide de la fonction [**RpcEpUnregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) , ou vous pouvez autoriser un nettoyage automatique pour gérer la suppression du point de terminaison.

 

 