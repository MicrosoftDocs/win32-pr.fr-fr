---
description: 'Msvm_FcDeviceSAPImplementation Class : représente une association entre un point d’accès au service et l’appareil logique qui l’implémente.'
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Classe Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119027"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="cb996-103">MSVM \_ FcDeviceSAPImplementation, classe</span><span class="sxs-lookup"><span data-stu-id="cb996-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="cb996-104">Représente une association entre un point d’accès de service et l’appareil logique qui l’implémente.</span><span class="sxs-lookup"><span data-stu-id="cb996-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="cb996-105">La cardinalité de cette association est plusieurs-à-plusieurs.</span><span class="sxs-lookup"><span data-stu-id="cb996-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="cb996-106">Un point d’accès au service (SAP) peut être fourni par plusieurs unités logiques, fonctionnant conjointement.</span><span class="sxs-lookup"><span data-stu-id="cb996-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="cb996-107">N’importe quel appareil peut fournir plusieurs SAP.</span><span class="sxs-lookup"><span data-stu-id="cb996-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="cb996-108">Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="cb996-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="cb996-109">Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="cb996-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="cb996-110">Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.</span><span class="sxs-lookup"><span data-stu-id="cb996-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="cb996-111">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb996-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb996-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb996-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cb996-113">Membres</span><span class="sxs-lookup"><span data-stu-id="cb996-113">Members</span></span>

<span data-ttu-id="cb996-114">La classe **MSVM \_ FcDeviceSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb996-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="cb996-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb996-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb996-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb996-116">Properties</span></span>

<span data-ttu-id="cb996-117">La classe **MSVM \_ FcDeviceSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb996-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb996-118">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="cb996-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb996-119">Type de données : **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="cb996-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="cb996-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb996-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb996-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="cb996-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cb996-122">Référence à une classe dérivée de **CIM \_ FCPort** qui représente l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="cb996-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cb996-123">**Charge**</span><span class="sxs-lookup"><span data-stu-id="cb996-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb996-124">Type de données : **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="cb996-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="cb996-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb996-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb996-126">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="cb996-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cb996-127">Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le SAP qui utilise l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="cb996-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb996-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb996-128">Requirements</span></span>



| <span data-ttu-id="cb996-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb996-129">Requirement</span></span> | <span data-ttu-id="cb996-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb996-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb996-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb996-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cb996-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb996-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cb996-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb996-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cb996-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb996-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb996-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb996-135">Namespace</span></span><br/>                | <span data-ttu-id="cb996-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb996-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cb996-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cb996-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb996-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb996-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb996-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cb996-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb996-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb996-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

