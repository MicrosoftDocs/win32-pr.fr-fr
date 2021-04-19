---
description: Représente un point d’accès de service (SAP), qui est en mesure d’utiliser ou d’appeler un service. SAP indique qu’un service peut être utilisé par d’autres entités.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: Classe CIM_ServiceAccessPoint (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516691"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="7ec91-104">Classe CIM_ServiceAccessPoint (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7ec91-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="7ec91-105">Représente un point d’accès de service (SAP), qui est en mesure d’utiliser ou d’appeler un service.</span><span class="sxs-lookup"><span data-stu-id="7ec91-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="7ec91-106">SAP indique qu’un service peut être utilisé par d’autres entités.</span><span class="sxs-lookup"><span data-stu-id="7ec91-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec91-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec91-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7ec91-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7ec91-108">Members</span></span>

<span data-ttu-id="7ec91-109">La classe **CIM \_ ServiceAccessPoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7ec91-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7ec91-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ec91-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ec91-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ec91-111">Properties</span></span>

<span data-ttu-id="7ec91-112">La classe **CIM \_ ServiceAccessPoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ec91-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ec91-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ec91-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec91-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ec91-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ec91-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ec91-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ec91-117">Nom de classe utilisé pour créer une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="7ec91-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="7ec91-118">**CreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7ec91-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7ec91-119">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7ec91-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec91-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ec91-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ec91-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-122">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ec91-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ec91-123">Nom unique du SAP qui indique les fonctionnalités prises en charge par SAP.</span><span class="sxs-lookup"><span data-stu-id="7ec91-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="7ec91-124">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ec91-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec91-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ec91-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ec91-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="7ec91-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="7ec91-128">Nom de la classe utilisé pour créer une instance du système qui contient SAP.</span><span class="sxs-lookup"><span data-stu-id="7ec91-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="7ec91-129">**SystemCreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7ec91-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7ec91-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7ec91-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec91-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ec91-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ec91-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec91-133">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="7ec91-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="7ec91-134">Nom du système qui contient SAP.</span><span class="sxs-lookup"><span data-stu-id="7ec91-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ec91-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec91-135">Requirements</span></span>



| <span data-ttu-id="7ec91-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec91-136">Requirement</span></span> | <span data-ttu-id="7ec91-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec91-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec91-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec91-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec91-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ec91-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7ec91-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec91-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec91-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ec91-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7ec91-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ec91-142">Namespace</span></span><br/>                | <span data-ttu-id="7ec91-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ec91-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7ec91-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7ec91-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ec91-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ec91-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ec91-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec91-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ec91-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ec91-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ec91-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec91-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec91-149">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7ec91-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

