---
description: La \_ classe de service CIM représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: CIM_Service, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514931"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="82971-103">CIM_Service, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="82971-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="82971-104">La classe de **\_ service CIM** représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.</span><span class="sxs-lookup"><span data-stu-id="82971-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="82971-105">Un service est un objet à usage général permettant de configurer et de gérer l’implémentation des fonctionnalités. il ne s’agit pas de la fonctionnalité elle-même.</span><span class="sxs-lookup"><span data-stu-id="82971-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82971-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="82971-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="82971-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="82971-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="82971-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="82971-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="82971-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="82971-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82971-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82971-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="82971-111">Membres</span><span class="sxs-lookup"><span data-stu-id="82971-111">Members</span></span>

<span data-ttu-id="82971-112">La classe de **\_ service CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="82971-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="82971-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="82971-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="82971-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="82971-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="82971-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="82971-115">Methods</span></span>

<span data-ttu-id="82971-116">La classe de **\_ service CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="82971-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="82971-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="82971-117">Method</span></span>                                                           | <span data-ttu-id="82971-118">Description</span><span class="sxs-lookup"><span data-stu-id="82971-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82971-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="82971-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="82971-120">Tente de mettre le service dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="82971-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="82971-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="82971-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="82971-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="82971-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="82971-123">Méthode de classe qui place le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="82971-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="82971-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="82971-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="82971-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="82971-125">Properties</span></span>

<span data-ttu-id="82971-126">La classe de **\_ service CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="82971-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82971-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="82971-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="82971-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="82971-131">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="82971-131">A short textual description of the object.</span></span>

<span data-ttu-id="82971-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82971-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82971-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="82971-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-136">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="82971-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="82971-137">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="82971-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="82971-138">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="82971-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="82971-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="82971-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-142">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="82971-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="82971-143">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="82971-143">A textual description of the object.</span></span>

<span data-ttu-id="82971-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82971-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82971-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="82971-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="82971-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="82971-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="82971-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="82971-149">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="82971-149">Indicates when the object was installed.</span></span> <span data-ttu-id="82971-150">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="82971-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="82971-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82971-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82971-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="82971-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-155">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82971-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82971-156">La propriété Name identifie de façon unique le service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="82971-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="82971-157">Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="82971-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="82971-158">**Cours**</span><span class="sxs-lookup"><span data-stu-id="82971-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-159">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="82971-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="82971-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-161">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="82971-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="82971-162">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="82971-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="82971-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="82971-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-166">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="82971-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="82971-167">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="82971-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="82971-168">**Automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="82971-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="82971-169">**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="82971-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="82971-170">**État**</span><span class="sxs-lookup"><span data-stu-id="82971-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-173">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="82971-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="82971-174">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="82971-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="82971-175">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="82971-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="82971-176">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="82971-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="82971-177">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="82971-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="82971-178">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="82971-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="82971-179">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="82971-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="82971-180">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="82971-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="82971-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82971-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="82971-182">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="82971-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="82971-183">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="82971-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="82971-184">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="82971-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="82971-185">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="82971-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="82971-186">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="82971-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="82971-187">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="82971-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="82971-188">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="82971-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="82971-189">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="82971-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="82971-190">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="82971-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="82971-191">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="82971-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="82971-192">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="82971-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="82971-193">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="82971-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="82971-194">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="82971-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="82971-195">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="82971-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-198">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="82971-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="82971-199">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="82971-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="82971-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="82971-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82971-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="82971-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82971-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="82971-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82971-203">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="82971-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="82971-204">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="82971-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82971-205">Notes</span><span class="sxs-lookup"><span data-stu-id="82971-205">Remarks</span></span>

<span data-ttu-id="82971-206">La classe de **\_ service CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="82971-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="82971-207">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="82971-207">WMI does not implement this class.</span></span> <span data-ttu-id="82971-208">Pour les classes WMI dérivées du **\_ service CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="82971-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="82971-209">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="82971-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="82971-210">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="82971-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="82971-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82971-211">Requirements</span></span>



| <span data-ttu-id="82971-212">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82971-212">Requirement</span></span> | <span data-ttu-id="82971-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="82971-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82971-214">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82971-214">Minimum supported client</span></span><br/> | <span data-ttu-id="82971-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82971-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82971-216">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82971-216">Minimum supported server</span></span><br/> | <span data-ttu-id="82971-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82971-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82971-218">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82971-218">Namespace</span></span><br/>                | <span data-ttu-id="82971-219">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="82971-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82971-220">MOF</span><span class="sxs-lookup"><span data-stu-id="82971-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82971-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82971-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82971-222">DLL</span><span class="sxs-lookup"><span data-stu-id="82971-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82971-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82971-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82971-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82971-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82971-225">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="82971-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

