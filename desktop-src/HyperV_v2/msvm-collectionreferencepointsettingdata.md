---
description: Fournit des informations supplémentaires à utiliser avec la méthode CreateReferencePoint de la \_ classe CollectionReferencePointService MSVM.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114582"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="7e1fc-103">MSVM \_ CollectionReferencePointSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="7e1fc-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="7e1fc-104">Fournit des informations supplémentaires à utiliser avec la méthode [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) de la [**classe \_ CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7e1fc-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="7e1fc-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7e1fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e1fc-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="7e1fc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7e1fc-107">Members</span></span>

<span data-ttu-id="7e1fc-108">La classe **MSVM \_ CollectionReferencePointSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e1fc-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7e1fc-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e1fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e1fc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e1fc-110">Properties</span></span>

<span data-ttu-id="7e1fc-111">La classe **MSVM \_ CollectionReferencePointSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e1fc-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e1fc-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="7e1fc-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1fc-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7e1fc-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e1fc-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7e1fc-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7e1fc-115">Niveau de cohérence du point de référence.</span><span class="sxs-lookup"><span data-stu-id="7e1fc-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e1fc-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7e1fc-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="7e1fc-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)</span><span class="sxs-lookup"><span data-stu-id="7e1fc-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7e1fc-118">Le point de référence indique un point dans le temps où le système virtuel se trouvait dans un état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="7e1fc-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="7e1fc-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)</span><span class="sxs-lookup"><span data-stu-id="7e1fc-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7e1fc-120">Le point de référence indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.</span><span class="sxs-lookup"><span data-stu-id="7e1fc-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e1fc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e1fc-121">Requirements</span></span>



| <span data-ttu-id="7e1fc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e1fc-122">Requirement</span></span> | <span data-ttu-id="7e1fc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e1fc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1fc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e1fc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7e1fc-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e1fc-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7e1fc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e1fc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7e1fc-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e1fc-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e1fc-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e1fc-128">Namespace</span></span><br/>                | <span data-ttu-id="7e1fc-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e1fc-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e1fc-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7e1fc-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e1fc-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e1fc-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e1fc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7e1fc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e1fc-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e1fc-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e1fc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e1fc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1fc-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7e1fc-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




