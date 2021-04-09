---
description: La \_ classe WMI de l’Association ClassicCOMApplicationClasses Win32 lie une application com et un composant com groupé.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861518"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="ff431-103">\_Classe ClassicCOMApplicationClasses Win32</span><span class="sxs-lookup"><span data-stu-id="ff431-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="ff431-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ ClassicCOMApplicationClasses Win32** lie une application com et un composant com groupé.</span><span class="sxs-lookup"><span data-stu-id="ff431-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="ff431-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ff431-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ff431-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ff431-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff431-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff431-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ff431-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ff431-108">Members</span></span>

<span data-ttu-id="ff431-109">La classe **Win32 \_ ClassicCOMApplicationClasses** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ff431-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="ff431-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ff431-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff431-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ff431-111">Properties</span></span>

<span data-ttu-id="ff431-112">La classe **Win32 \_ ClassicCOMApplicationClasses** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ff431-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff431-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ff431-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff431-114">Type de données : **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="ff431-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="ff431-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ff431-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff431-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="ff431-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="ff431-117">[**\_ DCOMApplication Win32**](win32-dcomapplication.md) qui représente une application DCOM contenant ou utilisant le composant com.</span><span class="sxs-lookup"><span data-stu-id="ff431-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="ff431-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ff431-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff431-119">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="ff431-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="ff431-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ff431-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff431-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="ff431-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="ff431-122">[**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) qui représente le composant com existant dans ou utilisé par l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="ff431-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff431-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ff431-123">Remarks</span></span>

<span data-ttu-id="ff431-124">La classe **Win32 \_ ClassicCOMApplicationClasses** est dérivée de [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md).</span><span class="sxs-lookup"><span data-stu-id="ff431-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff431-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff431-125">Requirements</span></span>



| <span data-ttu-id="ff431-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff431-126">Requirement</span></span> | <span data-ttu-id="ff431-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff431-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff431-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff431-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff431-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff431-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff431-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff431-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff431-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff431-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff431-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ff431-132">Namespace</span></span><br/>                | <span data-ttu-id="ff431-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ff431-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff431-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ff431-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff431-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff431-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff431-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ff431-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff431-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff431-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff431-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff431-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff431-139">**\_COMApplicationClasses Win32**</span><span class="sxs-lookup"><span data-stu-id="ff431-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="ff431-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff431-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

