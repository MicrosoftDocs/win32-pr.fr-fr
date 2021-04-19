---
description: Associe un service de pontage transparent à une entrée de sa base de données de transfert.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: Classe CIM_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518190"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="caff4-103">\_Classe CIM TransparentBridgingDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="caff4-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="caff4-104">Associe un service de pontage transparent à une entrée de sa base de données de transfert.</span><span class="sxs-lookup"><span data-stu-id="caff4-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="caff4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caff4-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="caff4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="caff4-106">Members</span></span>

<span data-ttu-id="caff4-107">La classe **CIM \_ TransparentBridgingDynamicForwarding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="caff4-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="caff4-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="caff4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="caff4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="caff4-109">Properties</span></span>

<span data-ttu-id="caff4-110">La classe **CIM \_ TransparentBridgingDynamicForwarding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="caff4-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="caff4-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="caff4-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caff4-112">Type de données : **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="caff4-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="caff4-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="caff4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caff4-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="caff4-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="caff4-115">Référence [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) au service de pontage transparent.</span><span class="sxs-lookup"><span data-stu-id="caff4-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="caff4-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="caff4-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caff4-117">Type de données : **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="caff4-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="caff4-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="caff4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caff4-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="caff4-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="caff4-120">Référence [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) à l’entrée de la base de données de transfert.</span><span class="sxs-lookup"><span data-stu-id="caff4-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="caff4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caff4-121">Requirements</span></span>



| <span data-ttu-id="caff4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caff4-122">Requirement</span></span> | <span data-ttu-id="caff4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="caff4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caff4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caff4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="caff4-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="caff4-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="caff4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caff4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="caff4-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="caff4-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="caff4-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="caff4-128">Namespace</span></span><br/>                | <span data-ttu-id="caff4-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="caff4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="caff4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="caff4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caff4-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="caff4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="caff4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="caff4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caff4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="caff4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="caff4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caff4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caff4-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="caff4-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

