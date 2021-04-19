---
description: Définit le moyen par lequel un client peut découvrir la plage valide de paramètres par défaut pour une fonctionnalité de commutateur Ethernet.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Classe Msvm_EthernetSwitchFeatureCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525763"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="63250-103">MSVM \_ EthernetSwitchFeatureCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="63250-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="63250-104">Définit le moyen par lequel un client peut découvrir la plage valide de paramètres par défaut pour une fonctionnalité de commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="63250-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="63250-105">Un objet **MSVM \_ EthernetSwitchFeatureCapabilities** est associé à chaque commutateur Ethernet virtuel, pour chaque fonctionnalité prise en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="63250-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="63250-106">Quatre [**objets \_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md) sont associés à l' **objet \_ MSVM EthernetSwitchFeatureCapabilities** pour décrire les valeurs minimale, maximale, par défaut et incrémentielle pour les fonctionnalités de fonctionnalité du commutateur donné.</span><span class="sxs-lookup"><span data-stu-id="63250-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="63250-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="63250-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63250-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63250-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="63250-109">Membres</span><span class="sxs-lookup"><span data-stu-id="63250-109">Members</span></span>

<span data-ttu-id="63250-110">La classe **MSVM \_ EthernetSwitchFeatureCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63250-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="63250-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63250-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63250-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63250-112">Properties</span></span>

<span data-ttu-id="63250-113">La classe **MSVM \_ EthernetSwitchFeatureCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="63250-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63250-114">**Applicabilité**</span><span class="sxs-lookup"><span data-stu-id="63250-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-115">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63250-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63250-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63250-117">Indique si cette fonctionnalité est appliquée à un commutateur Ethernet ou à un port commuté Ethernet particulier.</span><span class="sxs-lookup"><span data-stu-id="63250-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63250-118">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="63250-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="63250-119">**Port** (1)</span><span class="sxs-lookup"><span data-stu-id="63250-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="63250-120">**Commutateur** (2)</span><span class="sxs-lookup"><span data-stu-id="63250-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63250-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63250-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63250-124">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="63250-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="63250-125">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63250-125">A short description of the object.</span></span> <span data-ttu-id="63250-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63250-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63250-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="63250-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63250-130">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="63250-130">A description of the object.</span></span> <span data-ttu-id="63250-131">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63250-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63250-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="63250-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63250-135">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63250-135">A display name for the object.</span></span> <span data-ttu-id="63250-136">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63250-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63250-137">**FeatureId**</span><span class="sxs-lookup"><span data-stu-id="63250-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63250-140">Identificateur de la fonctionnalité pour laquelle cet objet fournit des informations sur les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="63250-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="63250-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63250-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63250-144">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="63250-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="63250-145">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="63250-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="63250-146">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63250-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63250-147">**Version**</span><span class="sxs-lookup"><span data-stu-id="63250-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63250-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63250-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63250-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63250-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63250-150">Version de la fonctionnalité dans un format « major. minor », par exemple « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="63250-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63250-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63250-151">Requirements</span></span>



| <span data-ttu-id="63250-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63250-152">Requirement</span></span> | <span data-ttu-id="63250-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="63250-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63250-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63250-154">Minimum supported client</span></span><br/> | <span data-ttu-id="63250-155">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63250-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="63250-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63250-156">Minimum supported server</span></span><br/> | <span data-ttu-id="63250-157">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63250-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63250-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63250-158">Namespace</span></span><br/>                | <span data-ttu-id="63250-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="63250-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="63250-160">MOF</span><span class="sxs-lookup"><span data-stu-id="63250-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63250-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63250-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63250-162">DLL</span><span class="sxs-lookup"><span data-stu-id="63250-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63250-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63250-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

