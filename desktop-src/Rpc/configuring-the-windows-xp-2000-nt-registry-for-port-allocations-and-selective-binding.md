---
title: Configuration du Registre pour les allocations de port et la liaison sélective
description: à compter de Windows 2000, vous devez utiliser un utilitaire du Kit de ressources Windows appelé Rpccfg.exe pour définir des liaisons. pour plus d’informations, consultez le Kit de ressources Windows pour la version appropriée du système d’exploitation.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Appel de procédure distante RPC, tâches, configuration du Registre pour les allocations de port et la liaison sélective
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8166e9cb4d6706e8eafb016fba309eb64a4c4910b5727bcf88c2e071a7077d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931246"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configuration du Registre pour les allocations de port et la liaison sélective

à compter de Windows 2000, vous devez utiliser un utilitaire du Kit de ressources Windows appelé Rpccfg.exe pour définir des liaisons. pour plus d’informations, consultez le Kit de ressources Windows pour la version appropriée du système d’exploitation.

pour les versions de windows antérieures à Windows 2000, les clés de registre du tableau suivant spécifient les valeurs système par défaut pour l’allocation de port dynamique et pour la liaison aux cartes réseau sur les ordinateurs multirésidents. Vous devez d’abord créer ces clés, puis spécifier les paramètres appropriés.

L’utilisation de la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) affecte ces paramètres. Les développeurs doivent être familiarisés avec les paramètres de Registre expliqués dans cette section et la fonction **RpcServerUseProtseqEx** lors de la gestion des allocations de port. Un exemple avec trois applications hypothétiques suit le tableau ci-dessous et montre comment ces paramètres et la fonction **RpcServerUseProtseqEx** interagissent.

Si une clé est manquante ou si elle contient une valeur non valide, la configuration entière est marquée comme non valide et tous les appels **RpcServerUseProtseq \** _ sur [_ *ncacn \_ IP \_ TCP* *](/windows/desktop/Midl/ncacn-ip-tcp) ou [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) échouent.

> [!Note]  
> Les ports alloués à un processus restent alloués jusqu’à ce que ce processus soit supprimé. Si tous les ports disponibles sont en cours d’utilisation, la fonction retourne RPC \_ S \_ \_ sur \_ ressources.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Clé de port</th>
<th>Type de données</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Spécifie un ensemble de plages de ports IP comprenant tous les ports disponibles à partir d’Internet ou tous les ports qui ne sont pas disponibles sur Internet. Chaque chaîne représente un port unique ou un ensemble de ports inclusifs (par exemple, 1000-1050, 1984). Si des entrées sont en dehors de la plage comprise entre 0 et 65535, ou si une chaîne ne peut pas être interprétée, le temps d’exécution RPC traitera la configuration entière comme non valide.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>O ou N (ne respecte pas la casse). Si Y, les ports répertoriés dans la clé ports sont tous les ports disponibles sur Internet sur cet ordinateur. Si N, les ports répertoriés dans la clé ports sont tous les ports qui ne sont pas disponibles sur Internet.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>O ou N (ne respecte pas la casse). Spécifie la stratégie par défaut du système. Si Y, les processus utilisant la valeur par défaut sont des ports affectés à partir de l’ensemble de ports disponibles sur Internet, comme défini ci-dessus. Si N, les processus utilisant la valeur par défaut seront affectés aux ports à partir de l’ensemble de ports intranet uniquement.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Répertorie les noms de toutes les cartes réseau sur lesquelles effectuer la liaison par défaut (par exemple, \Device\AMDPCN1). Si la clé n’existe pas, le serveur est lié à toutes les cartes réseau. Si la clé existe, le serveur crée une liaison avec les cartes réseau spécifiées dans la clé, à moins que le champ NICFlags ne soit défini sur RPC_C_BIND_TO_ALL_NICS. Si la clé a une valeur null ( &quot; &quot; ), la configuration est marquée comme non valide et tous les appels à <strong>RpcServerUseProtseq *</strong> sur <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> ou <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> échouent.</td>
</tr>
</tbody>
</table>



 

Le tableau suivant illustre comment trois exemples d’applications sont affectés par les paramètres définis dans le tableau précédent et comment les paramètres appliqués à l’aide de la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) sont également affectés.

Dans cet exemple, trois applications hypothétiques sont prises en compte :

-   Internetapp : cette application est destinée à être exposée à Internet et a spécifié le \_ \_ \_ port Internet RPC utilisé \_ dans le membre **EndpointFlags** de la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   LocalApp : cette application n’est pas destinée à être exposée à Internet, et a spécifié le \_ \_ \_ port intranet RPC use \_ dans le membre **EndpointFlags** de la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   DefaultApp : cette application spécifie zéro dans le membre **EndpointFlags** de la structure de [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

Le tableau suivant décrit l’impact de ces paramètres sur les valeurs spécifiées dans les entrées de Registre expliquées dans le tableau précédent. Pour les considérations relatives à la mise en forme, les codes suivants sont affectés :

Assembly PIA = valeur de clé PortsInternetAvailable

UIP = valeur de clé de UseInternetPorts

La valeur de la clé ports, par souci de cet exemple, est 5000-5100 pour chaque entrée.



| Application | PIA | UIP | Résultat                                  |
|-------------|-----|-----|-----------------------------------------|
| Internetapp | O   | O   | Utilise des ports entre 5000 et 5100        |
| LocalApp    | O   | O   | Utilise un port en dehors de la plage 5000-5100 |
| DefaultApp  | O   | O   | Utilise des ports entre 5000 et 5100        |
| Internetapp | O   | N   | Utilise des ports entre 5000 et 5100        |
| LocalApp    | O   | N   | Utilise un port en dehors de la plage 5000-5100 |
| DefaultApp  | O   | N   | Utilise un port en dehors de la plage 5000-5100 |
| Internetapp | N   | O   | Utilise un port en dehors de la plage 5000-5100 |
| LocalApp    | N   | O   | Utilise des ports entre 5000 et 5100        |
| DefaultApp  | N   | O   | Utilise un port en dehors de la plage 5000-5100 |
| Internetapp | N   | N   | Utilise un port en dehors de la plage 5000-5100 |
| LocalApp    | N   | N   | Utilise des ports entre 5000 et 5100        |
| DefaultApp  | N   | N   | Utilise des ports entre 5000 et 5100        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**\_TCP IP \_ ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**\_UDP IP \_ ncadg**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 