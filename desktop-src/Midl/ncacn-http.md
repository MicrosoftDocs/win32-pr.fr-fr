---
title: attribut ncacn_http
description: Le \_ mot clé http ncacn identifie Microsoft Internet Information Server (IIS) comme famille de protocoles pour le point de terminaison.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7eed41849f59e497000e9ad56ae7c3166cf2d0212986fa9ba5f5ea910ed364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642210"
---
# <a name="ncacn_http-attribute"></a>\_attribut http ncacn

Le mot clé **\_ http ncacn** identifie Microsoft Internet Information Server (IIS) comme famille de protocoles pour le point de terminaison.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*\_serveur RPC* 
</dt> <dd>

Adresse Internet ou nom de l’ordinateur sur lequel s’exécute le processus du serveur RPC.

</dd> <dt>

*endpoint* 
</dt> <dd>

Port TCP/IP connu (statique) sur lequel le processus serveur RPC est à l’écoute.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’identification de Microsoft Internet Information Server (IIS) comme famille de protocole permet aux applications client et serveur de communiquer sur Internet à l’aide de Microsoft Internet Information Server (IIS) en tant que proxy. Étant donné que les appels sont acheminés via un port HTTP établi, ils peuvent traverser les pare-feu.

Toutes les applications clientes et serveur RPC peuvent prendre en charge le protocole **\_ http ncacn** tant qu’elles sont en réseau sur un serveur Internet Information Server. IIS contacte le serveur RPC et établit un socket TCP/IP, qu’il gère pour le client. IIS négocie une connexion TCP/IP avec le serveur RPC et, une fois la négociation terminée, agit comme un proxy RPC, en transférant les données entre le socket TCP/IP côté client et le socket TCP/IP côté serveur. Lorsque le proxy RPC IIS détecte une fermeture de session sur le côté client ou côté serveur, il ferme le socket restant.

L’application cliente utilise implicitement la liaison statique aux services Internet (IIS), mais le serveur peut utiliser des points de terminaison dynamiques, avec le mappeur de point de terminaison (RPCSS) du serveur qui résout le port du serveur RPC. Si IIS se trouve sur un autre ordinateur que le serveur RPC, IIS reçoit l’appel distant, contacte le service RPCSS sur l’ordinateur serveur RPC pour obtenir le point de terminaison du processus serveur, puis transfère l’appel au serveur RPC approprié.

Si Internet Explorer est installé, le transport vérifie le registre pour déterminer s’il existe une configuration pour un proxy HTTP. Si un proxy existe, le transport l’utilise.

## <a name="examples"></a>Exemples

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 