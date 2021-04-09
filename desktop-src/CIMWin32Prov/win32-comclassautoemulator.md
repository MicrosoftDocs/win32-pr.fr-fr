---
description: La \_ classe WMI de l’Association Win32 ComClassAutoEmulator lie une classe com (Component Object Model) et une autre classe com émulée automatiquement.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Classe Win32_ComClassAutoEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111230"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="96c51-103">\_Classe ComClassAutoEmulator Win32</span><span class="sxs-lookup"><span data-stu-id="96c51-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="96c51-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **Win32 \_ COMCLASSAUTOEMULATOR** lie une classe com (Component Object Model) et une autre classe com émulée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="96c51-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="96c51-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="96c51-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="96c51-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="96c51-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c51-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96c51-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="96c51-108">Membres</span><span class="sxs-lookup"><span data-stu-id="96c51-108">Members</span></span>

<span data-ttu-id="96c51-109">La classe **Win32 \_ ComClassAutoEmulator** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="96c51-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="96c51-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96c51-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96c51-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96c51-111">Properties</span></span>

<span data-ttu-id="96c51-112">La classe **Win32 \_ ComClassAutoEmulator** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="96c51-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96c51-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="96c51-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c51-114">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="96c51-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="96c51-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96c51-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c51-116">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="96c51-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="96c51-117">Référence à l’instance représentant le composant COM qui peut émuler automatiquement le composant COM associé.</span><span class="sxs-lookup"><span data-stu-id="96c51-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="96c51-118">Ces informations sont obtenues par le biais de l’entrée de Registre AutoTreatAs.</span><span class="sxs-lookup"><span data-stu-id="96c51-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="96c51-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="96c51-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c51-120">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="96c51-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="96c51-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96c51-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c51-122">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="96c51-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="96c51-123">Référence à l’instance représentant le composant COM qui est automatiquement émulé par un autre composant.</span><span class="sxs-lookup"><span data-stu-id="96c51-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96c51-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96c51-124">Requirements</span></span>



| <span data-ttu-id="96c51-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96c51-125">Requirement</span></span> | <span data-ttu-id="96c51-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="96c51-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c51-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96c51-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96c51-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96c51-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96c51-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96c51-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96c51-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96c51-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96c51-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96c51-131">Namespace</span></span><br/>                | <span data-ttu-id="96c51-132">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="96c51-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96c51-133">MOF</span><span class="sxs-lookup"><span data-stu-id="96c51-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96c51-134"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96c51-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96c51-135">DLL</span><span class="sxs-lookup"><span data-stu-id="96c51-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c51-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c51-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c51-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96c51-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="96c51-138">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96c51-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

