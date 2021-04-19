---
description: Fournit des informations supplémentaires à utiliser avec la méthode CreateReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Classe Msvm_VirtualSystemReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538251"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="c30bf-103">MSVM \_ VirtualSystemReferencePointSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="c30bf-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="c30bf-104">Fournit des informations supplémentaires à utiliser avec la méthode [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) de la [**classe \_ VirtualSystemReferencePointService MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c30bf-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="c30bf-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c30bf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30bf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c30bf-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="c30bf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c30bf-107">Members</span></span>

<span data-ttu-id="c30bf-108">La classe **MSVM \_ VirtualSystemReferencePointSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c30bf-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c30bf-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c30bf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c30bf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c30bf-110">Properties</span></span>

<span data-ttu-id="c30bf-111">La classe **MSVM \_ VirtualSystemReferencePointSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c30bf-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c30bf-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="c30bf-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bf-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="c30bf-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c30bf-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c30bf-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c30bf-115">Niveau de cohérence du point de référence.</span><span class="sxs-lookup"><span data-stu-id="c30bf-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c30bf-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c30bf-116">Requirements</span></span>



| <span data-ttu-id="c30bf-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c30bf-117">Requirement</span></span> | <span data-ttu-id="c30bf-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c30bf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30bf-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c30bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c30bf-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c30bf-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c30bf-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c30bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c30bf-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c30bf-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c30bf-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c30bf-123">Namespace</span></span><br/>                | <span data-ttu-id="c30bf-124">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c30bf-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c30bf-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c30bf-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c30bf-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c30bf-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c30bf-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c30bf-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c30bf-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c30bf-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c30bf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c30bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30bf-130">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c30bf-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




