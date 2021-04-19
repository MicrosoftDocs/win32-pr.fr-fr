---
description: La \_ classe WMI de l’Association NetworkAdapterSetting Win32 associe une carte réseau et ses paramètres de configuration.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515375"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="36766-103">\_Classe NetworkAdapterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="36766-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="36766-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ NetworkAdapterSetting Win32** associe une carte réseau et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="36766-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="36766-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36766-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="36766-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="36766-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36766-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36766-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="36766-108">Membres</span><span class="sxs-lookup"><span data-stu-id="36766-108">Members</span></span>

<span data-ttu-id="36766-109">La classe **Win32 \_ NetworkAdapterSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36766-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="36766-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36766-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36766-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36766-111">Properties</span></span>

<span data-ttu-id="36766-112">La classe **Win32 \_ NetworkAdapterSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="36766-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36766-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="36766-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36766-114">Type de données : carte réseau **Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="36766-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="36766-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36766-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36766-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapter")</span><span class="sxs-lookup"><span data-stu-id="36766-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="36766-117">Un [**\_ NetworkAdapter Win32**](win32-networkadapter.md) qui décrit les propriétés de la carte réseau qui utilise un paramètre de carte réseau particulier.</span><span class="sxs-lookup"><span data-stu-id="36766-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="36766-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="36766-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36766-119">Type de données : **Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="36766-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="36766-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36766-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36766-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")</span><span class="sxs-lookup"><span data-stu-id="36766-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="36766-122">[**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) qui décrit les paramètres de configuration utilisés sur la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="36766-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36766-123">Notes</span><span class="sxs-lookup"><span data-stu-id="36766-123">Remarks</span></span>

<span data-ttu-id="36766-124">La classe **Win32 \_ NetworkAdapterSetting** est dérivée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="36766-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="36766-125">Pour plus d’informations sur l’utilisation des classes d’association, consultez [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="36766-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="36766-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="36766-126">Examples</span></span>

<span data-ttu-id="36766-127">L’exemple VBScript suivant utilise **Win32 \_ NetworkAdapterSetting** pour identifier l’adresse IP sur la connexion au réseau local.</span><span class="sxs-lookup"><span data-stu-id="36766-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="36766-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36766-128">Requirements</span></span>



| <span data-ttu-id="36766-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36766-129">Requirement</span></span> | <span data-ttu-id="36766-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="36766-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36766-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36766-131">Minimum supported client</span></span><br/> | <span data-ttu-id="36766-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36766-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36766-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36766-133">Minimum supported server</span></span><br/> | <span data-ttu-id="36766-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36766-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36766-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36766-135">Namespace</span></span><br/>                | <span data-ttu-id="36766-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36766-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36766-137">MOF</span><span class="sxs-lookup"><span data-stu-id="36766-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36766-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36766-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36766-139">DLL</span><span class="sxs-lookup"><span data-stu-id="36766-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36766-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36766-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36766-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36766-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36766-142">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="36766-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="36766-143">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="36766-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="36766-144">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="36766-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
