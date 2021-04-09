---
description: La \_ classe WMI de l’Association ComClassEmulator Win32 associe deux versions d’une classe com (Component Object Model).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Classe Win32_ComClassEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110239"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="5f64e-103">\_Classe ComClassEmulator Win32</span><span class="sxs-lookup"><span data-stu-id="5f64e-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="5f64e-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ ComClassEmulator Win32** associe deux versions d’une classe com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="5f64e-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="5f64e-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5f64e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5f64e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5f64e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f64e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f64e-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="5f64e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5f64e-108">Members</span></span>

<span data-ttu-id="5f64e-109">La classe **Win32 \_ ComClassEmulator** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f64e-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="5f64e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f64e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f64e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f64e-111">Properties</span></span>

<span data-ttu-id="5f64e-112">La classe **Win32 \_ ComClassEmulator** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5f64e-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f64e-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="5f64e-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f64e-114">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="5f64e-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="5f64e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f64e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f64e-116">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="5f64e-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="5f64e-117">Référence à l’instance représentant le composant COM qui contient des interfaces émulant l’ancienne version du composant.</span><span class="sxs-lookup"><span data-stu-id="5f64e-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="5f64e-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="5f64e-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f64e-119">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="5f64e-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="5f64e-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f64e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f64e-121">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="5f64e-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="5f64e-122">Référence à l’instance représentant le composant COM avec des interfaces qui peuvent être émulées par la nouvelle version du composant.</span><span class="sxs-lookup"><span data-stu-id="5f64e-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f64e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f64e-123">Requirements</span></span>



| <span data-ttu-id="5f64e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f64e-124">Requirement</span></span> | <span data-ttu-id="5f64e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f64e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f64e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f64e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f64e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f64e-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f64e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f64e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f64e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f64e-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f64e-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f64e-130">Namespace</span></span><br/>                | <span data-ttu-id="5f64e-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5f64e-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f64e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5f64e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f64e-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f64e-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f64e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5f64e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f64e-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f64e-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f64e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f64e-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f64e-137">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f64e-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

