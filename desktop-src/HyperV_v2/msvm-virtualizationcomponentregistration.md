---
description: Représente l’inscription d’un service dans la plateforme Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Classe Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517450"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="eb341-103">MSVM \_ VirtualizationComponentRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="eb341-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="eb341-104">Représente l’inscription d’un service dans la plateforme Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="eb341-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="eb341-105">La syntaxe suivante est simplifiée format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb341-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb341-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb341-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="eb341-107">Membres</span><span class="sxs-lookup"><span data-stu-id="eb341-107">Members</span></span>

<span data-ttu-id="eb341-108">La classe **MSVM \_ VirtualizationComponentRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb341-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="eb341-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb341-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb341-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb341-110">Properties</span></span>

<span data-ttu-id="eb341-111">La classe **MSVM \_ VirtualizationComponentRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb341-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb341-112">**Composant**</span><span class="sxs-lookup"><span data-stu-id="eb341-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb341-113">Type de données : **[ **MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="eb341-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eb341-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb341-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb341-115">Référence à une instance de qui décrit l’objet COM qui implémente cette classe.</span><span class="sxs-lookup"><span data-stu-id="eb341-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="eb341-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="eb341-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb341-117">Type de données : **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="eb341-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eb341-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb341-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb341-119">Référence à une instance de qui décrit un type de ressource pris en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="eb341-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb341-120">Notes</span><span class="sxs-lookup"><span data-stu-id="eb341-120">Remarks</span></span>

<span data-ttu-id="eb341-121">L’accès à la classe **MSVM \_ VirtualizationComponentRegistration** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="eb341-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eb341-122">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eb341-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb341-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb341-123">Requirements</span></span>



| <span data-ttu-id="eb341-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb341-124">Requirement</span></span> | <span data-ttu-id="eb341-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb341-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb341-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb341-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb341-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb341-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eb341-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb341-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb341-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb341-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb341-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="eb341-130">End of client support</span></span><br/>    | <span data-ttu-id="eb341-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb341-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="eb341-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="eb341-132">End of server support</span></span><br/>    | <span data-ttu-id="eb341-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb341-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="eb341-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb341-134">Namespace</span></span><br/>                | <span data-ttu-id="eb341-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb341-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eb341-136">MOF</span><span class="sxs-lookup"><span data-stu-id="eb341-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb341-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb341-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb341-138">DLL</span><span class="sxs-lookup"><span data-stu-id="eb341-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb341-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb341-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

