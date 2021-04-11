---
description: Cette classe représente l’association entre un système d’exploitation et les paramètres Autochk qui s’appliquent aux disques sur l’ordinateur. Notez que le paramètre est associé au système d’exploitation plutôt qu’au système informatique, car il peut y avoir un ou plusieurs systèmes d’exploitation installés sur l’ordinateur, chacun avec ses propres paramètres Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111350"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="6abba-103">\_Classe OperatingSystemAutochkSetting Win32</span><span class="sxs-lookup"><span data-stu-id="6abba-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="6abba-104">Cette classe représente l’association entre un système d’exploitation et les paramètres Autochk qui s’appliquent aux disques sur l’ordinateur. Notez que le paramètre est associé au système d’exploitation plutôt qu’au système informatique, car il peut y avoir un ou plusieurs systèmes d’exploitation installés sur l’ordinateur, chacun avec ses propres paramètres Autochk.</span><span class="sxs-lookup"><span data-stu-id="6abba-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="6abba-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6abba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abba-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6abba-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6abba-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6abba-107">Members</span></span>

<span data-ttu-id="6abba-108">La classe **Win32 \_ OperatingSystemAutochkSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6abba-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6abba-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6abba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6abba-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6abba-110">Properties</span></span>

<span data-ttu-id="6abba-111">La classe **Win32 \_ OperatingSystemAutochkSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6abba-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6abba-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="6abba-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6abba-113">Type de données : **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="6abba-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6abba-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6abba-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6abba-115">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6abba-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="6abba-116">TBD</span><span class="sxs-lookup"><span data-stu-id="6abba-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="6abba-117">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="6abba-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6abba-118">Type de données : **Win32 \_ AutochkSetting**</span><span class="sxs-lookup"><span data-stu-id="6abba-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="6abba-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6abba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6abba-120">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6abba-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="6abba-121">TBD</span><span class="sxs-lookup"><span data-stu-id="6abba-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6abba-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6abba-122">Requirements</span></span>



| <span data-ttu-id="6abba-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6abba-123">Requirement</span></span> | <span data-ttu-id="6abba-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6abba-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6abba-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6abba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6abba-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6abba-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6abba-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6abba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6abba-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6abba-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6abba-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6abba-129">Namespace</span></span><br/>                | <span data-ttu-id="6abba-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6abba-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6abba-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6abba-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6abba-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6abba-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6abba-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6abba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6abba-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abba-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abba-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6abba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abba-136">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="6abba-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
