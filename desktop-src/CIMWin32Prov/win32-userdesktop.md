---
description: La \_ classe WMI de l’Association UserDesktop Win32 associe un compte d’utilisateur et des paramètres de bureau qui lui sont spécifiques.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Classe Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860822"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="6a993-103">\_Classe UserDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="6a993-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="6a993-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ UserDesktop Win32** associe un compte d’utilisateur et des paramètres de bureau qui lui sont spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6a993-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="6a993-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6a993-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6a993-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6a993-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a993-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a993-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6a993-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6a993-108">Members</span></span>

<span data-ttu-id="6a993-109">La classe **Win32 \_ UserDesktop** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a993-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="6a993-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a993-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a993-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a993-111">Properties</span></span>

<span data-ttu-id="6a993-112">La classe **Win32 \_ UserDesktop** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6a993-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a993-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a993-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a993-114">Type de données : **Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="6a993-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="6a993-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a993-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a993-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")</span><span class="sxs-lookup"><span data-stu-id="6a993-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="6a993-117">Référence à l’instance de qui représente le compte d’utilisateur dont le Bureau peut être personnalisé par la propriété de **paramètres** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6a993-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="6a993-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="6a993-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a993-119">Type de données **: \_ Bureau Win32**</span><span class="sxs-lookup"><span data-stu-id="6a993-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="6a993-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a993-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a993-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="6a993-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="6a993-122">Référence à l’instance représentant les paramètres de bureau qui servent à personnaliser un bureau de compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a993-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a993-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6a993-123">Remarks</span></span>

<span data-ttu-id="6a993-124">La classe **Win32 \_ UserDesktop** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="6a993-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a993-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a993-125">Requirements</span></span>



| <span data-ttu-id="6a993-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a993-126">Requirement</span></span> | <span data-ttu-id="6a993-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a993-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a993-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a993-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a993-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a993-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a993-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a993-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a993-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a993-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a993-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a993-132">Namespace</span></span><br/>                | <span data-ttu-id="6a993-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6a993-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a993-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6a993-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a993-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a993-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a993-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6a993-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a993-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a993-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a993-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a993-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a993-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="6a993-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="6a993-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6a993-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
