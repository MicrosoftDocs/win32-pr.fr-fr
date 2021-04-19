---
description: Gère les appareils attribuables sur un système d’ordinateur hôte.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525745"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="00e03-103">MSVM \_ AssignableDeviceService, classe</span><span class="sxs-lookup"><span data-stu-id="00e03-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="00e03-104">Gère les appareils attribuables sur un système d’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="00e03-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="00e03-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00e03-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e03-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00e03-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="00e03-107">Membres</span><span class="sxs-lookup"><span data-stu-id="00e03-107">Members</span></span>

<span data-ttu-id="00e03-108">La classe **MSVM \_ AssignableDeviceService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00e03-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="00e03-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00e03-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="00e03-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00e03-110">Methods</span></span>

<span data-ttu-id="00e03-111">La classe **MSVM \_ AssignableDeviceService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="00e03-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="00e03-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="00e03-112">Method</span></span>                                                                                    | <span data-ttu-id="00e03-113">Description</span><span class="sxs-lookup"><span data-stu-id="00e03-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00e03-114">**DismountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="00e03-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="00e03-115">Démonte l’appareil PCI spécifié afin qu’il puisse être attribué.</span><span class="sxs-lookup"><span data-stu-id="00e03-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="00e03-116">**MountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="00e03-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="00e03-117">Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="00e03-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="00e03-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00e03-118">Requirements</span></span>



| <span data-ttu-id="00e03-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00e03-119">Requirement</span></span> | <span data-ttu-id="00e03-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="00e03-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e03-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00e03-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00e03-122">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00e03-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="00e03-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00e03-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00e03-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="00e03-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="00e03-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00e03-125">Namespace</span></span><br/>                | <span data-ttu-id="00e03-126">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="00e03-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="00e03-127">MOF</span><span class="sxs-lookup"><span data-stu-id="00e03-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00e03-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00e03-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00e03-129">DLL</span><span class="sxs-lookup"><span data-stu-id="00e03-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00e03-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00e03-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00e03-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00e03-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e03-132">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="00e03-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




