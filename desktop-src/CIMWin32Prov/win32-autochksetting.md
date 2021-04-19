---
description: La \_ classe WMI Win32 AutochkSetting représente les paramètres de l’opération de vérification de la validation d’un disque.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Classe Win32_AutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516584"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="77dc2-103">\_Classe AutochkSetting Win32</span><span class="sxs-lookup"><span data-stu-id="77dc2-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="77dc2-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ AutochkSetting** représente les paramètres de l’opération de vérification de la validation d’un disque.</span><span class="sxs-lookup"><span data-stu-id="77dc2-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="77dc2-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="77dc2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="77dc2-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="77dc2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77dc2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77dc2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="77dc2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="77dc2-108">Members</span></span>

<span data-ttu-id="77dc2-109">La classe **Win32 \_ AutochkSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77dc2-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="77dc2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77dc2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77dc2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77dc2-111">Properties</span></span>

<span data-ttu-id="77dc2-112">La classe **Win32 \_ AutochkSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="77dc2-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77dc2-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="77dc2-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77dc2-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77dc2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77dc2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="77dc2-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="77dc2-117">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="77dc2-117">Short textual description of the current object.</span></span>

<span data-ttu-id="77dc2-118">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="77dc2-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="77dc2-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="77dc2-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77dc2-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77dc2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77dc2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77dc2-122">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="77dc2-122">Textual description of the current object.</span></span>

<span data-ttu-id="77dc2-123">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="77dc2-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="77dc2-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="77dc2-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77dc2-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77dc2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77dc2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77dc2-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77dc2-128">ID utilisé dans le cadre d’une clé pour l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="77dc2-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="77dc2-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="77dc2-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77dc2-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77dc2-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="77dc2-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77dc2-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="77dc2-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="77dc2-133">Délai d’entrée utilisateur pour la vérification autoactive.</span><span class="sxs-lookup"><span data-stu-id="77dc2-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77dc2-134">Notes</span><span class="sxs-lookup"><span data-stu-id="77dc2-134">Remarks</span></span>

<span data-ttu-id="77dc2-135">La classe **Win32 \_ AutochkSetting** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="77dc2-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77dc2-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77dc2-136">Requirements</span></span>



| <span data-ttu-id="77dc2-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77dc2-137">Requirement</span></span> | <span data-ttu-id="77dc2-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="77dc2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc2-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77dc2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="77dc2-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77dc2-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77dc2-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77dc2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="77dc2-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77dc2-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77dc2-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77dc2-143">Namespace</span></span><br/>                | <span data-ttu-id="77dc2-144">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="77dc2-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77dc2-145">MOF</span><span class="sxs-lookup"><span data-stu-id="77dc2-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77dc2-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77dc2-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77dc2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="77dc2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77dc2-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77dc2-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77dc2-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77dc2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77dc2-150">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="77dc2-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="77dc2-151">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="77dc2-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

