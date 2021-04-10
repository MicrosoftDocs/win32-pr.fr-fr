---
description: Décrit les données de paramètre d’un port série virtuel.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Classe Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865513"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="82c18-103">MSVM \_ SerialPortSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="82c18-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="82c18-104">Décrit les données de paramètre d’un port série virtuel.</span><span class="sxs-lookup"><span data-stu-id="82c18-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="82c18-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="82c18-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82c18-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="82c18-107">Membres</span><span class="sxs-lookup"><span data-stu-id="82c18-107">Members</span></span>

<span data-ttu-id="82c18-108">La classe **MSVM \_ SerialPortSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="82c18-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="82c18-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="82c18-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82c18-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="82c18-110">Properties</span></span>

<span data-ttu-id="82c18-111">La classe **MSVM \_ SerialPortSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="82c18-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82c18-112">**DebuggerMode**</span><span class="sxs-lookup"><span data-stu-id="82c18-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="82c18-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="82c18-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-115">**true** si le mode du débogueur est activé sur un port série virtuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="82c18-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="82c18-116">Le mode du débogueur améliore l’utilisation d’un débogueur du noyau Microsoft Windows sur un port série virtuel.</span><span class="sxs-lookup"><span data-stu-id="82c18-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82c18-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82c18-117">Requirements</span></span>



| <span data-ttu-id="82c18-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82c18-118">Requirement</span></span> | <span data-ttu-id="82c18-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="82c18-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c18-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82c18-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82c18-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82c18-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="82c18-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82c18-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82c18-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82c18-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82c18-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82c18-124">Namespace</span></span><br/>                | <span data-ttu-id="82c18-125">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="82c18-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82c18-126">MOF</span><span class="sxs-lookup"><span data-stu-id="82c18-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82c18-127"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82c18-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82c18-128">DLL</span><span class="sxs-lookup"><span data-stu-id="82c18-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82c18-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82c18-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82c18-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82c18-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c18-131">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="82c18-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




