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
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="fd16b-104">Qualificateurs spécifiques au fournisseur SNMP</span><span class="sxs-lookup"><span data-stu-id="fd16b-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="fd16b-105">Les qualificateurs contiennent des informations de contexte spécifiques à l’implémentation et des propriétés de transport qui définissent la façon dont le fournisseur SNMP accède à un agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="fd16b-106">La liste suivante répertorie les qualificateurs propres au fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="fd16b-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="fd16b-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-108">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="fd16b-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="fd16b-109">Adresse de transport associée à l’agent SNMP, telle qu’une adresse IP ou un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="fd16b-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="fd16b-110">Vous devez définir **AgentAddress** sur une adresse d’hôte de monodiffusion valide ou un nom d’hôte de domaine qui peut être résolu par le biais du processus de résolution de noms de domaine du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fd16b-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="fd16b-111">**AgentAddress** n’a pas de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd16b-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span><span class="sxs-lookup"><span data-stu-id="fd16b-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-113">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="fd16b-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="fd16b-114">Nombre maximal de demandes SNMP en suspens qui peuvent être envoyées à cet agent alors qu’aucune réponse n’a encore été reçue.</span><span class="sxs-lookup"><span data-stu-id="fd16b-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="fd16b-115">Une requête SNMP est considérée comme en suspens jusqu’à ce qu’une réponse PDU soit reçue ou qu’elle ait expiré. Une grande taille de fenêtre améliore généralement les performances, mais certains agents peuvent ne pas fonctionner correctement sous une charge importante.</span><span class="sxs-lookup"><span data-stu-id="fd16b-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="fd16b-116">**AgentFlowControlWindowSize** peut avoir la valeur 0 pour indiquer une taille de fenêtre infinie ou un entier compris entre 1 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="fd16b-117">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="fd16b-117">The default value is 10.</span></span> <span data-ttu-id="fd16b-118">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span><span class="sxs-lookup"><span data-stu-id="fd16b-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-120">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="fd16b-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="fd16b-121">Chaîne d’octet de longueur variable qui est utilisée par l’agent SNMP pour authentifier une unité de données de protocole SNMP (PDU) lors d’une opération de lecture (obtenir/obtenir les requêtes suivantes SNMP).</span><span class="sxs-lookup"><span data-stu-id="fd16b-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="fd16b-122">Le nom de la Communauté doit être mappé à une chaîne Unicode et est limité à des caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="fd16b-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="fd16b-123">La valeur par défaut est public.</span><span class="sxs-lookup"><span data-stu-id="fd16b-123">The default value is public.</span></span> <span data-ttu-id="fd16b-124">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span><span class="sxs-lookup"><span data-stu-id="fd16b-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-126">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="fd16b-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="fd16b-127">Nombre de tentatives d’une demande SNMP unique en l’absence de réponse de l’agent SNMP avant que la demande ne soit considérée comme ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="fd16b-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="fd16b-128">**AgentRetryCount** doit être défini sur un entier compris entre 0 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="fd16b-129">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-129">The default value is 1.</span></span> <span data-ttu-id="fd16b-130">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="fd16b-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-132">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="fd16b-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="fd16b-133">Durée en millisecondes avant que l’unité de données de protocole SNMP (PDU) soit considérée comme supprimée.</span><span class="sxs-lookup"><span data-stu-id="fd16b-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="fd16b-134">Il s’agit du nombre de millisecondes d’attente d’une réponse à une demande SNMP envoyée à l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="fd16b-135">**AgentRetryTimeout** doit être défini sur un entier compris entre 0 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="fd16b-136">La valeur par défaut est 500.</span><span class="sxs-lookup"><span data-stu-id="fd16b-136">The default value is 500.</span></span> <span data-ttu-id="fd16b-137">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span><span class="sxs-lookup"><span data-stu-id="fd16b-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-139">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="fd16b-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="fd16b-140">Version du protocole SNMP à utiliser lors de la communication avec l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="fd16b-141">Actuellement, les seules valeurs valides sont 1 (pour SNMPv1) et 2C (pour SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="fd16b-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="fd16b-142">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-142">The default value is 1.</span></span> <span data-ttu-id="fd16b-143">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="fd16b-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-145">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="fd16b-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="fd16b-146">Protocole de transport utilisé pour communiquer avec l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="fd16b-147">Actuellement, les seules valeurs valides sont les adresses IP (Internet Protocol) et IPX (Internet Packet Exchange).</span><span class="sxs-lookup"><span data-stu-id="fd16b-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="fd16b-148">La valeur par défaut est IP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-148">The default value is IP.</span></span> <span data-ttu-id="fd16b-149">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span><span class="sxs-lookup"><span data-stu-id="fd16b-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-151">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="fd16b-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="fd16b-152">Nombre maximal de liaisons de variables contenues dans un seul PDU SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="fd16b-153">Chaque requête SNMP envoyée à l’agent SNMP contient une ou plusieurs variables SNMP.</span><span class="sxs-lookup"><span data-stu-id="fd16b-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="fd16b-154">Ce paramètre spécifie le plus grand nombre de variables qui peuvent être incluses dans une demande unique.</span><span class="sxs-lookup"><span data-stu-id="fd16b-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="fd16b-155">**AgentVarBindsPerPdu** peut avoir la valeur 0 (zéro) pour que l’implémentation détermine les liaisons de variables optimales ou un entier compris entre 1 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fd16b-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="fd16b-156">Notez que même si l’augmentation de cette valeur peut améliorer les performances, certains agents et réseaux ne peuvent pas traiter la requête résultante.</span><span class="sxs-lookup"><span data-stu-id="fd16b-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="fd16b-157">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="fd16b-157">The default value is 10.</span></span> <span data-ttu-id="fd16b-158">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fd16b-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span><span class="sxs-lookup"><span data-stu-id="fd16b-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="fd16b-160">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="fd16b-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="fd16b-161">Chaîne d’octet de longueur variable qui est utilisée par l’agent SNMP pour authentifier une unité de données de protocole SNMP lors d’une opération d’écriture (requête de définition SNMP).</span><span class="sxs-lookup"><span data-stu-id="fd16b-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="fd16b-162">Le nom de la Communauté doit être mappé à une chaîne Unicode et est limité à des caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="fd16b-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="fd16b-163">La valeur par défaut est public.</span><span class="sxs-lookup"><span data-stu-id="fd16b-163">The default value is public.</span></span> <span data-ttu-id="fd16b-164">Ce qualificateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd16b-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd16b-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd16b-165">Requirements</span></span>



| <span data-ttu-id="fd16b-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd16b-166">Requirement</span></span> | <span data-ttu-id="fd16b-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd16b-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fd16b-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd16b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="fd16b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd16b-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fd16b-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd16b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="fd16b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd16b-171">Windows Server 2008</span></span><br/> |



 

 




