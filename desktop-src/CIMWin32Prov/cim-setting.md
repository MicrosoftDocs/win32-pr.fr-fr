---
description: La \_ classe de paramètres CIM représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: CIM_Setting, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861021"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="49db8-103">CIM_Setting, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="49db8-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="49db8-104">La classe de **\_ paramètres CIM** représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="49db8-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="49db8-105">Plusieurs objets de paramètre peuvent être associés à un élément système géré.</span><span class="sxs-lookup"><span data-stu-id="49db8-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="49db8-106">Les valeurs opérationnelles actuelles des paramètres d’un élément sont reflétées par les propriétés de l’élément lui-même ou par les propriétés de ses associations.</span><span class="sxs-lookup"><span data-stu-id="49db8-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="49db8-107">Il n’est pas nécessaire que ces propriétés soient les mêmes que celles présentes dans l’objet de paramètre.</span><span class="sxs-lookup"><span data-stu-id="49db8-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="49db8-108">Par exemple, un modem peut avoir un paramètre d’une vitesse de transmission de 56 kilo-octets par seconde, mais doit fonctionner à 19,2 kilo-octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="49db8-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49db8-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="49db8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49db8-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="49db8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49db8-111">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="49db8-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="49db8-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="49db8-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49db8-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49db8-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="49db8-114">Membres</span><span class="sxs-lookup"><span data-stu-id="49db8-114">Members</span></span>

<span data-ttu-id="49db8-115">La classe de **\_ paramètres CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49db8-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="49db8-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49db8-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49db8-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49db8-117">Properties</span></span>

<span data-ttu-id="49db8-118">La classe de **\_ paramètres CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="49db8-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49db8-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="49db8-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49db8-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49db8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49db8-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49db8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49db8-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="49db8-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="49db8-123">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="49db8-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="49db8-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="49db8-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49db8-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49db8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49db8-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49db8-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49db8-127">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="49db8-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="49db8-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="49db8-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49db8-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49db8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49db8-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49db8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49db8-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49db8-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49db8-132">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="49db8-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49db8-133">Notes</span><span class="sxs-lookup"><span data-stu-id="49db8-133">Remarks</span></span>

<span data-ttu-id="49db8-134">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="49db8-134">WMI does not implement this class.</span></span> <span data-ttu-id="49db8-135">Pour les classes WMI dérivées du **\_ paramètre CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="49db8-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="49db8-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="49db8-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49db8-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="49db8-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49db8-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49db8-138">Requirements</span></span>



| <span data-ttu-id="49db8-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49db8-139">Requirement</span></span> | <span data-ttu-id="49db8-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="49db8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49db8-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49db8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="49db8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49db8-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49db8-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49db8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="49db8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49db8-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49db8-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49db8-145">Namespace</span></span><br/>                | <span data-ttu-id="49db8-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="49db8-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49db8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="49db8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49db8-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49db8-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49db8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="49db8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49db8-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49db8-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

