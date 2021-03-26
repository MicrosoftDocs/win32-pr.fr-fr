---
description: Cette classe est la classe de type d’événement pour les événements réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Classe SystemConfig_Network
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972163"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="70bd4-104">\_Classe de réseau SystemConfig</span><span class="sxs-lookup"><span data-stu-id="70bd4-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="70bd4-105">Cette classe est la classe de type d’événement pour les événements réseau.</span><span class="sxs-lookup"><span data-stu-id="70bd4-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="70bd4-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="70bd4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="70bd4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70bd4-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="70bd4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="70bd4-108">Members</span></span>

<span data-ttu-id="70bd4-109">La classe de **\_ réseau SystemConfig** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70bd4-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="70bd4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70bd4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70bd4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70bd4-111">Properties</span></span>

<span data-ttu-id="70bd4-112">La **classe \_ réseau SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70bd4-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70bd4-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="70bd4-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70bd4-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70bd4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70bd4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-116">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="70bd4-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="70bd4-117">Taille de la table de hachage dans laquelle les blocs de contrôle TCP (TCBs) sont stockés.</span><span class="sxs-lookup"><span data-stu-id="70bd4-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="70bd4-118">Le protocole TCP stocke les blocs de contrôle dans une table de hachage afin qu’il puisse les trouver très rapidement.</span><span class="sxs-lookup"><span data-stu-id="70bd4-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="70bd4-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="70bd4-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70bd4-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70bd4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70bd4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-122">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="70bd4-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="70bd4-123">Le numéro de port le plus élevé que TCP peut attribuer lorsqu’une application demande un port utilisateur disponible à partir du système.</span><span class="sxs-lookup"><span data-stu-id="70bd4-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="70bd4-124">En règle générale, les ports éphémères (ceux utilisés brièvement) sont alloués aux numéros de port 1024 à 5000.</span><span class="sxs-lookup"><span data-stu-id="70bd4-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="70bd4-125">La valeur du numéro de port utilisateur le plus élevé que TCP peut attribuer est contrôlée par un paramètre du Registre.</span><span class="sxs-lookup"><span data-stu-id="70bd4-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="70bd4-126">Pour plus d’informations, consultez [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="70bd4-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="70bd4-127">**TcbTablePartitions**</span><span class="sxs-lookup"><span data-stu-id="70bd4-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70bd4-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70bd4-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70bd4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-130">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="70bd4-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="70bd4-131">Nombre de partitions dans la table des blocs de contrôle de transport.</span><span class="sxs-lookup"><span data-stu-id="70bd4-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="70bd4-132">Le partitionnement de la table de blocs de contrôle de transport minimise la contention pour l’accès aux tables.</span><span class="sxs-lookup"><span data-stu-id="70bd4-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="70bd4-133">Cela s’avère particulièrement utile sur les systèmes multiprocesseurs.</span><span class="sxs-lookup"><span data-stu-id="70bd4-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="70bd4-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="70bd4-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70bd4-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70bd4-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70bd4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70bd4-137">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="70bd4-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="70bd4-138">Temps qui doit s’écouler avant que TCP puisse libérer une connexion fermée et réutiliser ses ressources.</span><span class="sxs-lookup"><span data-stu-id="70bd4-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="70bd4-139">Cet intervalle entre la clôture et la mise en version est connu sous le nom d' \_ État d’attente ou d’état 2MSL.</span><span class="sxs-lookup"><span data-stu-id="70bd4-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="70bd4-140">Pendant ce temps, la connexion peut être rouverte à un coût plus faible pour le client et le serveur que lors de l’établissement d’une nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="70bd4-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="70bd4-141">La norme RFC 793 publiée par l’IETF requiert que TCP maintienne une connexion fermée pendant un intervalle au moins égale à deux fois la durée de vie maximale du segment (2MSL) du réseau.</span><span class="sxs-lookup"><span data-stu-id="70bd4-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="70bd4-142">Lorsqu’une connexion est libérée, sa paire de sockets et le bloc de contrôle TCP (TCB) peuvent être utilisés pour prendre en charge une autre connexion.</span><span class="sxs-lookup"><span data-stu-id="70bd4-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="70bd4-143">Par défaut, le langage MSL est défini sur 120 secondes, et la valeur de cette entrée est égale à 2 MSLs, soit 4 minutes.</span><span class="sxs-lookup"><span data-stu-id="70bd4-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="70bd4-144">Pour plus d’informations, consultez la [RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="70bd4-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="70bd4-145">La réduction de la valeur de cette entrée à l’aide d’un paramètre du registre permet à TCP de libérer des connexions fermées plus rapidement, ce qui fournit davantage de ressources pour les nouvelles connexions.</span><span class="sxs-lookup"><span data-stu-id="70bd4-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="70bd4-146">Toutefois, si la valeur est trop faible, TCP peut libérer des ressources de connexion avant que la connexion ne soit terminée, ce qui nécessite que le serveur utilise des ressources supplémentaires pour rétablir la connexion.</span><span class="sxs-lookup"><span data-stu-id="70bd4-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="70bd4-147">En règle générale, TCP ne libère pas les connexions fermées tant que la valeur de cette entrée n’a pas expiré.</span><span class="sxs-lookup"><span data-stu-id="70bd4-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="70bd4-148">Toutefois, TCP peut libérer des connexions avant que cette valeur n’expire s’il ne manque pas de blocs de contrôle TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="70bd4-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="70bd4-149">Le nombre de TCBs créés par le système est contrôlé par un paramètre du Registre.</span><span class="sxs-lookup"><span data-stu-id="70bd4-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="70bd4-150">Pour plus d’informations, consultez [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="70bd4-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70bd4-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="70bd4-151">Requirements</span></span>



| <span data-ttu-id="70bd4-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70bd4-152">Requirement</span></span> | <span data-ttu-id="70bd4-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="70bd4-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70bd4-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70bd4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="70bd4-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70bd4-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70bd4-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70bd4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="70bd4-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70bd4-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70bd4-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70bd4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70bd4-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="70bd4-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
