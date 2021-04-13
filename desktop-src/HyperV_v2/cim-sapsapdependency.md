---
description: Représente une association entre deux points d’accès de service (SAP), dans laquelle un SAP dépend de l’autre pour utiliser un service ou s’y connecter.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: Classe CIM_SAPSAPDependency (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526781"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="d9532-103">Classe CIM_SAPSAPDependency (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d9532-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="d9532-104">Représente une association entre deux points d’accès de service (SAP), dans laquelle un SAP dépend de l’autre pour utiliser un service ou s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="d9532-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="d9532-105">Par exemple, pour imprimer sur une imprimante réseau, les points d’accès d’impression locaux doivent utiliser des SAP liés au réseau sous-jacents pour envoyer la demande d’impression.</span><span class="sxs-lookup"><span data-stu-id="d9532-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9532-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9532-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d9532-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d9532-107">Members</span></span>

<span data-ttu-id="d9532-108">La classe **CIM \_ SAPSAPDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d9532-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d9532-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9532-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9532-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9532-110">Properties</span></span>

<span data-ttu-id="d9532-111">La classe **CIM \_ SAPSAPDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9532-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9532-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d9532-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9532-113">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="d9532-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d9532-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9532-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9532-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d9532-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d9532-116">Une référence au SAP requis.</span><span class="sxs-lookup"><span data-stu-id="d9532-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="d9532-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d9532-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9532-118">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="d9532-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d9532-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9532-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9532-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="d9532-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d9532-121">Référence à la fonction SAP dépendante.</span><span class="sxs-lookup"><span data-stu-id="d9532-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9532-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9532-122">Requirements</span></span>



| <span data-ttu-id="d9532-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9532-123">Requirement</span></span> | <span data-ttu-id="d9532-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9532-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9532-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9532-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9532-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d9532-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d9532-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9532-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9532-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9532-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d9532-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9532-129">Namespace</span></span><br/>                | <span data-ttu-id="d9532-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d9532-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d9532-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d9532-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9532-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9532-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9532-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d9532-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9532-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9532-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9532-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9532-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9532-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="d9532-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

