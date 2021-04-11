---
title: Indicateurs d’inscription de l’interface (rpcdce. h)
description: Les constantes suivantes sont utilisées dans le paramètre flags des fonctions RpcServerRegisterIf2 et RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105700"
---
# <a name="interface-registration-flags"></a>Indicateurs d’inscription de l’interface

Les constantes suivantes sont utilisées dans le paramètre *Flags* des fonctions [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) et [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>entre</strong></dt> </dl></td>
<td style="text-align: left;">Sémantique d’interface standard.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Lorsque cet indicateur d’interface est inscrit, le runtime RPC appelle le rappel de sécurité inscrit pour tous les appels, quelle que soit l’identité, la séquence de protocole ou le niveau d’authentification du client.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1. Lorsque cet indicateur n’est pas défini, RPC filtre automatiquement tous les appels non authentifiés avant qu’ils n’atteignent le rappel de sécurité.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Lorsque cet indicateur d’interface est inscrit, le runtime RPC rejette les appels effectués par les clients distants. Tous les appels locaux à l’aide de séquences de protocole ncadg_ * et ncacn_ * sont également rejetés, à l’exception de ncacn_np. RPC autorise les appels de ncacn_NP uniquement si l’appel n’est pas fourni par SRV. Les appels de Ncalrpc sont toujours traités.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Il s’agit d’une interface d' <strong>écoute automatique</strong> . Le temps d’exécution commence à écouter les appels dès que la première interface autolistn est inscrite et cesse d’écouter lorsque la dernière interface autolistn est désinscrite.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Réservé pour OLE. N’utilisez pas cet indicateur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">Non implémenté actuellement.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Limite les connexions aux clients qui utilisent un niveau d’autorisation supérieur à RPC_C_AUTHN_LEVEL_NONE. La spécification de cet indicateur permet aux clients de traverser la session <strong>null</strong> . Sur Windows XP et Windows Server 2003, ces clients ne sont pas autorisés. Les clients qui échouent au test de RPC_IF_ALLOW_SECURE_ONLY reçoivent une erreur de RPC_S_ACCESS_DENIED. L’utilisation de l’indicateur RPC_IF_ALLOW_SECURE_ONLY n’implique pas ou ne garantit pas un niveau élevé de privilège sur la partie de l’utilisateur appelant. RPC vérifie uniquement que l’utilisateur dispose d’informations d’identification valides ; l’utilisateur appelant peut utiliser le compte invité ou d’autres comptes à faibles privilèges. N’assumez pas de privilèges élevés lorsque RPC_IF_ALLOW_SECURE_ONLY est utilisé.<br/> <strong>Windows NT 4,0 et Windows Me/98/95 :  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Désactive la mise en cache des rappels de sécurité, en forçant un rappel de sécurité pour chaque appel RPC sur une interface donnée.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





