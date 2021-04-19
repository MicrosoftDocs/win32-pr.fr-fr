---
description: Association entre une instance de CIM \_ VirtualSystemSettingData et l' \_ instance VirtualSystemSettingData CIM qui représente l’instantané le plus récent sur lequel cet objet est basé.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542632"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="e52c9-103">\_Classe CIM ParentChildSettingData</span><span class="sxs-lookup"><span data-stu-id="e52c9-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="e52c9-104">Association entre une instance de [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) et l’instance **\_ VirtualSystemSettingData CIM** qui représente l’instantané le plus récent sur lequel cet objet est basé.</span><span class="sxs-lookup"><span data-stu-id="e52c9-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e52c9-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e52c9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e52c9-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e52c9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e52c9-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e52c9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52c9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e52c9-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="e52c9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e52c9-109">Members</span></span>

<span data-ttu-id="e52c9-110">La classe **CIM \_ ParentChildSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e52c9-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e52c9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e52c9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e52c9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e52c9-112">Properties</span></span>

<span data-ttu-id="e52c9-113">La classe **CIM \_ ParentChildSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e52c9-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e52c9-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e52c9-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e52c9-115">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="e52c9-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e52c9-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e52c9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e52c9-117">Référence à l’objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="e52c9-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="e52c9-118">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="e52c9-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="e52c9-119">**Enfant**</span><span class="sxs-lookup"><span data-stu-id="e52c9-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e52c9-120">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="e52c9-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e52c9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e52c9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e52c9-122">Données de paramètre pour le système virtuel qui représente l’enfant du parent.</span><span class="sxs-lookup"><span data-stu-id="e52c9-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="e52c9-123">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e52c9-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e52c9-124">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="e52c9-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e52c9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e52c9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e52c9-126">Référence à l’objet qui est dépendant de la propriété **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="e52c9-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="e52c9-127">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="e52c9-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="e52c9-128">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e52c9-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e52c9-129">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="e52c9-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e52c9-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e52c9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e52c9-131">Données de paramètre d’instantané sur lesquelles les données de paramètres enfants sont basées.</span><span class="sxs-lookup"><span data-stu-id="e52c9-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e52c9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e52c9-132">Requirements</span></span>



| <span data-ttu-id="e52c9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e52c9-133">Requirement</span></span> | <span data-ttu-id="e52c9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e52c9-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="e52c9-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e52c9-135">Namespace</span></span><br/> | <span data-ttu-id="e52c9-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e52c9-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e52c9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e52c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52c9-138">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e52c9-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

