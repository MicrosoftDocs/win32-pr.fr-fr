---
description: La \_ classe système CIM agrège un ensemble énumérable d’éléments système gérés.
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: CIM_System, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950691"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="3372d-103">CIM_System, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3372d-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3372d-104">La **classe \_ système CIM** agrège un ensemble énumérable d’éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3372d-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="3372d-105">L’agrégation fonctionne comme un ensemble fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="3372d-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="3372d-106">Dans une sous-classe particulière du système, il existe une liste bien définie de classes d’éléments système gérés dont les instances doivent être agrégées.</span><span class="sxs-lookup"><span data-stu-id="3372d-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="3372d-107">L' **objet \_ système CIM** et ses dérivés sont des objets de niveau supérieur de CIM.</span><span class="sxs-lookup"><span data-stu-id="3372d-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="3372d-108">Ils fournissent l’étendue de nombreux composants et doivent avoir des clés système uniques.</span><span class="sxs-lookup"><span data-stu-id="3372d-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3372d-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3372d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3372d-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3372d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3372d-111">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3372d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3372d-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3372d-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3372d-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3372d-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="3372d-114">Membres</span><span class="sxs-lookup"><span data-stu-id="3372d-114">Members</span></span>

<span data-ttu-id="3372d-115">La **classe \_ système CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3372d-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="3372d-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3372d-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3372d-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3372d-117">Properties</span></span>

<span data-ttu-id="3372d-118">La **classe \_ système CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3372d-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3372d-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3372d-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="3372d-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3372d-123">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3372d-123">A short textual description of the object.</span></span>

<span data-ttu-id="3372d-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3372d-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3372d-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-128">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3372d-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3372d-129">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="3372d-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3372d-130">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="3372d-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="3372d-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="3372d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-134">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3372d-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3372d-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3372d-135">A textual description of the object.</span></span>

<span data-ttu-id="3372d-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3372d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3372d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3372d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="3372d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3372d-141">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="3372d-141">Indicates when the object was installed.</span></span> <span data-ttu-id="3372d-142">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="3372d-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3372d-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3372d-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3372d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-147">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3372d-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3372d-148">Définit l’étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="3372d-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="3372d-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="3372d-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3372d-152">Identifie la manière dont le nom du système a été généré, à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="3372d-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="3372d-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="3372d-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3372d-156">Comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="3372d-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="3372d-157">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="3372d-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-160">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3372d-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3372d-161">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="3372d-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="3372d-162">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="3372d-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-163">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3372d-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3372d-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3372d-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3372d-165">Rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="3372d-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="3372d-166">Les sous-classes du système peuvent remplacer cette propriété pour définir des valeurs de rôle explicites.</span><span class="sxs-lookup"><span data-stu-id="3372d-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="3372d-167">Un groupe de travail peut également décrire les heuristiques, les conventions et les instructions pour la spécification des rôles.</span><span class="sxs-lookup"><span data-stu-id="3372d-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="3372d-168">Par exemple, pour une instance d’un système de mise en réseau, cette propriété peut contenir la chaîne « Switch » ou « Bridge ».</span><span class="sxs-lookup"><span data-stu-id="3372d-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="3372d-169">**État**</span><span class="sxs-lookup"><span data-stu-id="3372d-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3372d-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3372d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3372d-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3372d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3372d-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3372d-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3372d-173">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3372d-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="3372d-174">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="3372d-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3372d-175">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="3372d-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3372d-176">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="3372d-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3372d-177">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="3372d-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3372d-178">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="3372d-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3372d-179">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="3372d-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3372d-180">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3372d-181">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3372d-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3372d-182">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="3372d-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3372d-183">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="3372d-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3372d-184">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="3372d-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3372d-185">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="3372d-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3372d-186">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="3372d-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3372d-187">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="3372d-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3372d-188">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="3372d-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3372d-189">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="3372d-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3372d-190">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="3372d-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3372d-191">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="3372d-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3372d-192">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="3372d-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3372d-193">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="3372d-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="3372d-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3372d-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3372d-195">Notes</span><span class="sxs-lookup"><span data-stu-id="3372d-195">Remarks</span></span>

<span data-ttu-id="3372d-196">La **classe \_ système CIM** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="3372d-197">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="3372d-197">WMI does not implement this class.</span></span> <span data-ttu-id="3372d-198">Pour les classes WMI dérivées du **\_ système CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3372d-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3372d-199">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3372d-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3372d-200">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3372d-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3372d-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3372d-201">Requirements</span></span>



| <span data-ttu-id="3372d-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3372d-202">Requirement</span></span> | <span data-ttu-id="3372d-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="3372d-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3372d-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3372d-204">Minimum supported client</span></span><br/> | <span data-ttu-id="3372d-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3372d-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3372d-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3372d-206">Minimum supported server</span></span><br/> | <span data-ttu-id="3372d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3372d-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3372d-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3372d-208">Namespace</span></span><br/>                | <span data-ttu-id="3372d-209">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3372d-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3372d-210">MOF</span><span class="sxs-lookup"><span data-stu-id="3372d-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3372d-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3372d-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3372d-212">DLL</span><span class="sxs-lookup"><span data-stu-id="3372d-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3372d-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3372d-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3372d-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3372d-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3372d-215">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3372d-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

