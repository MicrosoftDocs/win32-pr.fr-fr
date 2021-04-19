---
description: Représente une association générique entre deux éléments managés qui représentent différents aspects de la même entité sous-jacente.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: Classe CIM_LogicalIdentity (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536320"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="a25a3-103">Classe CIM_LogicalIdentity (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="a25a3-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="a25a3-104">Représente une association générique entre deux éléments managés qui représentent différents aspects de la même entité sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="a25a3-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="a25a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a25a3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="a25a3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a25a3-106">Members</span></span>

<span data-ttu-id="a25a3-107">La classe **CIM \_ LogicalIdentity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a25a3-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="a25a3-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a25a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a25a3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a25a3-109">Properties</span></span>

<span data-ttu-id="a25a3-110">La classe **CIM \_ LogicalIdentity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a25a3-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a25a3-111">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="a25a3-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a25a3-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a25a3-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a25a3-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a25a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a25a3-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a25a3-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a25a3-115">Deuxième aspect de l’Association.</span><span class="sxs-lookup"><span data-stu-id="a25a3-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a25a3-116">**SYSTEME**</span><span class="sxs-lookup"><span data-stu-id="a25a3-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a25a3-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a25a3-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a25a3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a25a3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a25a3-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a25a3-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a25a3-120">Premier aspect de l’Association.</span><span class="sxs-lookup"><span data-stu-id="a25a3-120">The first aspect in the association.</span></span> <span data-ttu-id="a25a3-121">L’utilisation du système dans le nom de propriété ne limite pas l’étendue de l’Association.</span><span class="sxs-lookup"><span data-stu-id="a25a3-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a25a3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a25a3-122">Requirements</span></span>



| <span data-ttu-id="a25a3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a25a3-123">Requirement</span></span> | <span data-ttu-id="a25a3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a25a3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25a3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a25a3-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a25a3-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a25a3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a25a3-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a25a3-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a25a3-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a25a3-129">Namespace</span></span><br/>                | <span data-ttu-id="a25a3-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a25a3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a25a3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a25a3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a25a3-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a25a3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a25a3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a25a3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a25a3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a25a3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

