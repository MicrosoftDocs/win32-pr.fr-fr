---
description: Association entre un point d’accès de service (SAP) et son implémentation.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Classe Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862462"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="a4089-103">MSVM \_ WiFiDeviceSAPImplementation, classe</span><span class="sxs-lookup"><span data-stu-id="a4089-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="a4089-104">Association entre un point d’accès de service (SAP) et son implémentation.</span><span class="sxs-lookup"><span data-stu-id="a4089-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="a4089-105">La cardinalité de cette association est plusieurs-à-plusieurs.</span><span class="sxs-lookup"><span data-stu-id="a4089-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="a4089-106">Un SAP peut être fourni par plusieurs unités logiques, fonctionnant conjointement.</span><span class="sxs-lookup"><span data-stu-id="a4089-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="a4089-107">N’importe quel appareil peut fournir plusieurs SAP.</span><span class="sxs-lookup"><span data-stu-id="a4089-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="a4089-108">Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="a4089-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="a4089-109">Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="a4089-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="a4089-110">Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.</span><span class="sxs-lookup"><span data-stu-id="a4089-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="a4089-111">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a4089-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4089-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4089-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a4089-113">Membres</span><span class="sxs-lookup"><span data-stu-id="a4089-113">Members</span></span>

<span data-ttu-id="a4089-114">La classe **MSVM \_ WiFiDeviceSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a4089-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="a4089-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a4089-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4089-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a4089-116">Properties</span></span>

<span data-ttu-id="a4089-117">La classe **MSVM \_ WiFiDeviceSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a4089-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4089-118">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="a4089-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4089-119">Type de données : **[ **MSVM \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="a4089-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a4089-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4089-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4089-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a4089-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a4089-122">Instance de la classe [**MSVM \_ WiFiPort**](msvm-wifiport.md) qui représente l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="a4089-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="a4089-123">**Charge**</span><span class="sxs-lookup"><span data-stu-id="a4089-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4089-124">Type de données : **[ **MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="a4089-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a4089-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4089-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4089-126">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="a4089-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a4089-127">Instance de la classe [**MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md) qui représente le point d’accès au service implémenté à l’aide de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a4089-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4089-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4089-128">Requirements</span></span>



| <span data-ttu-id="a4089-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4089-129">Requirement</span></span> | <span data-ttu-id="a4089-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4089-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4089-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4089-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4089-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4089-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4089-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4089-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4089-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4089-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4089-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4089-135">Namespace</span></span><br/>                | <span data-ttu-id="a4089-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4089-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4089-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a4089-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4089-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4089-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4089-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a4089-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4089-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4089-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

