---
title: attribut de point de terminaison
description: L’attribut \ Endpoint \ spécifie un ou des ports connus (points de terminaison de communication) sur lesquels les serveurs de l’interface écoutent les appels.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- MIDL, attribut de point de terminaison
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea4951a407f09c1407c6e897938460d780e0429e888210e7e1ade392b5e94af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383179"
---
# <a name="endpoint-attribute"></a>attribut de point de terminaison

L’attribut **\[ point de terminaison \]** spécifie un ou des ports bien connus (points de terminaison de communication) sur lesquels les serveurs de l’interface écoutent les appels.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Protocole-séquence* 
</dt> <dd>

Spécifie une chaîne de caractères qui représente une combinaison valide d’un protocole RPC (tel que « ncacn »), un protocole de transport (tel que « TCP ») et un protocole réseau (tel que « IP »). Pour obtenir la liste des séquences de protocole valides, consultez [constantes de séquence de protocole](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*port de point de terminaison* 
</dt> <dd>

Spécifie une chaîne qui représente la désignation du point de terminaison pour la famille de protocoles spécifiée. La syntaxe de la chaîne de port est spécifique à chaque séquence de protocole.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’attribut **\[ point de terminaison \]** spécifie une famille de transport telle que le protocole orienté connexion TCP/IP, un protocole orienté connexion NetBIOS ou le protocole orienté connexion de canal nommé. L’utilisation de l’attribut de **\[ point de terminaison \]** est cohérente avec d’autres méthodes pour ajouter un point de terminaison, et ne fournit pas de services supplémentaires ou spéciaux pour le point de terminaison ; il fournit simplement un raccourci pour appeler l’API.

> [!Note]  
> Spécification d’un point de terminaison dans le. La définition de l’interface IDL ne restreint pas l’accès à l’interface au point de terminaison spécifié. Ajout d’un point de terminaison à. La définition de l’interface IDL permet à l’interface d’être appelée par n’importe quel point de terminaison de ce processus, et permet d’utiliser le point de terminaison pour appeler d’autres interfaces dans ce processus.

 

La valeur de *séquence de protocole* détermine les valeurs valides pour le port de *point de terminaison*. Le compilateur MIDL vérifie uniquement la syntaxe générale de l’entrée *Endpoint-port* . Les erreurs de spécification de port sont signalées par les bibliothèques Runtime. Pour plus d’informations sur les valeurs autorisées pour chaque séquence de protocole, consultez les [constantes de séquence de protocole](/windows/desktop/Rpc/protocol-sequence-constants).

Les séquences de protocole suivantes spécifiées par DCE ne sont pas prises en charge par le compilateur MIDL fourni avec Microsoft RPC : **ncacn \_ OSI \_ DNA** et **ncadg \_ DDS**.

Veillez à bien citer les barres obliques inverses dans les points de terminaison. Cette erreur se produit généralement lorsque le point de terminaison est un canal nommé.

Les informations de point de terminaison spécifiées dans le fichier IDL sont utilisées par les fonctions d’exécution RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) et [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).

## <a name="examples"></a>Exemples

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 