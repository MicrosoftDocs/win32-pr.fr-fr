---
description: Décrit les fonctionnalités du VirtualSystemManagementService MSVM associé \_ .
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Classe Msvm_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318093"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="e911e-103">MSVM \_ VirtualSystemManagementCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="e911e-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="e911e-104">Décrit les fonctionnalités du [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)associé.</span><span class="sxs-lookup"><span data-stu-id="e911e-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="e911e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e911e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e911e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e911e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="e911e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e911e-107">Members</span></span>

<span data-ttu-id="e911e-108">La classe **MSVM \_ VirtualSystemManagementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e911e-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e911e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e911e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e911e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e911e-110">Properties</span></span>

<span data-ttu-id="e911e-111">La classe **MSVM \_ VirtualSystemManagementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e911e-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e911e-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-113">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e911e-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e911e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e911e-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="e911e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e911e-116">Spécifie les méthodes [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) qui sont prises en charge de façon asynchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="e911e-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e911e-117">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e911e-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="e911e-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="e911e-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e911e-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="e911e-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="e911e-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="e911e-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="e911e-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="e911e-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e911e-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="e911e-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="e911e-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="e911e-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="e911e-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="e911e-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="e911e-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="e911e-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="e911e-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="e911e-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="e911e-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="e911e-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="e911e-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="e911e-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="e911e-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="e911e-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="e911e-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="e911e-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="e911e-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="e911e-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="e911e-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="e911e-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="e911e-133">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="e911e-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="e911e-134">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="e911e-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="e911e-135">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="e911e-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="e911e-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="e911e-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="e911e-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="e911e-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="e911e-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="e911e-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="e911e-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="e911e-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="e911e-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="e911e-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="e911e-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="e911e-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="e911e-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="e911e-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e911e-143">**Fournisseur réservé** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e911e-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e911e-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e911e-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e911e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-147">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e911e-147">A short description of the object.</span></span> <span data-ttu-id="e911e-148">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e911e-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e911e-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="e911e-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e911e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-152">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="e911e-152">A description of the object.</span></span> <span data-ttu-id="e911e-153">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e911e-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e911e-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e911e-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e911e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-157">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e911e-157">A display name for the object.</span></span> <span data-ttu-id="e911e-158">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e911e-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e911e-159">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-160">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e911e-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-162">Indique si la propriété **ElementName** peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="e911e-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="e911e-163">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="e911e-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e911e-164">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="e911e-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e911e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-167">Spécifie les restrictions sur **ElementName**, exprimées sous la forme d’une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="e911e-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="e911e-168">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="e911e-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e911e-169">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-170">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e911e-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e911e-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e911e-172">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. IndicationsSupported")</span><span class="sxs-lookup"><span data-stu-id="e911e-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e911e-173">Spécifie les indications prises en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="e911e-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="e911e-174">Énumération des identificateurs d’indication identifiant chaque indication qui est prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="e911e-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e911e-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="e911e-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e911e-176">L’implémentation prend en charge la notification des modifications d’état des instances du [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) représentant les ressources des systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="e911e-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e911e-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="e911e-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e911e-178">L’implémentation prend en charge la notification des modifications d’état des instances [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e911e-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e911e-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="e911e-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e911e-180">L’implémentation prend en charge la notification des modifications d’état des instances [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) représentant des systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="e911e-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e911e-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e911e-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e911e-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e911e-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e911e-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e911e-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e911e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e911e-186">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="e911e-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e911e-187">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e911e-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e911e-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e911e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e911e-189">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="e911e-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-190">Type de données : **unit16**</span><span class="sxs-lookup"><span data-stu-id="e911e-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="e911e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e911e-192">Qualificateurs : **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="e911e-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e911e-193">Spécifie la longueur maximale prise en charge de la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="e911e-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="e911e-194">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="e911e-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e911e-195">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-196">Type de données : tableau **unit16**</span><span class="sxs-lookup"><span data-stu-id="e911e-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="e911e-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-198">Indique les États possibles qui peuvent être demandés lors de l’utilisation de la méthode **RequestStateChange** sur l’élément logique activé.</span><span class="sxs-lookup"><span data-stu-id="e911e-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="e911e-199">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="e911e-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="e911e-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="e911e-200">Value</span></span>                                                                         | <span data-ttu-id="e911e-201">Signification</span><span class="sxs-lookup"><span data-stu-id="e911e-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="e911e-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="e911e-203">activé</span><span class="sxs-lookup"><span data-stu-id="e911e-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="e911e-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="e911e-205">Désactive</span><span class="sxs-lookup"><span data-stu-id="e911e-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="e911e-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="e911e-207">Éteindre</span><span class="sxs-lookup"><span data-stu-id="e911e-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="e911e-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="e911e-209">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="e911e-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="e911e-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="e911e-211">Test</span><span class="sxs-lookup"><span data-stu-id="e911e-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="e911e-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="e911e-213">Fenêtres</span><span class="sxs-lookup"><span data-stu-id="e911e-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="e911e-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="e911e-215">Mettre en suspens</span><span class="sxs-lookup"><span data-stu-id="e911e-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="e911e-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="e911e-217">Reboot</span><span class="sxs-lookup"><span data-stu-id="e911e-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="e911e-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="e911e-219">Réinitialiser</span><span class="sxs-lookup"><span data-stu-id="e911e-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="e911e-220">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-221">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e911e-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e911e-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e911e-223">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. SynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="e911e-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e911e-224">Spécifie les méthodes [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) qui sont prises en charge de façon synchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="e911e-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e911e-225">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e911e-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="e911e-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="e911e-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e911e-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="e911e-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="e911e-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="e911e-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="e911e-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="e911e-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e911e-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="e911e-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="e911e-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="e911e-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="e911e-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="e911e-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="e911e-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="e911e-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="e911e-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="e911e-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="e911e-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="e911e-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="e911e-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="e911e-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="e911e-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="e911e-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="e911e-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="e911e-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="e911e-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="e911e-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="e911e-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="e911e-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="e911e-241">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="e911e-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="e911e-242">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="e911e-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="e911e-243">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="e911e-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="e911e-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="e911e-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="e911e-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="e911e-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="e911e-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="e911e-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="e911e-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="e911e-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="e911e-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="e911e-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="e911e-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="e911e-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="e911e-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="e911e-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e911e-251">**Fournisseur réservé** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e911e-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e911e-252">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="e911e-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e911e-253">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e911e-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e911e-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e911e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e911e-255">Tableau de chaînes désignant un type de système virtuel pris en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="e911e-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="e911e-256">La valeur de chaque élément de tableau non **null** doit être conforme aux chaînes définies pour la propriété [**MSVM \_ VirtualSystemSettingData. VirtualSystemType**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e911e-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e911e-257">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e911e-257">Requirements</span></span>



| <span data-ttu-id="e911e-258">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e911e-258">Requirement</span></span> | <span data-ttu-id="e911e-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="e911e-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e911e-260">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e911e-260">Minimum supported client</span></span><br/> | <span data-ttu-id="e911e-261">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e911e-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e911e-262">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e911e-262">Minimum supported server</span></span><br/> | <span data-ttu-id="e911e-263">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e911e-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e911e-264">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e911e-264">Namespace</span></span><br/>                | <span data-ttu-id="e911e-265">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e911e-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e911e-266">MOF</span><span class="sxs-lookup"><span data-stu-id="e911e-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e911e-267"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e911e-268">DLL</span><span class="sxs-lookup"><span data-stu-id="e911e-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e911e-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e911e-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

