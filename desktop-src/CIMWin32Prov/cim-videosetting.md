---
description: La \_ classe CIM VideoSetting associe l' \_ objet de paramètre CIM VideoControllerResolution au contrôleur auquel il s’applique.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: Classe CIM_VideoSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529099"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="737a6-103">\_Classe CIM VideoSetting</span><span class="sxs-lookup"><span data-stu-id="737a6-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="737a6-104">La classe **CIM \_ VideoSetting** associe l’objet de paramètre [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) au contrôleur auquel il s’applique.</span><span class="sxs-lookup"><span data-stu-id="737a6-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="737a6-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="737a6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="737a6-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="737a6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="737a6-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="737a6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="737a6-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="737a6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="737a6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="737a6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="737a6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="737a6-110">Members</span></span>

<span data-ttu-id="737a6-111">La classe **CIM \_ VideoSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="737a6-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="737a6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="737a6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="737a6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="737a6-113">Properties</span></span>

<span data-ttu-id="737a6-114">La classe **CIM \_ VideoSetting** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="737a6-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="737a6-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="737a6-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="737a6-116">Type de données : **CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="737a6-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="737a6-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="737a6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="737a6-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element")</span><span class="sxs-lookup"><span data-stu-id="737a6-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="737a6-119">[**\_ VideoController CIM**](cim-videocontroller.md) qui décrit le contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="737a6-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="737a6-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="737a6-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="737a6-121">Type de données : **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="737a6-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="737a6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="737a6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="737a6-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span><span class="sxs-lookup"><span data-stu-id="737a6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="737a6-124">[**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) qui décrit les résolutions, les taux de rafraîchissement, le mode d’analyse et le nombre de couleurs qui peuvent être définies pour le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="737a6-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="737a6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="737a6-125">Remarks</span></span>

<span data-ttu-id="737a6-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="737a6-126">WMI does not implement this class.</span></span> <span data-ttu-id="737a6-127">Pour les classes WMI dérivées de **CIM \_ VideoSetting**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="737a6-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="737a6-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="737a6-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="737a6-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="737a6-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="737a6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="737a6-130">Requirements</span></span>



| <span data-ttu-id="737a6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="737a6-131">Requirement</span></span> | <span data-ttu-id="737a6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="737a6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="737a6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="737a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="737a6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="737a6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="737a6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="737a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="737a6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="737a6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="737a6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="737a6-137">Namespace</span></span><br/>                | <span data-ttu-id="737a6-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="737a6-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="737a6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="737a6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="737a6-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="737a6-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="737a6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="737a6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="737a6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="737a6-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737a6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="737a6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737a6-144">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="737a6-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

