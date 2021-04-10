---
description: Associe une tête vidéo au contrôleur vidéo qui l’intègre.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Classe Msvm_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115403"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="4b6f6-103">MSVM \_ VideoHeadOnController, classe</span><span class="sxs-lookup"><span data-stu-id="4b6f6-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="4b6f6-104">Associe une tête vidéo au contrôleur vidéo qui l’intègre.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="4b6f6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6f6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b6f6-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4b6f6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4b6f6-107">Members</span></span>

<span data-ttu-id="4b6f6-108">La classe **MSVM \_ VideoHeadOnController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b6f6-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="4b6f6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b6f6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b6f6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b6f6-110">Properties</span></span>

<span data-ttu-id="4b6f6-111">La classe **MSVM \_ VideoHeadOnController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b6f6-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4b6f6-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b6f6-113">Type de données : **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4b6f6-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="4b6f6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b6f6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b6f6-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4b6f6-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4b6f6-116">Contrôleur vidéo qui comprend l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="4b6f6-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4b6f6-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b6f6-118">Type de données : **[ **MSVM \_ VideoHead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="4b6f6-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4b6f6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b6f6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b6f6-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4b6f6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4b6f6-121">La tête du périphérique vidéo.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b6f6-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4b6f6-122">Remarks</span></span>

<span data-ttu-id="4b6f6-123">L’accès à la classe **MSVM \_ VideoHeadOnController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4b6f6-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4b6f6-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4b6f6-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6f6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b6f6-125">Requirements</span></span>



| <span data-ttu-id="4b6f6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b6f6-126">Requirement</span></span> | <span data-ttu-id="4b6f6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b6f6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6f6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b6f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b6f6-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b6f6-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4b6f6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b6f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b6f6-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b6f6-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b6f6-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b6f6-132">Namespace</span></span><br/>                | <span data-ttu-id="4b6f6-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b6f6-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4b6f6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4b6f6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b6f6-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b6f6-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b6f6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4b6f6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b6f6-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b6f6-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b6f6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b6f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6f6-139">**\_VIDEOHEADONCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="4b6f6-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="4b6f6-140">[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b6f6-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4b6f6-141">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="4b6f6-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

