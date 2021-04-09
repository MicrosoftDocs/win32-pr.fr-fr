---
description: Contient un résumé des informations sur le système d’ordinateur virtuel spécifié.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Classe Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862653"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="14356-103">MSVM \_ ComputerSystemSummaryInformation, classe</span><span class="sxs-lookup"><span data-stu-id="14356-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="14356-104">Contient un résumé des informations sur le système d’ordinateur virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="14356-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="14356-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="14356-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14356-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14356-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="14356-107">Membres</span><span class="sxs-lookup"><span data-stu-id="14356-107">Members</span></span>

<span data-ttu-id="14356-108">La classe **MSVM \_ ComputerSystemSummaryInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14356-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="14356-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14356-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14356-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14356-110">Properties</span></span>

<span data-ttu-id="14356-111">La classe **MSVM \_ ComputerSystemSummaryInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="14356-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14356-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="14356-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14356-113">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="14356-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="14356-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14356-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14356-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="14356-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="14356-116">Objet [**CIM \_ CIM**](cim-computersystem.md) qui est une instance dans la représentation normalisée de la ressource managée.</span><span class="sxs-lookup"><span data-stu-id="14356-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="14356-117">Type de données mis à niveau à partir de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="14356-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="14356-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="14356-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14356-119">Type de données : **MSVM \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="14356-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="14356-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14356-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14356-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="14356-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="14356-122">Instance de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représente une vue dénormalisée ou agrégée de la ressource managée représentée par le [**MSVM \_ ComputerSystem**](msvm-computersystem.md) référencé par la propriété Antecedent.</span><span class="sxs-lookup"><span data-stu-id="14356-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="14356-123">Type de données mis à jour à partir de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="14356-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14356-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14356-124">Requirements</span></span>



| <span data-ttu-id="14356-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14356-125">Requirement</span></span> | <span data-ttu-id="14356-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="14356-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14356-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14356-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14356-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14356-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="14356-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14356-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14356-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="14356-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="14356-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="14356-131">Namespace</span></span><br/>                | <span data-ttu-id="14356-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="14356-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14356-133">MOF</span><span class="sxs-lookup"><span data-stu-id="14356-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14356-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14356-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14356-135">DLL</span><span class="sxs-lookup"><span data-stu-id="14356-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14356-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14356-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14356-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14356-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14356-138">**\_ELEMENTVIEW CIM**</span><span class="sxs-lookup"><span data-stu-id="14356-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

