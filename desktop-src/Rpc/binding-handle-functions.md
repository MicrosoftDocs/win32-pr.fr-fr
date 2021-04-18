---
title: Fonctions de handle de liaison
description: Le tableau suivant contient la liste des routines runtime RPC qui fonctionnent sur des handles de liaison et spécifie le type de handle de liaison autorisé.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512432"
---
# <a name="binding-handle-functions"></a>Fonctions de handle de liaison

Le tableau suivant contient la liste des routines runtime RPC qui fonctionnent sur des handles de liaison et spécifie le type de handle de liaison autorisé.



| Routine                                                            | Argument d’entrée   | Argument de sortie |
|--------------------------------------------------------------------|------------------|-----------------|
| [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | Serveur           | Serveur          |
| [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | Serveur           | Aucun            |
| [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | Aucun             | Serveur          |
| [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | Client           | None            |
| [**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | Serveur           | Aucun            |
| [**RpcBindingInqObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | Serveur ou client | Aucun            |
| [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | Serveur           | Aucun            |
| [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | Serveur           | Aucun            |
| [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | Serveur           | Aucun            |
| [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | Serveur ou client | Aucun            |
| [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | Serveur           | Aucun            |
| [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | Serveur           | Aucun            |
| [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | Aucun             | Serveur          |
| [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | Aucun             | Serveur          |
| [**RpcNsBindingSelect**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | Serveur           | Serveur          |
| [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | Aucun             | Serveur          |



 

 

 




