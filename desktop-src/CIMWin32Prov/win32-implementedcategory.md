---
description: La \_ classe WMI de l’Association ImplementedCategory Win32 associe une catégorie de composant et la classe com (Component Object Model) à l’aide de ses interfaces.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Classe Win32_ImplementedCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749013"
---
# <a name="win32_implementedcategory-class"></a><span data-ttu-id="0a54a-103">\_Classe ImplementedCategory Win32</span><span class="sxs-lookup"><span data-stu-id="0a54a-103">Win32\_ImplementedCategory class</span></span>

<span data-ttu-id="0a54a-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ ImplementedCategory Win32** associe une catégorie de composant et la classe com (Component Object Model) à l’aide de ses interfaces.</span><span class="sxs-lookup"><span data-stu-id="0a54a-104">The **Win32\_ImplementedCategory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a component category and the Component Object Model (COM) class using its interfaces.</span></span>

<span data-ttu-id="0a54a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0a54a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0a54a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0a54a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a54a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a54a-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a><span data-ttu-id="0a54a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0a54a-108">Members</span></span>

<span data-ttu-id="0a54a-109">La classe **Win32 \_ ImplementedCategory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a54a-109">The **Win32\_ImplementedCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="0a54a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a54a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a54a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a54a-111">Properties</span></span>

<span data-ttu-id="0a54a-112">La classe **Win32 \_ ImplementedCategory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0a54a-112">The **Win32\_ImplementedCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a54a-113">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="0a54a-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54a-114">Type de données : **Win32 \_ ComponentCategory**</span><span class="sxs-lookup"><span data-stu-id="0a54a-114">Data type: **Win32\_ComponentCategory**</span></span>
</dt> <dt>

<span data-ttu-id="0a54a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a54a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a54a-116">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComponentCategory")</span><span class="sxs-lookup"><span data-stu-id="0a54a-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComponentCategory")</span></span>
</dt> </dl>

<span data-ttu-id="0a54a-117">Référence à l’instance représentant la catégorie de composant utilisée par la classe COM.</span><span class="sxs-lookup"><span data-stu-id="0a54a-117">Reference to the instance representing the component category being used by the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="0a54a-118">**Composant**</span><span class="sxs-lookup"><span data-stu-id="0a54a-118">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54a-119">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="0a54a-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="0a54a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a54a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a54a-121">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="0a54a-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="0a54a-122">Référence à l’instance représentant la classe COM à l’aide de la catégorie associée.</span><span class="sxs-lookup"><span data-stu-id="0a54a-122">Reference to the instance representing the COM class using the associated category.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a54a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a54a-123">Requirements</span></span>



| <span data-ttu-id="0a54a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a54a-124">Requirement</span></span> | <span data-ttu-id="0a54a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a54a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a54a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a54a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a54a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a54a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a54a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a54a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a54a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a54a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a54a-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a54a-130">Namespace</span></span><br/>                | <span data-ttu-id="0a54a-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0a54a-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a54a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0a54a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a54a-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a54a-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a54a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0a54a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a54a-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a54a-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a54a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a54a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a54a-137">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a54a-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

