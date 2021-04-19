---
description: Associe le \_ BootSourceSettingData MSVM au VirtualSystemSettingData MSVM global \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536982"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="9f6f3-103">MSVM \_ BootSourceComponent, classe</span><span class="sxs-lookup"><span data-stu-id="9f6f3-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="9f6f3-104">Associe [**le \_ BootSourceSettingData MSVM**](msvm-bootsourcesettingdata.md) au [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md)global.</span><span class="sxs-lookup"><span data-stu-id="9f6f3-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="9f6f3-105">Cette classe dérive du [**\_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="9f6f3-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="9f6f3-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9f6f3-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f6f3-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9f6f3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9f6f3-108">Members</span></span>

<span data-ttu-id="9f6f3-109">La classe **MSVM \_ BootSourceComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9f6f3-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9f6f3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f6f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f6f3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f6f3-111">Properties</span></span>

<span data-ttu-id="9f6f3-112">La classe **MSVM \_ BootSourceComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f6f3-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f6f3-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f6f3-114">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9f6f3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f6f3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f6f3-116">Référence à l’élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9f6f3-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="9f6f3-117">Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="9f6f3-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f6f3-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f6f3-119">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9f6f3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f6f3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f6f3-121">Référence à l’élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9f6f3-121">Reference to the child element in the association.</span></span> <span data-ttu-id="9f6f3-122">Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="9f6f3-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f6f3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f6f3-123">Requirements</span></span>



| <span data-ttu-id="9f6f3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f6f3-124">Requirement</span></span> | <span data-ttu-id="9f6f3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f6f3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6f3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f6f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6f3-127">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f6f3-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9f6f3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f6f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6f3-129">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f6f3-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f6f3-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f6f3-130">Namespace</span></span><br/>                | <span data-ttu-id="9f6f3-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f6f3-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f6f3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9f6f3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f6f3-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f3-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f6f3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6f3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f6f3-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f3-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f6f3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f6f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6f3-137">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="9f6f3-138">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="9f6f3-139">**MSVM \_ BootSourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="9f6f3-140">**MSVM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="9f6f3-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

