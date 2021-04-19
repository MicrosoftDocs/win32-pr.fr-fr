---
description: Associe une tête vidéo à la carte vidéo qui la contient.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Classe CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534458"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="af958-103">\_Classe CIM VideoHeadOnController</span><span class="sxs-lookup"><span data-stu-id="af958-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="af958-104">Associe une tête vidéo à la carte vidéo qui la contient.</span><span class="sxs-lookup"><span data-stu-id="af958-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="af958-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af958-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="af958-106">Membres</span><span class="sxs-lookup"><span data-stu-id="af958-106">Members</span></span>

<span data-ttu-id="af958-107">La classe **CIM \_ VideoHeadOnController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="af958-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="af958-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af958-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af958-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af958-109">Properties</span></span>

<span data-ttu-id="af958-110">La classe **CIM \_ VideoHeadOnController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="af958-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af958-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="af958-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af958-112">Type de données : **CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="af958-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="af958-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af958-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af958-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="af958-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="af958-115">Carte vidéo qui comprend l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="af958-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="af958-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="af958-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af958-117">Type de données : **CIM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="af958-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="af958-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af958-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af958-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="af958-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="af958-120">Le début de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="af958-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af958-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af958-121">Requirements</span></span>



| <span data-ttu-id="af958-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af958-122">Requirement</span></span> | <span data-ttu-id="af958-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="af958-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af958-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af958-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af958-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="af958-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="af958-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af958-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af958-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af958-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="af958-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af958-128">Namespace</span></span><br/>                | <span data-ttu-id="af958-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="af958-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="af958-130">MOF</span><span class="sxs-lookup"><span data-stu-id="af958-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af958-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af958-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af958-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af958-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af958-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af958-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af958-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af958-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af958-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="af958-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

