---
description: Version concrète de la classe de \_ tâche CIM. Cette classe représente une unité de travail instanciable générique à exécuter, telle qu’un traitement ou un travail d’impression.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534366"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="de27a-104">\_Classe CIM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="de27a-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="de27a-105">Version concrète de la classe [**de \_ tâche CIM**](cim-job.md) .</span><span class="sxs-lookup"><span data-stu-id="de27a-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="de27a-106">Cette classe représente une unité de travail instanciable générique à exécuter, telle qu’un traitement ou un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="de27a-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="de27a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de27a-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="de27a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="de27a-108">Members</span></span>

<span data-ttu-id="de27a-109">La classe **CIM \_ ConcreteJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de27a-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="de27a-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de27a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="de27a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de27a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="de27a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de27a-112">Methods</span></span>

<span data-ttu-id="de27a-113">La classe **CIM \_ ConcreteJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="de27a-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="de27a-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="de27a-114">Method</span></span>                                                           | <span data-ttu-id="de27a-115">Description</span><span class="sxs-lookup"><span data-stu-id="de27a-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="de27a-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="de27a-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="de27a-117">Récupère les informations d’erreur pour l’état opérationnel d’un travail concret.</span><span class="sxs-lookup"><span data-stu-id="de27a-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="de27a-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="de27a-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="de27a-119">Demande le changement d’état spécifié à un travail concret.</span><span class="sxs-lookup"><span data-stu-id="de27a-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="de27a-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de27a-120">Properties</span></span>

<span data-ttu-id="de27a-121">La classe **CIM \_ ConcreteJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="de27a-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de27a-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de27a-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de27a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de27a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de27a-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de27a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de27a-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="de27a-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="de27a-126">Identifie de façon unique et opaque une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="de27a-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="de27a-127">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="de27a-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="de27a-128">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="de27a-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="de27a-129">Ce modèle est similaire à la structure des noms de classes de schéma.</span><span class="sxs-lookup"><span data-stu-id="de27a-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="de27a-130">En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="de27a-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="de27a-131">Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="de27a-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="de27a-132">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="de27a-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="de27a-133">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="de27a-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="de27a-134">Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="de27a-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="de27a-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="de27a-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de27a-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de27a-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de27a-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de27a-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de27a-138">L’état opérationnel du travail et la transition entre ces États.</span><span class="sxs-lookup"><span data-stu-id="de27a-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="de27a-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Nouveau** (2)</span><span class="sxs-lookup"><span data-stu-id="de27a-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-140">le travail n’a jamais été démarré.</span><span class="sxs-lookup"><span data-stu-id="de27a-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="de27a-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="de27a-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-142">Le travail passe des États « nouveau », « suspendu » ou « service » à l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="de27a-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="de27a-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (4)</span><span class="sxs-lookup"><span data-stu-id="de27a-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-144">Le travail est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="de27a-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="de27a-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (5)</span><span class="sxs-lookup"><span data-stu-id="de27a-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-146">La tâche est arrêtée, mais peut être redémarrée de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="de27a-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="de27a-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (6)</span><span class="sxs-lookup"><span data-stu-id="de27a-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-148">Le travail passe à l’état « terminé », « terminé » ou « mort ».</span><span class="sxs-lookup"><span data-stu-id="de27a-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="de27a-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (7)</span><span class="sxs-lookup"><span data-stu-id="de27a-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-150">Le travail s’est terminé normalement.</span><span class="sxs-lookup"><span data-stu-id="de27a-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="de27a-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="de27a-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-152">La tâche a été arrêtée par une demande de modification d’État « Terminate ».</span><span class="sxs-lookup"><span data-stu-id="de27a-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="de27a-153">Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés (il s’agit d’un travail spécifique) uniquement en tant que nouveau travail.</span><span class="sxs-lookup"><span data-stu-id="de27a-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="de27a-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Abattu** (9)</span><span class="sxs-lookup"><span data-stu-id="de27a-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-155">La tâche a été arrêtée par une demande de modification d’État « Kill ».</span><span class="sxs-lookup"><span data-stu-id="de27a-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="de27a-156">Les processus sous-jacents peuvent avoir été laissés s’exécuter et le nettoyage peut être nécessaire pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="de27a-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="de27a-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span><span class="sxs-lookup"><span data-stu-id="de27a-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-158">La tâche est dans un état anormal qui peut indiquer une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="de27a-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="de27a-159">L’état réel peut être affiché en dépit d’objets spécifiques à un travail.</span><span class="sxs-lookup"><span data-stu-id="de27a-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="de27a-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span><span class="sxs-lookup"><span data-stu-id="de27a-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-161">La tâche est dans un état spécifique au fournisseur qui prend en charge la détection des problèmes, ou la résolution, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="de27a-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="de27a-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Requête en attente** (12)</span><span class="sxs-lookup"><span data-stu-id="de27a-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="de27a-163">En attente de la résolution d’une requête par un client.</span><span class="sxs-lookup"><span data-stu-id="de27a-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="de27a-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="de27a-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="de27a-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="de27a-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de27a-166">**Nom**</span><span class="sxs-lookup"><span data-stu-id="de27a-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de27a-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de27a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de27a-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de27a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de27a-169">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="de27a-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="de27a-170">Nom convivial de l’instance.</span><span class="sxs-lookup"><span data-stu-id="de27a-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="de27a-171">En outre, le nom convivial peut être utilisé en tant que propriété pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="de27a-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="de27a-172">Le nom ne doit pas nécessairement être unique au sein de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="de27a-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="de27a-173">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="de27a-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de27a-174">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de27a-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de27a-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de27a-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="de27a-176">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="de27a-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="de27a-177">Indique la durée de conservation d’un travail terminé.</span><span class="sxs-lookup"><span data-stu-id="de27a-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="de27a-178">La valeur par défaut est « 00000000000500.000000:000 » (cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="de27a-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="de27a-179">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="de27a-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de27a-180">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de27a-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de27a-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de27a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de27a-182">Date ou heure de la dernière modification de l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="de27a-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="de27a-183">Si l’état de la tâche n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="de27a-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de27a-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de27a-184">Requirements</span></span>



| <span data-ttu-id="de27a-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de27a-185">Requirement</span></span> | <span data-ttu-id="de27a-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="de27a-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de27a-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de27a-187">Minimum supported client</span></span><br/> | <span data-ttu-id="de27a-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="de27a-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="de27a-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de27a-189">Minimum supported server</span></span><br/> | <span data-ttu-id="de27a-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de27a-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="de27a-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de27a-191">Namespace</span></span><br/>                | <span data-ttu-id="de27a-192">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="de27a-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="de27a-193">MOF</span><span class="sxs-lookup"><span data-stu-id="de27a-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de27a-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de27a-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de27a-195">DLL</span><span class="sxs-lookup"><span data-stu-id="de27a-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de27a-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de27a-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de27a-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de27a-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de27a-198">**\_Travail CIM**</span><span class="sxs-lookup"><span data-stu-id="de27a-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

