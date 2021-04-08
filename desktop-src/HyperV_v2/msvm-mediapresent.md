---
description: Associe un lecteur de stockage au support inséré dans le lecteur.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869593"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="3f438-103">MSVM \_ MediaPresent, classe</span><span class="sxs-lookup"><span data-stu-id="3f438-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="3f438-104">Associe un lecteur de stockage au support inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="3f438-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="3f438-105">Cette association est utilisée pour tous les objets de lecteur de stockage.</span><span class="sxs-lookup"><span data-stu-id="3f438-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="3f438-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3f438-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f438-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f438-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="3f438-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3f438-108">Members</span></span>

<span data-ttu-id="3f438-109">La classe **MSVM \_ MediaPresent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f438-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="3f438-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f438-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f438-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f438-111">Properties</span></span>

<span data-ttu-id="3f438-112">La classe **MSVM \_ MediaPresent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f438-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f438-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3f438-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f438-114">Type de données : **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="3f438-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="3f438-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f438-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f438-116">Référence à l’appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="3f438-116">The reference to the media access device.</span></span> <span data-ttu-id="3f438-117">Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="3f438-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="3f438-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3f438-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f438-119">Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="3f438-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="3f438-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f438-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f438-121">Référence à l’extension de stockage accessible avec l’appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="3f438-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="3f438-122">Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="3f438-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="3f438-123">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="3f438-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f438-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3f438-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f438-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f438-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f438-126">Indique si l’extension de stockage accessible est fixe et ne peut pas être éjectée.</span><span class="sxs-lookup"><span data-stu-id="3f438-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="3f438-127">La valeur est **true** pour les disques durs et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3f438-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="3f438-128">Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="3f438-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f438-129">Notes</span><span class="sxs-lookup"><span data-stu-id="3f438-129">Remarks</span></span>

<span data-ttu-id="3f438-130">L’accès à la classe **MSVM \_ MediaPresent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="3f438-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3f438-131">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3f438-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f438-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f438-132">Requirements</span></span>



| <span data-ttu-id="3f438-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f438-133">Requirement</span></span> | <span data-ttu-id="3f438-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f438-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f438-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f438-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3f438-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f438-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f438-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f438-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3f438-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f438-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f438-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f438-139">Namespace</span></span><br/>                | <span data-ttu-id="3f438-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f438-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f438-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3f438-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f438-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f438-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f438-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3f438-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f438-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f438-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f438-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f438-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f438-146">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3f438-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="3f438-147">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3f438-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="3f438-148">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="3f438-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

