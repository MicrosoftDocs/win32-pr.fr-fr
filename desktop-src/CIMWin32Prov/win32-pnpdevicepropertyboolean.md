---
description: Représente une propriété d’appareil PnP de type booléen.
ms.assetid: 19681413-712C-4A09-9BEF-8CFEC5D81801
ms.tgt_platform: multiple
title: Classe Win32_PnPDevicePropertyBoolean
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertyBoolean
- Win32_PnPDevicePropertyBoolean.Key
- Win32_PnPDevicePropertyBoolean.KeyName
- Win32_PnPDevicePropertyBoolean.Type
- Win32_PnPDevicePropertyBoolean.DeviceID
- Win32_PnPDevicePropertyBoolean.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b64ea80fe1304a0991e592a582ea16db76722b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033781"
---
# <a name="win32_pnpdevicepropertyboolean-class"></a><span data-ttu-id="137d7-103">\_Classe PnPDevicePropertyBoolean Win32</span><span class="sxs-lookup"><span data-stu-id="137d7-103">Win32\_PnPDevicePropertyBoolean class</span></span>

<span data-ttu-id="137d7-104">Représente une propriété d’appareil PnP de type **booléen**.</span><span class="sxs-lookup"><span data-stu-id="137d7-104">Represents a PnP device property of type **boolean**.</span></span>

<span data-ttu-id="137d7-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="137d7-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="137d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="137d7-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertyBoolean : Win32_PnPDeviceProperty
{
  string  Key;
  string  KeyName;
  Uint32  Type;
  string  DeviceID;
  boolean Data;
};
```

## <a name="members"></a><span data-ttu-id="137d7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="137d7-107">Members</span></span>

<span data-ttu-id="137d7-108">La classe **Win32 \_ PnPDevicePropertyBoolean** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="137d7-108">The **Win32\_PnPDevicePropertyBoolean** class has these types of members:</span></span>

-   [<span data-ttu-id="137d7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="137d7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="137d7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="137d7-110">Properties</span></span>

<span data-ttu-id="137d7-111">La classe **Win32 \_ PnPDevicePropertyBoolean** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="137d7-111">The **Win32\_PnPDevicePropertyBoolean** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="137d7-112">**Données**</span><span class="sxs-lookup"><span data-stu-id="137d7-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="137d7-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="137d7-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="137d7-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="137d7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="137d7-115">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="137d7-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="137d7-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="137d7-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="137d7-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="137d7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="137d7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="137d7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="137d7-119">Identifie l’appareil PnP.</span><span class="sxs-lookup"><span data-stu-id="137d7-119">Identifies the PnP device.</span></span>

<span data-ttu-id="137d7-120">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="137d7-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="137d7-121">**Clé**</span><span class="sxs-lookup"><span data-stu-id="137d7-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="137d7-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="137d7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="137d7-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="137d7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="137d7-124">Valeur de la paire clé Name-Value qui identifie la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="137d7-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="137d7-125">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="137d7-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="137d7-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="137d7-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="137d7-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="137d7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="137d7-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="137d7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="137d7-129">Nom de la paire de clés Name-Value qui identifie la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="137d7-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="137d7-130">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="137d7-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="137d7-131">**Type**</span><span class="sxs-lookup"><span data-stu-id="137d7-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="137d7-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="137d7-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="137d7-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="137d7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="137d7-134">Type de la propriété de **données** .</span><span class="sxs-lookup"><span data-stu-id="137d7-134">The type of the **Data** property.</span></span>

<span data-ttu-id="137d7-135">Cette propriété est héritée de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="137d7-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="137d7-136">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="137d7-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="137d7-137">**Vide** (0)</span><span class="sxs-lookup"><span data-stu-id="137d7-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="137d7-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="137d7-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="137d7-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="137d7-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="137d7-140">**Octet** (3)</span><span class="sxs-lookup"><span data-stu-id="137d7-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="137d7-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="137d7-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="137d7-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="137d7-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="137d7-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="137d7-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="137d7-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="137d7-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="137d7-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="137d7-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="137d7-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="137d7-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="137d7-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="137d7-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="137d7-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="137d7-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="137d7-149">**Décimal** (12)</span><span class="sxs-lookup"><span data-stu-id="137d7-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="137d7-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="137d7-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="137d7-151">**Devise** (14)</span><span class="sxs-lookup"><span data-stu-id="137d7-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="137d7-152">**Date** (15)</span><span class="sxs-lookup"><span data-stu-id="137d7-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="137d7-153">**FileTime** (16)</span><span class="sxs-lookup"><span data-stu-id="137d7-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="137d7-154">**Booléen** (17)</span><span class="sxs-lookup"><span data-stu-id="137d7-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="137d7-155">**Chaîne** (18)</span><span class="sxs-lookup"><span data-stu-id="137d7-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="137d7-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="137d7-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="137d7-157">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="137d7-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="137d7-158">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="137d7-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="137d7-159">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="137d7-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="137d7-160">**Erreur** (23)</span><span class="sxs-lookup"><span data-stu-id="137d7-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="137d7-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="137d7-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="137d7-162">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="137d7-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="137d7-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="137d7-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="137d7-164">26 – 4097</span><span class="sxs-lookup"><span data-stu-id="137d7-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="137d7-165">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="137d7-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="137d7-166">**Binaire** (4099)</span><span class="sxs-lookup"><span data-stu-id="137d7-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="137d7-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="137d7-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="137d7-168">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="137d7-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="137d7-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="137d7-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="137d7-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="137d7-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="137d7-171">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="137d7-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="137d7-172">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="137d7-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="137d7-173">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="137d7-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="137d7-174">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="137d7-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="137d7-175">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="137d7-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="137d7-176">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="137d7-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="137d7-177">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="137d7-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="137d7-178">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="137d7-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="137d7-179">**StringList** (4112)</span><span class="sxs-lookup"><span data-stu-id="137d7-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="137d7-180">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="137d7-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="137d7-181">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="137d7-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="137d7-182">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="137d7-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="137d7-183">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="137d7-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="137d7-184">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="137d7-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="137d7-185">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="137d7-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="137d7-186">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="137d7-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="137d7-187">**Inconnu-Vérifiez dans devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="137d7-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="137d7-188">**TBD** (8217)</span><span class="sxs-lookup"><span data-stu-id="137d7-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="137d7-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="137d7-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="137d7-190">8218 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="137d7-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="137d7-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="137d7-191">Requirements</span></span>



| <span data-ttu-id="137d7-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="137d7-192">Requirement</span></span> | <span data-ttu-id="137d7-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="137d7-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="137d7-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="137d7-194">Minimum supported client</span></span><br/> | <span data-ttu-id="137d7-195">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="137d7-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="137d7-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="137d7-196">Minimum supported server</span></span><br/> | <span data-ttu-id="137d7-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="137d7-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="137d7-198">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="137d7-198">Namespace</span></span><br/>                | <span data-ttu-id="137d7-199">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="137d7-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="137d7-200">MOF</span><span class="sxs-lookup"><span data-stu-id="137d7-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="137d7-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="137d7-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="137d7-202">DLL</span><span class="sxs-lookup"><span data-stu-id="137d7-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="137d7-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="137d7-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="137d7-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="137d7-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137d7-205">**\_PnPDeviceProperty Win32**</span><span class="sxs-lookup"><span data-stu-id="137d7-205">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> </dl>

 

 




