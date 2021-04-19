---
description: Représente une association dans laquelle un élément managé est conforme à la norme d’un profil inscrit.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Classe CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517554"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="a2787-103">\_Classe CIM ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="a2787-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="a2787-104">Représente une association dans laquelle un élément managé est conforme à la norme d’un profil inscrit.</span><span class="sxs-lookup"><span data-stu-id="a2787-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="a2787-105">Cette association s’applique généralement à une instance de niveau supérieur, telle qu’un système, un espace de noms ou un service.</span><span class="sxs-lookup"><span data-stu-id="a2787-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="a2787-106">En cas d’application à une instance de niveau supérieur, tous les éléments constitutifs doivent se comporter de manière appropriée pour la prise en charge de la conformité du propriété ManagedElement au RegisteredProfile nommé.</span><span class="sxs-lookup"><span data-stu-id="a2787-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2787-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2787-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="a2787-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a2787-108">Members</span></span>

<span data-ttu-id="a2787-109">La classe **CIM \_ ElementConformsToProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2787-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="a2787-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2787-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2787-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2787-111">Properties</span></span>

<span data-ttu-id="a2787-112">La classe **CIM \_ ElementConformsToProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2787-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2787-113">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="a2787-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2787-114">Type de données : **CIM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="a2787-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="a2787-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2787-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2787-116">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2787-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a2787-117">Profil inscrit auquel l’élément managé est conforme.</span><span class="sxs-lookup"><span data-stu-id="a2787-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="a2787-118">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a2787-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2787-119">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a2787-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a2787-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2787-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2787-121">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2787-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a2787-122">Élément managé qui est conforme au profil inscrit.</span><span class="sxs-lookup"><span data-stu-id="a2787-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2787-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2787-123">Requirements</span></span>



| <span data-ttu-id="a2787-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2787-124">Requirement</span></span> | <span data-ttu-id="a2787-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2787-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2787-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2787-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a2787-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a2787-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a2787-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2787-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a2787-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2787-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a2787-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2787-130">Namespace</span></span><br/>                | <span data-ttu-id="a2787-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2787-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2787-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a2787-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2787-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2787-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2787-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a2787-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2787-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2787-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

