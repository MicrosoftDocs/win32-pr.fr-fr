---
description: Décrit les fonctionnalités de l’MSVM \_ ComputerSystem associé.
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Classe Msvm_VirtualSystemCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201254"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="b47e6-103">MSVM \_ VirtualSystemCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="b47e6-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="b47e6-104">Décrit les fonctionnalités de l' [**MSVM \_ ComputerSystem**](msvm-computersystem.md)associé.</span><span class="sxs-lookup"><span data-stu-id="b47e6-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="b47e6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b47e6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47e6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b47e6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="b47e6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b47e6-107">Members</span></span>

<span data-ttu-id="b47e6-108">La classe **MSVM \_ VirtualSystemCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b47e6-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b47e6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b47e6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b47e6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b47e6-110">Properties</span></span>

<span data-ttu-id="b47e6-111">La classe **MSVM \_ VirtualSystemCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b47e6-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b47e6-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b47e6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b47e6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b47e6-115">A short description of the object.</span></span> <span data-ttu-id="b47e6-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b47e6-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="b47e6-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b47e6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="b47e6-120">A description of the object.</span></span> <span data-ttu-id="b47e6-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b47e6-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b47e6-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b47e6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b47e6-125">A display name for the object.</span></span> <span data-ttu-id="b47e6-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b47e6-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-127">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="b47e6-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b47e6-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-130">Indique si la propriété **ElementName** peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="b47e6-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="b47e6-131">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b47e6-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-132">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="b47e6-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b47e6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-135">Spécifie les restrictions sur **ElementName**, exprimées sous la forme d’une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="b47e6-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="b47e6-136">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b47e6-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b47e6-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b47e6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-140">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b47e6-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-141">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b47e6-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b47e6-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b47e6-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-143">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="b47e6-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-144">Type de données : **unit16**</span><span class="sxs-lookup"><span data-stu-id="b47e6-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-146">Qualificateurs : **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="b47e6-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-147">Spécifie la longueur maximale prise en charge de la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="b47e6-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="b47e6-148">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b47e6-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b47e6-149">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="b47e6-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47e6-150">Type de données : tableau **unit16**</span><span class="sxs-lookup"><span data-stu-id="b47e6-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="b47e6-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b47e6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b47e6-152">Indique les États possibles qui peuvent être demandés lors de l’utilisation de la méthode **RequestStateChange** sur l’élément logique activé.</span><span class="sxs-lookup"><span data-stu-id="b47e6-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="b47e6-153">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b47e6-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="b47e6-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="b47e6-154">Value</span></span>                                                                         | <span data-ttu-id="b47e6-155">Signification</span><span class="sxs-lookup"><span data-stu-id="b47e6-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="b47e6-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="b47e6-157">activé</span><span class="sxs-lookup"><span data-stu-id="b47e6-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="b47e6-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="b47e6-159">Désactive</span><span class="sxs-lookup"><span data-stu-id="b47e6-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="b47e6-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="b47e6-161">Éteindre</span><span class="sxs-lookup"><span data-stu-id="b47e6-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="b47e6-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="b47e6-163">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="b47e6-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="b47e6-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="b47e6-165">Test</span><span class="sxs-lookup"><span data-stu-id="b47e6-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="b47e6-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="b47e6-167">Fenêtres</span><span class="sxs-lookup"><span data-stu-id="b47e6-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="b47e6-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="b47e6-169">Mettre en suspens</span><span class="sxs-lookup"><span data-stu-id="b47e6-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="b47e6-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="b47e6-171">Reboot</span><span class="sxs-lookup"><span data-stu-id="b47e6-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="b47e6-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="b47e6-173">Réinitialiser</span><span class="sxs-lookup"><span data-stu-id="b47e6-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b47e6-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b47e6-174">Requirements</span></span>



| <span data-ttu-id="b47e6-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b47e6-175">Requirement</span></span> | <span data-ttu-id="b47e6-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="b47e6-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47e6-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b47e6-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b47e6-178">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b47e6-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b47e6-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b47e6-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b47e6-180">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b47e6-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b47e6-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b47e6-181">Namespace</span></span><br/>                | <span data-ttu-id="b47e6-182">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b47e6-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b47e6-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b47e6-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b47e6-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b47e6-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b47e6-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b47e6-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b47e6-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

