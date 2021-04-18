---
description: Représente une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès au média.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Classe CIM_MediaPresent (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106536427"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="5d8fb-103">Classe CIM_MediaPresent (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="5d8fb-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="5d8fb-104">Représente une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="5d8fb-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d8fb-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="5d8fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5d8fb-106">Members</span></span>

<span data-ttu-id="5d8fb-107">La classe **CIM \_ MediaPresent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5d8fb-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="5d8fb-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d8fb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d8fb-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d8fb-109">Properties</span></span>

<span data-ttu-id="5d8fb-110">La classe **CIM \_ MediaPresent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5d8fb-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d8fb-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d8fb-112">Type de données : **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5d8fb-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d8fb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d8fb-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="5d8fb-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5d8fb-115">L’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="5d8fb-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="5d8fb-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d8fb-117">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="5d8fb-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d8fb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d8fb-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="5d8fb-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5d8fb-120">L’étendue de stockage accessible lors de l’utilisation de l’appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="5d8fb-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="5d8fb-121">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d8fb-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d8fb-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d8fb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d8fb-124">**true** si l’extension de stockage est fixe dans le périphérique d’accès au support et ne peut pas être éjectée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5d8fb-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d8fb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d8fb-125">Requirements</span></span>



| <span data-ttu-id="5d8fb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d8fb-126">Requirement</span></span> | <span data-ttu-id="5d8fb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d8fb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8fb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d8fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8fb-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d8fb-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5d8fb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d8fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8fb-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d8fb-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5d8fb-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5d8fb-132">Namespace</span></span><br/>                | <span data-ttu-id="5d8fb-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5d8fb-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5d8fb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5d8fb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d8fb-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d8fb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d8fb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5d8fb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d8fb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d8fb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d8fb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d8fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8fb-139">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="5d8fb-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

