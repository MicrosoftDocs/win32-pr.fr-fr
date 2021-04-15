---
title: Classe MSAD_ReplCursor
description: Fournit des informations d’état de réplication entrante sur tous les réplicas d’un contexte d’appellation (NC) donné.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor de la classe Active Directory
- MSAD_ReplCursor de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465394"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="80976-105">MSAD \_ ReplCursor, classe</span><span class="sxs-lookup"><span data-stu-id="80976-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="80976-106">Fournit des informations d’état de réplication entrante sur tous les réplicas d’un contexte d’appellation (NC) donné.</span><span class="sxs-lookup"><span data-stu-id="80976-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="80976-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80976-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="80976-108">Membres</span><span class="sxs-lookup"><span data-stu-id="80976-108">Members</span></span>

<span data-ttu-id="80976-109">La classe **MSAD \_ ReplCursor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80976-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="80976-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80976-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80976-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80976-111">Properties</span></span>

<span data-ttu-id="80976-112">La classe **MSAD \_ ReplCursor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="80976-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80976-113">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="80976-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80976-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80976-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80976-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80976-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80976-116">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80976-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80976-117">Obtient le chemin d’accès X. 500 pour le contexte d’appellation (NC) qui contient ce curseur.</span><span class="sxs-lookup"><span data-stu-id="80976-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="80976-118">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="80976-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80976-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80976-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80976-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80976-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80976-121">Obtient le chemin d’accès X. 500 pour l’agent de système d’annuaire (DSA) qui représente le contrôleur de domaine source.</span><span class="sxs-lookup"><span data-stu-id="80976-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="80976-122">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="80976-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80976-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80976-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="80976-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80976-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80976-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80976-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80976-126">Obtient l’identificateur d’appel du serveur d’origine auquel correspond le **USNAttributeFilter** .</span><span class="sxs-lookup"><span data-stu-id="80976-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="80976-127">**TimeOfLastSuccessfulSync**</span><span class="sxs-lookup"><span data-stu-id="80976-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80976-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80976-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80976-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80976-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80976-130">Obtient l’horodateur de la dernière synchronisation de réplication réussie avec le DSA source.</span><span class="sxs-lookup"><span data-stu-id="80976-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="80976-131">Indique l’heure de la dernière modification apportée par ce contrôleur de périphérique sur le DSA source pour ce contexte de nommage.</span><span class="sxs-lookup"><span data-stu-id="80976-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="80976-132">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="80976-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80976-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80976-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80976-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80976-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80976-135">Obtient le numéro de séquence de mise à jour maximal sur lequel le serveur de destination peut indiquer qu’il a enregistré toutes les modifications apportées par le serveur donné aux numéros de séquence de mise à jour inférieurs ou égaux à ce numéro de séquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="80976-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="80976-136">Cette propriété est utilisée pour filtrer les modifications que le serveur de destination a déjà appliquées sur les serveurs sources de réplication.</span><span class="sxs-lookup"><span data-stu-id="80976-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80976-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80976-137">Requirements</span></span>



| <span data-ttu-id="80976-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80976-138">Requirement</span></span> | <span data-ttu-id="80976-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="80976-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80976-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80976-140">Minimum supported client</span></span><br/> | <span data-ttu-id="80976-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80976-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="80976-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80976-142">Minimum supported server</span></span><br/> | <span data-ttu-id="80976-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80976-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80976-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80976-144">Namespace</span></span><br/>                | <span data-ttu-id="80976-145">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="80976-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="80976-146">MOF</span><span class="sxs-lookup"><span data-stu-id="80976-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80976-147"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80976-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="80976-148">DLL</span><span class="sxs-lookup"><span data-stu-id="80976-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80976-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80976-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80976-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80976-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80976-151">**\_curseur de réplication DS \_**</span><span class="sxs-lookup"><span data-stu-id="80976-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

