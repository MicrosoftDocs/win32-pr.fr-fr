---
description: Association générique utilisée pour établir une partie des relations entre des éléments managés.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523284"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="c0490-103">MSVM \_ ConcreteComponent, classe</span><span class="sxs-lookup"><span data-stu-id="c0490-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="c0490-104">Association générique utilisée pour établir des relations « partie de » entre des éléments managés.</span><span class="sxs-lookup"><span data-stu-id="c0490-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="c0490-105">[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) est défini comme une sous-classe concrète de la classe de [**\_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component) abstraite, à utiliser à la place de nombreuses sous-classes spécifiques de composant qui n’ajoutent aucune sémantique (c’est-à-dire des sous-classes qui ne clarifient pas le type de composition, les cardinales de mise à jour ou l’ajout ou la suppression de qualificateurs).</span><span class="sxs-lookup"><span data-stu-id="c0490-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="c0490-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c0490-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0490-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0490-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c0490-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c0490-108">Members</span></span>

<span data-ttu-id="c0490-109">La classe **MSVM \_ ConcreteComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0490-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="c0490-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0490-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0490-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0490-111">Properties</span></span>

<span data-ttu-id="c0490-112">La classe **MSVM \_ ConcreteComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0490-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0490-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c0490-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0490-114">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c0490-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c0490-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0490-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0490-116">Élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="c0490-116">The parent element in the association.</span></span> <span data-ttu-id="c0490-117">Cette propriété est héritée de la [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0490-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c0490-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c0490-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0490-119">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c0490-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c0490-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0490-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0490-121">Élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="c0490-121">The child element in the association.</span></span> <span data-ttu-id="c0490-122">Cette propriété est héritée de la [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0490-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0490-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c0490-123">Remarks</span></span>

<span data-ttu-id="c0490-124">L’accès à la classe **MSVM \_ ConcreteComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="c0490-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c0490-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c0490-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0490-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0490-126">Requirements</span></span>



| <span data-ttu-id="c0490-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0490-127">Requirement</span></span> | <span data-ttu-id="c0490-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0490-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0490-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0490-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0490-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0490-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c0490-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0490-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0490-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0490-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0490-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c0490-133">Namespace</span></span><br/>                | <span data-ttu-id="c0490-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0490-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c0490-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c0490-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0490-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0490-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0490-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c0490-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0490-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0490-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0490-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0490-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0490-140">**\_CONCRETECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="c0490-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="c0490-141">[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0490-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0490-142">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="c0490-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

