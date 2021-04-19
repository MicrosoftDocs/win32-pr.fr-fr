---
description: La \_ classe CIM ElementSetting représente l’association entre les éléments système gérés et la classe de paramètres définie pour eux.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: CIM_ElementSetting, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514752"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="532ea-103">CIM_ElementSetting, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="532ea-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="532ea-104">La classe **CIM \_ ElementSetting** représente l’association entre les éléments système gérés et la classe de paramètres définie pour eux.</span><span class="sxs-lookup"><span data-stu-id="532ea-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="532ea-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="532ea-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="532ea-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="532ea-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="532ea-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="532ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="532ea-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="532ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="532ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="532ea-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="532ea-110">Membres</span><span class="sxs-lookup"><span data-stu-id="532ea-110">Members</span></span>

<span data-ttu-id="532ea-111">La classe **CIM \_ ElementSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="532ea-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="532ea-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="532ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="532ea-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="532ea-113">Properties</span></span>

<span data-ttu-id="532ea-114">La classe **CIM \_ ElementSetting** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="532ea-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="532ea-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="532ea-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="532ea-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="532ea-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="532ea-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="532ea-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="532ea-118">Référence au rôle de l’objet [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) de l’Association **CIM \_ ElementSetting** .</span><span class="sxs-lookup"><span data-stu-id="532ea-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="532ea-119">L’élément système managé associé fournit l’élément qui implémente le paramètre de l’élément.</span><span class="sxs-lookup"><span data-stu-id="532ea-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="532ea-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="532ea-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="532ea-121">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="532ea-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="532ea-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="532ea-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="532ea-123">Référence au rôle de l’objet [**de \_ paramètre CIM**](cim-setting.md) de l' **Association \_ CIM ElementSetting** .</span><span class="sxs-lookup"><span data-stu-id="532ea-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="532ea-124">Le paramètre associé fournit le paramètre qui implémente le paramètre de l’élément.</span><span class="sxs-lookup"><span data-stu-id="532ea-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="532ea-125">Notes</span><span class="sxs-lookup"><span data-stu-id="532ea-125">Remarks</span></span>

<span data-ttu-id="532ea-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="532ea-126">WMI does not implement this class.</span></span> <span data-ttu-id="532ea-127">Pour les classes dérivées de **CIM \_ ElementSetting**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="532ea-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="532ea-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="532ea-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="532ea-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="532ea-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="532ea-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="532ea-130">Requirements</span></span>



| <span data-ttu-id="532ea-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="532ea-131">Requirement</span></span> | <span data-ttu-id="532ea-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="532ea-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="532ea-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="532ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="532ea-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="532ea-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="532ea-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="532ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="532ea-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="532ea-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="532ea-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="532ea-137">Namespace</span></span><br/>                | <span data-ttu-id="532ea-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="532ea-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="532ea-139">MOF</span><span class="sxs-lookup"><span data-stu-id="532ea-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="532ea-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="532ea-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="532ea-141">DLL</span><span class="sxs-lookup"><span data-stu-id="532ea-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="532ea-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="532ea-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




