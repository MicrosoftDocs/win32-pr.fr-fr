---
description: La \_ classe CIM ApplicationSystem représente une application ou un système logiciel qui prend en charge une fonction commerciale particulière qui peut être gérée comme une unité indépendante.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516790"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="922b0-103">\_Classe CIM ApplicationSystem</span><span class="sxs-lookup"><span data-stu-id="922b0-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="922b0-104">La classe **CIM \_ ApplicationSystem** représente une application ou un système logiciel qui prend en charge une fonction commerciale particulière qui peut être gérée comme une unité indépendante.</span><span class="sxs-lookup"><span data-stu-id="922b0-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="922b0-105">Un tel système peut être décomposé en ses composants fonctionnels à l’aide de la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="922b0-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="922b0-106">Les fonctionnalités logicielles d’une application ou d’un système logiciel particulier sont localisées à l’aide de l’Association [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="922b0-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="922b0-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="922b0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="922b0-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="922b0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="922b0-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="922b0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="922b0-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="922b0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="922b0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="922b0-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
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

## <a name="members"></a><span data-ttu-id="922b0-112">Membres</span><span class="sxs-lookup"><span data-stu-id="922b0-112">Members</span></span>

<span data-ttu-id="922b0-113">La classe **CIM \_ ApplicationSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="922b0-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="922b0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="922b0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="922b0-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="922b0-115">Properties</span></span>

<span data-ttu-id="922b0-116">La classe **CIM \_ ApplicationSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="922b0-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="922b0-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="922b0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="922b0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="922b0-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="922b0-121">A short textual description of the object.</span></span>

<span data-ttu-id="922b0-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="922b0-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-126">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="922b0-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="922b0-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="922b0-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="922b0-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="922b0-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="922b0-129">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="922b0-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-133">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="922b0-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="922b0-134">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="922b0-134">A textual description of the object.</span></span>

<span data-ttu-id="922b0-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="922b0-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-137">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="922b0-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="922b0-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="922b0-140">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="922b0-140">Indicates when the object was installed.</span></span> <span data-ttu-id="922b0-141">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="922b0-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="922b0-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="922b0-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="922b0-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="922b0-147">Définit l’étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="922b0-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="922b0-148">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="922b0-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="922b0-152">Identifie la manière dont le nom du système a été généré, à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="922b0-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="922b0-153">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="922b0-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="922b0-157">Comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="922b0-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="922b0-158">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-159">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="922b0-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="922b0-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="922b0-163">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="922b0-163">Name of the primary system owner.</span></span>

<span data-ttu-id="922b0-164">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-165">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="922b0-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-166">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="922b0-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="922b0-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="922b0-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="922b0-168">Rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="922b0-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="922b0-169">Les sous-classes du système peuvent remplacer cette propriété pour définir des valeurs de rôle explicites.</span><span class="sxs-lookup"><span data-stu-id="922b0-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="922b0-170">Un groupe de travail peut également décrire les heuristiques, les conventions et les instructions pour la spécification des rôles.</span><span class="sxs-lookup"><span data-stu-id="922b0-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="922b0-171">Par exemple, pour une instance d’un système de mise en réseau, cette propriété peut contenir la chaîne « Switch » ou « Bridge ».</span><span class="sxs-lookup"><span data-stu-id="922b0-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="922b0-172">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="922b0-173">**État**</span><span class="sxs-lookup"><span data-stu-id="922b0-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="922b0-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="922b0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="922b0-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="922b0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="922b0-176">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="922b0-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="922b0-177">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="922b0-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="922b0-178">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="922b0-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="922b0-179">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="922b0-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="922b0-180">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="922b0-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="922b0-181">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="922b0-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="922b0-182">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="922b0-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="922b0-183">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="922b0-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="922b0-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="922b0-185">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="922b0-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="922b0-186">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="922b0-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="922b0-187">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="922b0-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="922b0-188">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="922b0-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="922b0-189">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="922b0-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="922b0-190">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="922b0-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="922b0-191">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="922b0-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="922b0-192">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="922b0-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="922b0-193">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="922b0-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="922b0-194">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="922b0-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="922b0-195">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="922b0-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="922b0-196">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="922b0-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="922b0-197">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="922b0-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="922b0-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="922b0-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="922b0-199">Notes</span><span class="sxs-lookup"><span data-stu-id="922b0-199">Remarks</span></span>

<span data-ttu-id="922b0-200">La classe **CIM \_ ApplicationSystem** est dérivée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="922b0-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="922b0-201">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="922b0-201">WMI does not implement this class.</span></span>

<span data-ttu-id="922b0-202">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="922b0-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="922b0-203">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="922b0-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="922b0-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="922b0-204">Requirements</span></span>



| <span data-ttu-id="922b0-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="922b0-205">Requirement</span></span> | <span data-ttu-id="922b0-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="922b0-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="922b0-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="922b0-207">Minimum supported client</span></span><br/> | <span data-ttu-id="922b0-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="922b0-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="922b0-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="922b0-209">Minimum supported server</span></span><br/> | <span data-ttu-id="922b0-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="922b0-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="922b0-211">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="922b0-211">Namespace</span></span><br/>                | <span data-ttu-id="922b0-212">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="922b0-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="922b0-213">MOF</span><span class="sxs-lookup"><span data-stu-id="922b0-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="922b0-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="922b0-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="922b0-215">DLL</span><span class="sxs-lookup"><span data-stu-id="922b0-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="922b0-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="922b0-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="922b0-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="922b0-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922b0-218">**\_Système CIM**</span><span class="sxs-lookup"><span data-stu-id="922b0-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

