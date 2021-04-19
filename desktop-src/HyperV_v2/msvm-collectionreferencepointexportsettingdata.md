---
description: Exportez les données de paramètre à transmettre à la méthode ExportReferencePoint de la \_ classe CollectionReferencePointService MSVM.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523385"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="7b1f4-103">MSVM \_ CollectionReferencePointExportSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="7b1f4-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="7b1f4-104">Exportez les données de paramètre à transmettre à la méthode [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) de la classe [**\_ CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1f4-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="7b1f4-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b1f4-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="7b1f4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7b1f4-107">Members</span></span>

<span data-ttu-id="7b1f4-108">La classe **MSVM \_ CollectionReferencePointExportSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b1f4-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b1f4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b1f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b1f4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b1f4-110">Properties</span></span>

<span data-ttu-id="7b1f4-111">La classe **MSVM \_ CollectionReferencePointExportSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b1f4-112">**BaseReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b1f4-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b1f4-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b1f4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b1f4-115">Chemin d’accès à une instance [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) qui représente la collection de points de référence de base à utiliser pour l’exportation différentielle.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="7b1f4-116">**VirtualMachinesToDisksToExport**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b1f4-117">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7b1f4-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b1f4-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b1f4-119">Qualificateurs : **HyperVEmbeddedInstance** ("MSVM \_ VirtualMachineToDisks")</span><span class="sxs-lookup"><span data-stu-id="7b1f4-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="7b1f4-120">Liste des informations de mappage « VirtualMachines to DisksToExport » pour lesquelles les données doivent être exportées.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b1f4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b1f4-121">Requirements</span></span>



| <span data-ttu-id="7b1f4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b1f4-122">Requirement</span></span> | <span data-ttu-id="7b1f4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b1f4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1f4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b1f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7b1f4-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b1f4-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7b1f4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b1f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7b1f4-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b1f4-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7b1f4-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b1f4-128">Namespace</span></span><br/>                | <span data-ttu-id="7b1f4-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b1f4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b1f4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7b1f4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b1f4-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b1f4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b1f4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7b1f4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b1f4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b1f4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b1f4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b1f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1f4-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




