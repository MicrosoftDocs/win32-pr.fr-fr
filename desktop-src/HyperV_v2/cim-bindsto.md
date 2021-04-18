---
description: Représente une association dans laquelle un \_ objet SERVICEACCESSPOINT CIM demande des services de protocole à partir d’un \_ objet ProtocolEndpoint CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Classe CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519365"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="2c223-103">\_Classe CIM BindsTo</span><span class="sxs-lookup"><span data-stu-id="2c223-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="2c223-104">Représente une association dans laquelle un objet [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) demande des services de protocole à partir d’un objet [**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="2c223-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c223-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c223-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2c223-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2c223-106">Members</span></span>

<span data-ttu-id="2c223-107">La classe **CIM \_ BindsTo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c223-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="2c223-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c223-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c223-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c223-109">Properties</span></span>

<span data-ttu-id="2c223-110">La classe **CIM \_ BindsTo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c223-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c223-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2c223-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c223-112">Type de données **: \_ ProtocolEndpoint CIM**</span><span class="sxs-lookup"><span data-stu-id="2c223-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="2c223-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c223-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c223-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2c223-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2c223-115">Point de terminaison de niveau inférieur auquel accède le point d’accès au service.</span><span class="sxs-lookup"><span data-stu-id="2c223-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="2c223-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2c223-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c223-117">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="2c223-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="2c223-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c223-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c223-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="2c223-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2c223-120">Point d’accès ou point de terminaison de protocole qui est dépendant du point de terminaison de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="2c223-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c223-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c223-121">Requirements</span></span>



| <span data-ttu-id="2c223-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c223-122">Requirement</span></span> | <span data-ttu-id="2c223-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c223-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c223-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c223-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c223-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c223-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2c223-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c223-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c223-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c223-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2c223-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c223-128">Namespace</span></span><br/>                | <span data-ttu-id="2c223-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c223-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c223-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2c223-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c223-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c223-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c223-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c223-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c223-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c223-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c223-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c223-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c223-135">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="2c223-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

