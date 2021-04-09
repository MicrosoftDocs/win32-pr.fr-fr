---
description: Déplace un disque dur virtuel de la source vers le chemin d’accès de destination.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Classe Msvm_MoveUnmanagedVhd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868498"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="98184-103">MSVM \_ MoveUnmanagedVhd, classe</span><span class="sxs-lookup"><span data-stu-id="98184-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="98184-104">Déplace un disque dur virtuel de la source vers le chemin d’accès de destination.</span><span class="sxs-lookup"><span data-stu-id="98184-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="98184-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="98184-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98184-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98184-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="98184-107">Membres</span><span class="sxs-lookup"><span data-stu-id="98184-107">Members</span></span>

<span data-ttu-id="98184-108">La classe **MSVM \_ MoveUnmanagedVhd** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98184-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="98184-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98184-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98184-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98184-110">Properties</span></span>

<span data-ttu-id="98184-111">La classe **MSVM \_ MoveUnmanagedVhd** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="98184-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98184-112">**VhdDestinationPath**</span><span class="sxs-lookup"><span data-stu-id="98184-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98184-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98184-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98184-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98184-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98184-115">Chemin d'accès de destination.</span><span class="sxs-lookup"><span data-stu-id="98184-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="98184-116">**VhdSourcePath**</span><span class="sxs-lookup"><span data-stu-id="98184-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98184-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98184-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98184-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98184-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98184-119">Chemin source du disque dur virtuel à déplacer.</span><span class="sxs-lookup"><span data-stu-id="98184-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98184-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98184-120">Requirements</span></span>



| <span data-ttu-id="98184-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98184-121">Requirement</span></span> | <span data-ttu-id="98184-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="98184-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98184-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98184-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98184-124">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98184-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="98184-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98184-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98184-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="98184-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="98184-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98184-127">Namespace</span></span><br/>                | <span data-ttu-id="98184-128">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="98184-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="98184-129">MOF</span><span class="sxs-lookup"><span data-stu-id="98184-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98184-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98184-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98184-131">DLL</span><span class="sxs-lookup"><span data-stu-id="98184-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98184-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98184-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98184-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98184-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98184-134">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="98184-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




