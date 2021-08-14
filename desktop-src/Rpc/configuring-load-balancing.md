---
title: Configuration de l’équilibrage de charge
description: Configuration de l’équilibrage de charge
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3560359bd5ad064dc270e0840845674b97b093af66796dc92f31f7a15170f467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931692"
---
# <a name="configuring-load-balancing"></a>Configuration de l’équilibrage de charge

Chaque ordinateur proxy RPC qui doit agir en tant que service d’équilibrage de charge (LBS) doit être configuré en tant que service de la même façon que les serveurs de la batterie de serveurs. Si vous le souhaitez, la ressource par défaut peut être définie et la sécurité du proxy à LBS et lbs pour les appels RPC peut être définie. Ces paramètres sont configurés par un ensemble de **clés de Registre requises** et des **clés de Registre facultatives** , comme décrit ci-dessous.

## <a name="required-registry-keys"></a>Clés de Registre requises

Plusieurs clés et valeurs de Registre sont requises pour configurer un serveur LBS. si des clés sont manquantes ou sont entrées erronées, un événement Windows est enregistré. Pour plus d’informations sur l’événement enregistré, consultez la description de chaque clé et valeur.

Pour configurer la batterie de serveurs, vous devez créer une clé de Registre **HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy** appelée **LBSConfiguration**. Sous la clé **LBSConfiguration** , une clé est créée pour chaque ressource de la batterie de serveurs. Le nom de clé est la représentation sous forme de chaîne du GUID de la ressource. Au moins une clé de ressource doit exister et cette ressource est identique à l' [**UUID**](./rpcdce/ns-rpcdce-uuid.md) défini par les clients sur le handle de liaison, [**\_ \_ handle de liaison RPC**](rpc-binding-handle.md), lors de la création de la liaison RPC/HTTP (pour plus d’informations, consultez [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). Sous chaque clé UUID de ressource, il doit exister une valeur DWORD nommée **configuration** , qui décrit la configuration utilisée. Il doit également exister un identificateur de serveur, délimité par des points-virgules, de **reg \_** , appelé **batterie**. Les serveurs identifiés dans la clé **batterie** sont les serveurs qui sont membres de la batterie de serveurs d’équilibrage de charge.

Voici une répartition détaillée des clés et des valeurs de Registre requises :

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration**

Clé de registre. La clé **LBSConfiguration** est la clé de Registre qui contient la configuration de lbs. Cela comprend les [**UUID**](./rpcdce/ns-rpcdce-uuid.md) de ressource dont la charge doit être équilibrée, le type de configuration pour chaque ressource et les serveurs dans les batteries de serveurs qui participent à l’équilibrage de charge. Si cette clé est manquante ou non valide, LBS n’est pas considéré comme étant configuré et le service LBS ne s’exécutera pas.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**

Clé de registre. La clé **UUID de ressource** identifie l’UUID de ressource dont la charge doit être équilibrée. Cet UUID de ressource est le même que l' [**UUID**](./rpcdce/ns-rpcdce-uuid.md) que les clients définissent sur le handle de liaison, [**\_ \_ handle de liaison RPC**](rpc-binding-handle.md). Il doit y avoir au moins un UUID de ressource dont la charge doit être équilibrée, il peut y avoir plusieurs UUID de ressource. Il ne peut y avoir qu’une seule batterie de serveurs et tous les points de terminaison doivent se trouver sur tous les serveurs de la batterie de serveurs. si cette clé ne peut pas être analysée avec un UUID valide, l’événement **RPCPROXY \_ EVENTLOG- \_ \_ clé non valide \_ (0xC0000006)** est enregistré dans le journal des événements Windows.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ Configuration**

DWORD. La valeur DWORD **configuration** est stockée sous la clé **UUID de ressource** . La seule valeur autorisée est 1. si cette valeur est différente de 1, le TYPE d’événement **RPCPROXY \_ EVENTLOG \_ LB \_ unknown \_ \_ (0xC0000007)** sera enregistré dans le journal des événements Windows.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ batterie**

PRIX \_ SZ La valeur de Registre **batterie** contient un point-virgule délimités liste d’identificateurs de serveur. Le format des identificateurs de serveur est le suivant :

«ServerID1, ServerPort1, LBSPort1, \[ LBSPort2,... LBSPortN \] ;»

Plusieurs identificateurs de serveur doivent être listés dans la clé de Registre **batterie** . Ils doivent être délimités par un point-virgule. Les champs qui font partie de l’identificateur de serveur sont décrits dans le tableau suivant. si ce champ ne peut pas être analysé correctement, l' **entrée de la \_ \_ configuration incorrecte de l’événement RPCPROXY EVENTLOG \_ \_ \_ (0xC0000008)** sera enregistrée dans le journal des événements Windows.



| Champ d’identificateur | Condition requise | Description                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Obligatoire    | Nom réseau pouvant être résolu pour le serveur. Il peut s’agir d’un nom DNS, d’un nom NetBIOS ou d’une adresse IP.                                                                                                                                                                                |
| ServerPort       | Facultatif    | S’il est spécifié, le port sur lequel le serveur écoute les connexions RPC/HTTP. S’il n’est pas spécifié, le mappeur de point de terminaison sur l’ordinateur serveur est utilisé pour trouver le port du serveur.                                                                                                         |
| LBSPort          | Facultatif    | S’il est spécifié, le port sur lequel le serveur écoute les lb. Pour utiliser cette clé, les interfaces LBS doivent être définies sur un point de terminaison statique à l’aide d’une commande netsh RPC Firewall. Consultez [meilleures pratiques](load-balancing-best-practices.md) relatives à l’équilibrage de charge pour obtenir des exemples de commande netsh. |



 

## <a name="optional-registry-keys"></a>Clés de Registre facultatives

Il existe trois valeurs de Registre facultatives pour configurer un serveur LBS. Les clés contrôlent principalement le niveau de sécurité pour les appels vers et depuis le service LBS, et contrôlent également l’UUID de ressource par défaut à utiliser. Les valeurs facultatives sont les suivantes :

Voici une répartition détaillée des clés et des valeurs de Registre requises :

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Lorsque la valeur DWORD **NoSecurity** n’est pas présente ou définie sur 0, les appels non sécurisés entrants au service lbs sont rejetés. Lorsqu’ils sont présents et non 0, les appels non sécurisés entrants au service LBS ne sont pas rejetés. Cette clé est lue une fois au démarrage du service LBS.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Lorsque la valeur DWORD **AssumeResourceUUID** n’est pas présente, aucune modification n’est apportée au service lbs. Lorsqu’il est présent, il doit être défini avec un [**UUID**](./rpcdce/ns-rpcdce-uuid.md)valide. Cet **UUID** sera utilisé comme UUID de ressource pour toutes les connexions qui ne spécifient pas d’UUID de ressource. Cela est couramment utilisé dans les cas où les clients ne spécifient pas d’UUID de ressource lorsqu’ils créent la liaison RPC/HTTP, mais un administrateur souhaite équilibrer la charge du trafic RPC/HTTP vers une batterie de serveurs. Si cette clé ne peut pas être analysée avec un UUID, une erreur RPC interne est introduite, générant des [**\_ \_ \_ informations d’erreur étendues RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) si elle est activée.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Lorsque la valeur DWORD **NoSecurity** n’est pas présentée ou définie sur 0, tous les appels sortants effectués à lbs services disposent de la sécurité. S’il est présent et qu’il n’est pas défini sur 0, tous les appels sortants effectués à LBS services n’ont pas de sécurité. Vérifiez que ce paramètre correspond au paramètre **HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity** .

 

 