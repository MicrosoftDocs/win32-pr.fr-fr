---
description: Définition des données à transmettre en tant que tableau à la \_ classe MSVM CollectionReferencePointExportSettingData.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Classe Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862066"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="9fadf-103">MSVM \_ VirtualMachineToDisks, classe</span><span class="sxs-lookup"><span data-stu-id="9fadf-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="9fadf-104">Définition des données à transmettre en tant que tableau à la classe [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9fadf-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="9fadf-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9fadf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fadf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fadf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="9fadf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9fadf-107">Members</span></span>

<span data-ttu-id="9fadf-108">La classe **MSVM \_ VirtualMachineToDisks** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9fadf-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="9fadf-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9fadf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fadf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9fadf-110">Properties</span></span>

<span data-ttu-id="9fadf-111">La classe **MSVM \_ VirtualMachineToDisks** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fadf-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fadf-112">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="9fadf-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fadf-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9fadf-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9fadf-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fadf-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fadf-115">ID d’instance WMI des disques auxquels appartiennent l’ID d’ordinateur virtuel pour lequel les données doivent être exportées.</span><span class="sxs-lookup"><span data-stu-id="9fadf-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="9fadf-116">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="9fadf-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fadf-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fadf-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fadf-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9fadf-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9fadf-119">ID de machine virtuelle auquel les disques virtuels sont associés.</span><span class="sxs-lookup"><span data-stu-id="9fadf-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fadf-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fadf-120">Requirements</span></span>



| <span data-ttu-id="9fadf-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fadf-121">Requirement</span></span> | <span data-ttu-id="9fadf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fadf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fadf-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fadf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9fadf-124">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fadf-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9fadf-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fadf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9fadf-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9fadf-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9fadf-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9fadf-127">Namespace</span></span><br/>                | <span data-ttu-id="9fadf-128">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9fadf-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9fadf-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9fadf-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fadf-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fadf-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fadf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9fadf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fadf-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fadf-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




