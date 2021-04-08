---
description: Fournit des informations supplémentaires à utiliser avec la méthode ExportReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Classe Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042948"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="98ff7-103">MSVM \_ VirtualSystemReferencePointExportSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="98ff7-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="98ff7-104">Fournit des informations supplémentaires à utiliser avec la méthode [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) de la [**classe \_ VirtualSystemReferencePointService MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="98ff7-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="98ff7-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="98ff7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ff7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98ff7-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="98ff7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="98ff7-107">Members</span></span>

<span data-ttu-id="98ff7-108">La classe **MSVM \_ VirtualSystemReferencePointExportSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98ff7-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="98ff7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98ff7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98ff7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98ff7-110">Properties</span></span>

<span data-ttu-id="98ff7-111">La classe **MSVM \_ VirtualSystemReferencePointExportSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="98ff7-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98ff7-112">**BaseReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="98ff7-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff7-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98ff7-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="98ff7-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98ff7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98ff7-115">Chemin d’accès du point de référence de base par rapport auquel l’exportation doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="98ff7-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="98ff7-116">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="98ff7-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff7-117">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="98ff7-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="98ff7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98ff7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98ff7-119">ID d’instance WMI des disques pour lesquels les données doivent être exportées.</span><span class="sxs-lookup"><span data-stu-id="98ff7-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98ff7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98ff7-120">Requirements</span></span>



| <span data-ttu-id="98ff7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98ff7-121">Requirement</span></span> | <span data-ttu-id="98ff7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="98ff7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ff7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ff7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98ff7-124">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98ff7-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="98ff7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ff7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98ff7-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="98ff7-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="98ff7-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98ff7-127">Namespace</span></span><br/>                | <span data-ttu-id="98ff7-128">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="98ff7-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="98ff7-129">MOF</span><span class="sxs-lookup"><span data-stu-id="98ff7-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98ff7-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98ff7-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98ff7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="98ff7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ff7-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98ff7-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98ff7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98ff7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ff7-134">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="98ff7-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




