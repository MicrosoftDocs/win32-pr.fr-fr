---
description: La \_ classe CIM BootService représente la fonctionnalité fournie par un périphérique ou un logiciel, ou par un réseau, pour charger un système d’exploitation sur un système informatique unitaire.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: Classe CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514939"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="be7d7-103">\_Classe CIM BootService</span><span class="sxs-lookup"><span data-stu-id="be7d7-103">CIM\_BootService class</span></span>

<span data-ttu-id="be7d7-104">La classe **CIM \_ BootService** représente la fonctionnalité fournie par un périphérique ou un logiciel, ou par un réseau, pour charger un système d’exploitation sur un système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="be7d7-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be7d7-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="be7d7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be7d7-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be7d7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be7d7-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be7d7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="be7d7-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="be7d7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7d7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be7d7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="be7d7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="be7d7-110">Members</span></span>

<span data-ttu-id="be7d7-111">La classe **CIM \_ BootService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be7d7-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="be7d7-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="be7d7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="be7d7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be7d7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be7d7-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="be7d7-114">Methods</span></span>

<span data-ttu-id="be7d7-115">La classe **CIM \_ BootService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="be7d7-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="be7d7-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="be7d7-116">Method</span></span>                                                               | <span data-ttu-id="be7d7-117">Description</span><span class="sxs-lookup"><span data-stu-id="be7d7-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="be7d7-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="be7d7-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="be7d7-119">Met le service dans l’état Démarré.</span><span class="sxs-lookup"><span data-stu-id="be7d7-119">Puts the service in the started state.</span></span> <span data-ttu-id="be7d7-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="be7d7-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="be7d7-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="be7d7-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="be7d7-122">Met le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="be7d7-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="be7d7-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="be7d7-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="be7d7-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be7d7-124">Properties</span></span>

<span data-ttu-id="be7d7-125">La classe **CIM \_ BootService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="be7d7-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be7d7-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="be7d7-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-130">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be7d7-130">A short textual description of the object.</span></span>

<span data-ttu-id="be7d7-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be7d7-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-135">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="be7d7-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-136">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="be7d7-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="be7d7-137">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="be7d7-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="be7d7-138">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="be7d7-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-142">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="be7d7-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-143">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be7d7-143">A textual description of the object.</span></span>

<span data-ttu-id="be7d7-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be7d7-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be7d7-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="be7d7-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-149">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="be7d7-149">Indicates when the object was installed.</span></span> <span data-ttu-id="be7d7-150">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="be7d7-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="be7d7-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="be7d7-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be7d7-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-156">La propriété Name identifie de façon unique le service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="be7d7-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="be7d7-157">Cette fonctionnalité est décrite plus en détail dans la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be7d7-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="be7d7-158">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-159">**Cours**</span><span class="sxs-lookup"><span data-stu-id="be7d7-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-160">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be7d7-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-162">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="be7d7-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-163">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="be7d7-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="be7d7-164">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="be7d7-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-168">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-169">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="be7d7-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="be7d7-170">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="be7d7-171">**Automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="be7d7-172">**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be7d7-173">**État**</span><span class="sxs-lookup"><span data-stu-id="be7d7-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-176">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="be7d7-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-177">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be7d7-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="be7d7-178">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="be7d7-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="be7d7-179">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="be7d7-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="be7d7-180">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="be7d7-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="be7d7-181">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="be7d7-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="be7d7-182">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="be7d7-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="be7d7-183">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="be7d7-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="be7d7-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="be7d7-185">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="be7d7-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="be7d7-186">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="be7d7-187">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="be7d7-188">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="be7d7-189">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="be7d7-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="be7d7-190">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="be7d7-191">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="be7d7-192">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="be7d7-193">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="be7d7-194">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="be7d7-195">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="be7d7-196">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="be7d7-197">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="be7d7-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be7d7-198">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be7d7-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-201">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="be7d7-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-202">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="be7d7-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="be7d7-203">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="be7d7-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="be7d7-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7d7-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be7d7-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be7d7-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7d7-207">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="be7d7-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="be7d7-208">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="be7d7-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="be7d7-209">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be7d7-210">Notes</span><span class="sxs-lookup"><span data-stu-id="be7d7-210">Remarks</span></span>

<span data-ttu-id="be7d7-211">La classe **CIM \_ BootService** est dérivée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="be7d7-212">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="be7d7-212">WMI does not implement this class.</span></span>

<span data-ttu-id="be7d7-213">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="be7d7-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be7d7-214">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="be7d7-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7d7-215">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be7d7-215">Requirements</span></span>



| <span data-ttu-id="be7d7-216">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be7d7-216">Requirement</span></span> | <span data-ttu-id="be7d7-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="be7d7-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be7d7-218">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be7d7-218">Minimum supported client</span></span><br/> | <span data-ttu-id="be7d7-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be7d7-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be7d7-220">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be7d7-220">Minimum supported server</span></span><br/> | <span data-ttu-id="be7d7-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be7d7-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be7d7-222">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be7d7-222">Namespace</span></span><br/>                | <span data-ttu-id="be7d7-223">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="be7d7-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be7d7-224">MOF</span><span class="sxs-lookup"><span data-stu-id="be7d7-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be7d7-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be7d7-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be7d7-226">DLL</span><span class="sxs-lookup"><span data-stu-id="be7d7-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7d7-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7d7-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7d7-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be7d7-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7d7-229">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="be7d7-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

