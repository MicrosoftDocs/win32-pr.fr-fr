---
description: Représente une propriété d’appareil PnP de type Sint16.
ms.assetid: AD329F31-1E31-4C9D-B6BE-C4FF2364F534
ms.tgt_platform: multiple
title: Classe Win32_PnPDevicePropertySint16
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertySint16
- Win32_PnPDevicePropertySint16.Key
- Win32_PnPDevicePropertySint16.KeyName
- Win32_PnPDevicePropertySint16.Type
- Win32_PnPDevicePropertySint16.DeviceID
- Win32_PnPDevicePropertySint16.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cdaa510dfa8bccdc87f68083a6c64a3c3e0675f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111582"
---
# <a name="win32_pnpdevicepropertysint16-class"></a><span data-ttu-id="7a035-103">\_Classe PnPDevicePropertySint16 Win32</span><span class="sxs-lookup"><span data-stu-id="7a035-103">Win32\_PnPDevicePropertySint16 class</span></span>

<span data-ttu-id="7a035-104">Représente une propriété d’appareil PnP de type **Sint16**.</span><span class="sxs-lookup"><span data-stu-id="7a035-104">Represents a PnP device property of type **Sint16**.</span></span>

<span data-ttu-id="7a035-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7a035-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a035-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a035-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertySint16 : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  Sint16 Data;
};
```

## <a name="members"></a><span data-ttu-id="7a035-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7a035-107">Members</span></span>

<span data-ttu-id="7a035-108">La classe **Win32 \_ PnPDevicePropertySint16** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a035-108">The **Win32\_PnPDevicePropertySint16** class has these types of members:</span></span>

-   [<span data-ttu-id="7a035-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a035-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a035-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a035-110">Properties</span></span>

<span data-ttu-id="7a035-111">La classe **Win32 \_ PnPDevicePropertySint16** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7a035-111">The **Win32\_PnPDevicePropertySint16** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a035-112">**Données**</span><span class="sxs-lookup"><span data-stu-id="7a035-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a035-113">Type de données : **Sint16**</span><span class="sxs-lookup"><span data-stu-id="7a035-113">Data type: **Sint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a035-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a035-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a035-115">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7a035-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="7a035-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7a035-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a035-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7a035-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a035-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a035-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a035-119">Identifie l’appareil PnP.</span><span class="sxs-lookup"><span data-stu-id="7a035-119">Identifies the PnP device.</span></span>

<span data-ttu-id="7a035-120">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7a035-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a035-121">**Clé**</span><span class="sxs-lookup"><span data-stu-id="7a035-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a035-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7a035-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a035-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a035-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a035-124">Valeur de la paire clé Name-Value qui identifie la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="7a035-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="7a035-125">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7a035-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a035-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="7a035-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a035-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7a035-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a035-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a035-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a035-129">Nom de la paire de clés Name-Value qui identifie la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="7a035-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="7a035-130">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7a035-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a035-131">**Type**</span><span class="sxs-lookup"><span data-stu-id="7a035-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a035-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a035-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a035-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a035-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a035-134">Type de la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="7a035-134">The type of the **Data** property.</span></span>

<span data-ttu-id="7a035-135">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7a035-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="7a035-136">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="7a035-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="7a035-137">**Vide** (0)</span><span class="sxs-lookup"><span data-stu-id="7a035-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="7a035-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="7a035-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="7a035-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="7a035-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="7a035-140">**Octet** (3)</span><span class="sxs-lookup"><span data-stu-id="7a035-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="7a035-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="7a035-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="7a035-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="7a035-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="7a035-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="7a035-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="7a035-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="7a035-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="7a035-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="7a035-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="7a035-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="7a035-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="7a035-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="7a035-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="7a035-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="7a035-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="7a035-149">**Décimal** (12)</span><span class="sxs-lookup"><span data-stu-id="7a035-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="7a035-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="7a035-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="7a035-151">**Devise** (14)</span><span class="sxs-lookup"><span data-stu-id="7a035-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="7a035-152">**Date** (15)</span><span class="sxs-lookup"><span data-stu-id="7a035-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="7a035-153">**FileTime** (16)</span><span class="sxs-lookup"><span data-stu-id="7a035-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="7a035-154">**Booléen** (17)</span><span class="sxs-lookup"><span data-stu-id="7a035-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="7a035-155">**Chaîne** (18)</span><span class="sxs-lookup"><span data-stu-id="7a035-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="7a035-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="7a035-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="7a035-157">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="7a035-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="7a035-158">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="7a035-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="7a035-159">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="7a035-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7a035-160">**Erreur** (23)</span><span class="sxs-lookup"><span data-stu-id="7a035-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="7a035-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="7a035-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="7a035-162">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="7a035-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="7a035-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7a035-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="7a035-164">26 – 4097</span><span class="sxs-lookup"><span data-stu-id="7a035-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="7a035-165">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="7a035-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="7a035-166">**Binaire** (4099)</span><span class="sxs-lookup"><span data-stu-id="7a035-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="7a035-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="7a035-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="7a035-168">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="7a035-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="7a035-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="7a035-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="7a035-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="7a035-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="7a035-171">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="7a035-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="7a035-172">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="7a035-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="7a035-173">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="7a035-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="7a035-174">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="7a035-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="7a035-175">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="7a035-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="7a035-176">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="7a035-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="7a035-177">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="7a035-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="7a035-178">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="7a035-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="7a035-179">**StringList** (4112)</span><span class="sxs-lookup"><span data-stu-id="7a035-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="7a035-180">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="7a035-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="7a035-181">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="7a035-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="7a035-182">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="7a035-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="7a035-183">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="7a035-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="7a035-184">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="7a035-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="7a035-185">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="7a035-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="7a035-186">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="7a035-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="7a035-187">**Inconnu-Vérifiez dans devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="7a035-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="7a035-188">**TBD** (8217)</span><span class="sxs-lookup"><span data-stu-id="7a035-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="7a035-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7a035-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="7a035-190">8218 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="7a035-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a035-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a035-191">Requirements</span></span>



| <span data-ttu-id="7a035-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a035-192">Requirement</span></span> | <span data-ttu-id="7a035-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a035-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a035-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a035-194">Minimum supported client</span></span><br/> | <span data-ttu-id="7a035-195">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a035-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7a035-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a035-196">Minimum supported server</span></span><br/> | <span data-ttu-id="7a035-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7a035-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="7a035-198">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7a035-198">Namespace</span></span><br/>                | <span data-ttu-id="7a035-199">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7a035-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a035-200">MOF</span><span class="sxs-lookup"><span data-stu-id="7a035-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a035-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a035-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a035-202">DLL</span><span class="sxs-lookup"><span data-stu-id="7a035-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a035-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a035-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a035-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a035-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a035-205">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="7a035-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7a035-206">**\_PnPDeviceProperty Win32**</span><span class="sxs-lookup"><span data-stu-id="7a035-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="7a035-207">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="7a035-207">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




