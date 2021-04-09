---
description: La \_ classe CIM MonitorSetting associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: Classe CIM_MonitorSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861325"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="92559-103">\_Classe CIM MonitorSetting</span><span class="sxs-lookup"><span data-stu-id="92559-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="92559-104">La classe **CIM \_ MonitorSetting** associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.</span><span class="sxs-lookup"><span data-stu-id="92559-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92559-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="92559-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="92559-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="92559-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="92559-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="92559-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="92559-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="92559-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92559-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92559-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="92559-110">Membres</span><span class="sxs-lookup"><span data-stu-id="92559-110">Members</span></span>

<span data-ttu-id="92559-111">La classe **CIM \_ MonitorSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92559-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="92559-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92559-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92559-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92559-113">Properties</span></span>

<span data-ttu-id="92559-114">La classe **CIM \_ MonitorSetting** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="92559-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92559-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="92559-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92559-116">Type de données : **CIM \_ desktopmonitor**</span><span class="sxs-lookup"><span data-stu-id="92559-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="92559-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92559-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92559-118">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element")</span><span class="sxs-lookup"><span data-stu-id="92559-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="92559-119">[**\_ Desktopmonitor CIM**](cim-desktopmonitor.md) décrivant le moniteur de bureau.</span><span class="sxs-lookup"><span data-stu-id="92559-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="92559-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="92559-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92559-121">Type de données : **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="92559-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="92559-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92559-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92559-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("paramètre")</span><span class="sxs-lookup"><span data-stu-id="92559-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="92559-124">[**\_ MonitorResolution CIM**](cim-monitorresolution.md) décrivant la résolution de l’analyseur associée à l’analyseur de bureau.</span><span class="sxs-lookup"><span data-stu-id="92559-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92559-125">Notes</span><span class="sxs-lookup"><span data-stu-id="92559-125">Remarks</span></span>

<span data-ttu-id="92559-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="92559-126">WMI does not implement this class.</span></span>

<span data-ttu-id="92559-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="92559-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="92559-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="92559-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92559-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92559-129">Requirements</span></span>



| <span data-ttu-id="92559-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92559-130">Requirement</span></span> | <span data-ttu-id="92559-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="92559-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92559-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92559-132">Minimum supported client</span></span><br/> | <span data-ttu-id="92559-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92559-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92559-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92559-134">Minimum supported server</span></span><br/> | <span data-ttu-id="92559-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92559-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92559-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92559-136">Namespace</span></span><br/>                | <span data-ttu-id="92559-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="92559-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92559-138">MOF</span><span class="sxs-lookup"><span data-stu-id="92559-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92559-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92559-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92559-140">DLL</span><span class="sxs-lookup"><span data-stu-id="92559-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92559-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92559-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92559-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92559-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92559-143">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="92559-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

