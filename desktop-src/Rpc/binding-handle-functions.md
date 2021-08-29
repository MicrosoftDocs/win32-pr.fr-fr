---
title: Fonctions de handle de liaison
description: Le tableau suivant contient la liste des routines runtime RPC qui fonctionnent sur des handles de liaison et spécifie le type de handle de liaison autorisé.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a821396f4ab4bdd29e999d334921a933d32516c4ec23ba89c364c013535fb43d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023129"
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



 

 

 




