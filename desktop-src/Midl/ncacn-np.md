---
title: attribut ncacn_np
description: Le \_ mot clé ncacn NP identifie les canaux nommés comme famille de protocoles pour le point de terminaison.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7acf294241c1d38b2067ba54e315fc3240e5bb6eca81a6b12012f8dec457a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013757"
---
# <a name="ncacn_np-attribute"></a>\_attribut ncacn NP

Le mot clé **ncacn \_ NP** identifie les canaux nommés comme famille de protocoles pour le point de terminaison.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Facultatif. Spécifie le nom du serveur. Les barres obliques inverses sont facultatives.

</dd> <dt>

*nom du canal* 
</dt> <dd>

Spécifie un nom de canal valide. Un nom de canal valide est une chaîne contenant des identificateurs séparés par des barres obliques inverses. Le premier identificateur doit être [**pipe**](pipe.md). Chaque identificateur doit être séparé par deux barres obliques inverses.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un serveur crée une instance d’un canal nommé qui est ensuite disponible pour n’importe quel client. Lorsqu’un client tente de se connecter, l’instance existante est associée à ce client. Avant qu’un autre client puisse se connecter, le serveur doit créer une autre instance du canal nommé. Si un client tente d’établir une liaison avec le serveur avant la création de la nouvelle instance, l’appel de liaison, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), peut échouer avec le message d’erreur le \_ serveur RPC S est \_ \_ trop \_ occupé. Par conséquent, vous devez vous assurer que votre application cliente gère le cas où le serveur est trop occupé pour accepter une connexion. Le client doit réessayer automatiquement, demander à l’utilisateur un cours d’action ou échouer correctement.

La syntaxe de la chaîne de port de canal nommé, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL. Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ au \_ fournisseur DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ réseaux virtuels \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 