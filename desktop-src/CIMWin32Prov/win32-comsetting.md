---
description: La \_ classe WMI abstraite de paramètres Win32 représente les paramètres associés à un composant COM (Component Object Model) ou à une application com.
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Classe Win32_COMSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200914"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="d75ed-103">\_Classe de Comdéfinition Win32</span><span class="sxs-lookup"><span data-stu-id="d75ed-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="d75ed-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstraite de paramètres **Win32 \_** représente les paramètres associés à un composant COM (Component Object Model) ou à une application com.</span><span class="sxs-lookup"><span data-stu-id="d75ed-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="d75ed-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d75ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d75ed-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d75ed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75ed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d75ed-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="d75ed-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d75ed-108">Members</span></span>

<span data-ttu-id="d75ed-109">La classe de **\_ paramètres Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d75ed-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d75ed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d75ed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d75ed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d75ed-111">Properties</span></span>

<span data-ttu-id="d75ed-112">La classe de **\_ paramètres Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d75ed-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d75ed-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d75ed-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75ed-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d75ed-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75ed-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d75ed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d75ed-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d75ed-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d75ed-117">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="d75ed-117">Short textual description of the current object.</span></span>

<span data-ttu-id="d75ed-118">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d75ed-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d75ed-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="d75ed-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75ed-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d75ed-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75ed-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d75ed-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d75ed-122">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="d75ed-122">Textual description of the current object.</span></span>

<span data-ttu-id="d75ed-123">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d75ed-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d75ed-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="d75ed-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75ed-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d75ed-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75ed-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d75ed-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d75ed-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d75ed-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d75ed-128">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="d75ed-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="d75ed-129">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d75ed-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d75ed-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d75ed-130">Remarks</span></span>

<span data-ttu-id="d75ed-131">La classe de **\_ comdéfinition Win32** est dérivée du [**\_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d75ed-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d75ed-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d75ed-132">Requirements</span></span>



| <span data-ttu-id="d75ed-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d75ed-133">Requirement</span></span> | <span data-ttu-id="d75ed-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75ed-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75ed-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d75ed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d75ed-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d75ed-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d75ed-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d75ed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d75ed-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d75ed-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d75ed-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d75ed-139">Namespace</span></span><br/>                | <span data-ttu-id="d75ed-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d75ed-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d75ed-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d75ed-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d75ed-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d75ed-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d75ed-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d75ed-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d75ed-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75ed-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75ed-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d75ed-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75ed-146">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="d75ed-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="d75ed-147">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d75ed-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

