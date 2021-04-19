---
description: Utilisé dans la méthode GetSummaryInformation de la \_ classe MSVM VirtualSystemManagementService pour récupérer rapidement les informations communes relatives à un système virtuel ou à un instantané.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518132"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="eddca-103">MSVM \_ SummaryInformationBase, classe</span><span class="sxs-lookup"><span data-stu-id="eddca-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="eddca-104">Utilisé dans la méthode [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pour récupérer rapidement les informations communes relatives à un système virtuel ou à un instantané.</span><span class="sxs-lookup"><span data-stu-id="eddca-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="eddca-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eddca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddca-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eddca-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="eddca-107">Membres</span><span class="sxs-lookup"><span data-stu-id="eddca-107">Members</span></span>

<span data-ttu-id="eddca-108">La classe **MSVM \_ SummaryInformationBase** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eddca-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="eddca-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eddca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eddca-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eddca-110">Properties</span></span>

<span data-ttu-id="eddca-111">La classe **MSVM \_ SummaryInformationBase** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eddca-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eddca-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="eddca-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-113">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eddca-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-115">Heure à laquelle le système virtuel ou l’instantané a été créé.</span><span class="sxs-lookup"><span data-stu-id="eddca-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eddca-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eddca-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. ElementName")</span><span class="sxs-lookup"><span data-stu-id="eddca-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="eddca-120">Nom convivial du système virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="eddca-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="eddca-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eddca-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-124">État actuel du système virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="eddca-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-125">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="eddca-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eddca-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-128">Indique si les connexions en mode étendu sont autorisées par l’hôte et, le cas échéant, si elles sont disponibles pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eddca-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="eddca-129">**Autorisé et disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="eddca-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="eddca-130">**Non autorisé** (3)</span><span class="sxs-lookup"><span data-stu-id="eddca-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="eddca-131">**Autorisé mais non disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="eddca-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eddca-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="eddca-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eddca-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-135">État d’intégrité actuel du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-135">The current health state for the virtual system.</span></span> <span data-ttu-id="eddca-136">Cette propriété n’est pas valide pour les instances de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représentent un instantané de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-137">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="eddca-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-140">Nom de l’ordinateur hébergeant cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eddca-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eddca-144">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. InstanceId"), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eddca-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eddca-145">InstanceID est une propriété facultative qui peut être utilisée pour identifier de manière opaque et unique une instance de cette classe dans l’étendue de l’espace de noms d’instanciation.</span><span class="sxs-lookup"><span data-stu-id="eddca-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="eddca-146">Plusieurs sous-classes de cette classe peuvent substituer cette propriété pour la rendre obligatoire ou une clé.</span><span class="sxs-lookup"><span data-stu-id="eddca-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="eddca-147">Ces sous-classes peuvent également modifier les algorithmes préférés pour garantir l’unicité définie ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eddca-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="eddca-148">Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant :</span><span class="sxs-lookup"><span data-stu-id="eddca-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="eddca-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="eddca-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="eddca-150">Où <OrgID> et <LocalID> sont séparés par un signe deux-points ( :), et où <OrgID> doivent inclure un nom protégé par des droits d’auteur, une marque ou un nom unique qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="eddca-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="eddca-151">(Cette spécification est semblable à la <Schema Name> \_ <Class Name> suivante : structure des noms de classes de schéma.) En outre, pour garantir l’unicité, <OrgID> ne doit pas contenir de deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="eddca-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="eddca-152">Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre <OrgID> et <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="eddca-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="eddca-153"><LocalID> est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels).</span><span class="sxs-lookup"><span data-stu-id="eddca-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="eddca-154">Si la valeur n’est pas null et que l’algorithme « préféré » ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.</span><span class="sxs-lookup"><span data-stu-id="eddca-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="eddca-155">Si vous ne définissez pas la valeur null pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le <OrgID> défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="eddca-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-156">**Nom**</span><span class="sxs-lookup"><span data-stu-id="eddca-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-159">Nom unique du système virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="eddca-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-160">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="eddca-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-163">Remarques associées au système virtuel ou à l’instantané.</span><span class="sxs-lookup"><span data-stu-id="eddca-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="eddca-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eddca-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-167">Nombre total de processeurs virtuels alloués au système virtuel ou à la capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="eddca-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="eddca-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-169">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eddca-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eddca-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eddca-171">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="eddca-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="eddca-172">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="eddca-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-173">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="eddca-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-176">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="eddca-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="eddca-177">Cette propriété doit avoir la valeur NULL quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="eddca-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-178">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="eddca-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-179">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eddca-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eddca-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eddca-181">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="eddca-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="eddca-182">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="eddca-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-183">**Activité**</span><span class="sxs-lookup"><span data-stu-id="eddca-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-184">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eddca-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-186">Durée écoulée depuis le dernier démarrage du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="eddca-187">Cette propriété n’est pas valide pour les instances de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représentent un instantané de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-188">**Version**</span><span class="sxs-lookup"><span data-stu-id="eddca-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-191">La version du système virtuel dans un format « majeure. mineure »; par exemple, « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="eddca-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="eddca-192">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="eddca-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-193">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eddca-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eddca-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eddca-195">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="eddca-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="eddca-196">Chaînes qui répertorient les noms conviviaux des commutateurs virtuels auxquels la machine virtuelle est connectée.</span><span class="sxs-lookup"><span data-stu-id="eddca-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="eddca-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="eddca-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eddca-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eddca-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eddca-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eddca-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eddca-200">Sous-type du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eddca-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="eddca-201">**Microsoft : Hyper-v : sous-type : 1** (« Microsoft : Hyper-v : SubType : 1 »)</span><span class="sxs-lookup"><span data-stu-id="eddca-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="eddca-202">**Microsoft : Hyper-v : sous-type : 2** (« Microsoft : Hyper-v : SubType : 2 »)</span><span class="sxs-lookup"><span data-stu-id="eddca-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="eddca-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eddca-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="eddca-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eddca-204">Requirements</span></span>



| <span data-ttu-id="eddca-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eddca-205">Requirement</span></span> | <span data-ttu-id="eddca-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="eddca-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eddca-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddca-207">Minimum supported client</span></span><br/> | <span data-ttu-id="eddca-208">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eddca-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eddca-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddca-209">Minimum supported server</span></span><br/> | <span data-ttu-id="eddca-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eddca-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eddca-211">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eddca-211">Namespace</span></span><br/>                | <span data-ttu-id="eddca-212">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eddca-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eddca-213">MOF</span><span class="sxs-lookup"><span data-stu-id="eddca-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eddca-214"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eddca-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eddca-215">DLL</span><span class="sxs-lookup"><span data-stu-id="eddca-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eddca-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eddca-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eddca-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eddca-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddca-218">**\_Vue CIM**</span><span class="sxs-lookup"><span data-stu-id="eddca-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

