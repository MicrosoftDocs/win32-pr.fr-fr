---
description: Les qualificateurs contiennent des informations de contexte spécifiques à l’implémentation et des propriétés de transport qui définissent la façon dont le fournisseur SNMP accède à un agent SNMP. La liste suivante répertorie les qualificateurs propres au fournisseur SNMP.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Qualificateurs spécifiques au fournisseur SNMP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753676"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Qualificateurs spécifiques au fournisseur SNMP

Les qualificateurs contiennent des informations de contexte spécifiques à l’implémentation et des propriétés de transport qui définissent la façon dont le fournisseur SNMP accède à un agent SNMP. La liste suivante répertorie les qualificateurs propres au fournisseur SNMP.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Type de données **: \_ chaîne CIM**

Adresse de transport associée à l’agent SNMP, telle qu’une adresse IP ou un nom DNS. Vous devez définir **AgentAddress** sur une adresse d’hôte de monodiffusion valide ou un nom d’hôte de domaine qui peut être résolu par le biais du processus de résolution de noms de domaine du système d’exploitation. **AgentAddress** n’a pas de valeur par défaut.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Type de données : **CIM \_ SINT32**

Nombre maximal de demandes SNMP en suspens qui peuvent être envoyées à cet agent alors qu’aucune réponse n’a encore été reçue. Une requête SNMP est considérée comme en suspens jusqu’à ce qu’une réponse PDU soit reçue ou qu’elle ait expiré. Une grande taille de fenêtre améliore généralement les performances, mais certains agents peuvent ne pas fonctionner correctement sous une charge importante. **AgentFlowControlWindowSize** peut avoir la valeur 0 pour indiquer une taille de fenêtre infinie ou un entier compris entre 1 et 2 ^ 32-1. La valeur par défaut est 10. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Type de données **: \_ chaîne CIM**

Chaîne d’octet de longueur variable qui est utilisée par l’agent SNMP pour authentifier une unité de données de protocole SNMP (PDU) lors d’une opération de lecture (obtenir/obtenir les requêtes suivantes SNMP). Le nom de la Communauté doit être mappé à une chaîne Unicode et est limité à des caractères alphanumériques. La valeur par défaut est public. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Type de données : **CIM \_ SINT32**

Nombre de tentatives d’une demande SNMP unique en l’absence de réponse de l’agent SNMP avant que la demande ne soit considérée comme ayant échoué. **AgentRetryCount** doit être défini sur un entier compris entre 0 et 2 ^ 32-1. La valeur par défaut est 1. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Type de données : **CIM \_ SINT32**

Durée en millisecondes avant que l’unité de données de protocole SNMP (PDU) soit considérée comme supprimée. Il s’agit du nombre de millisecondes d’attente d’une réponse à une demande SNMP envoyée à l’agent SNMP. **AgentRetryTimeout** doit être défini sur un entier compris entre 0 et 2 ^ 32-1. La valeur par défaut est 500. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Type de données **: \_ chaîne CIM**

Version du protocole SNMP à utiliser lors de la communication avec l’agent SNMP. Actuellement, les seules valeurs valides sont 1 (pour SNMPv1) et 2C (pour SNMPv2C). La valeur par défaut est 1. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Type de données **: \_ chaîne CIM**

Protocole de transport utilisé pour communiquer avec l’agent SNMP. Actuellement, les seules valeurs valides sont les adresses IP (Internet Protocol) et IPX (Internet Packet Exchange). La valeur par défaut est IP. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Type de données : **CIM \_ SINT32**

Nombre maximal de liaisons de variables contenues dans un seul PDU SNMP. Chaque requête SNMP envoyée à l’agent SNMP contient une ou plusieurs variables SNMP. Ce paramètre spécifie le plus grand nombre de variables qui peuvent être incluses dans une demande unique. **AgentVarBindsPerPdu** peut avoir la valeur 0 (zéro) pour que l’implémentation détermine les liaisons de variables optimales ou un entier compris entre 1 et 2 ^ 32-1. Notez que même si l’augmentation de cette valeur peut améliorer les performances, certains agents et réseaux ne peuvent pas traiter la requête résultante. La valeur par défaut est 10. Ce qualificateur est facultatif.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Type de données **: \_ chaîne CIM**

Chaîne d’octet de longueur variable qui est utilisée par l’agent SNMP pour authentifier une unité de données de protocole SNMP lors d’une opération d’écriture (requête de définition SNMP). Le nom de la Communauté doit être mappé à une chaîne Unicode et est limité à des caractères alphanumériques. La valeur par défaut est public. Ce qualificateur est facultatif.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

 




