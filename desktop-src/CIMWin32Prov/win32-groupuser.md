---
description: La \_ classe WMI de l’Association GroupUser Win32 associe un groupe et un compte qui est membre de ce groupe.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Classe Win32_GroupUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483697"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="9716c-103">\_Classe GroupUser Win32</span><span class="sxs-lookup"><span data-stu-id="9716c-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="9716c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ GroupUser Win32** associe un groupe et un compte qui est membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="9716c-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="9716c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9716c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9716c-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9716c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9716c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9716c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9716c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9716c-108">Members</span></span>

<span data-ttu-id="9716c-109">La classe **Win32 \_ GroupUser** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9716c-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="9716c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9716c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9716c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9716c-111">Properties</span></span>

<span data-ttu-id="9716c-112">La classe **Win32 \_ GroupUser** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9716c-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9716c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9716c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9716c-114">Type de données **: \_ groupe Win32**</span><span class="sxs-lookup"><span data-stu-id="9716c-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="9716c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9716c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9716c-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| groupe Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="9716c-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="9716c-117">Référence à l’instance représentant le groupe dont le compte est membre.</span><span class="sxs-lookup"><span data-stu-id="9716c-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="9716c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9716c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9716c-119">Type de données **: \_ compte Win32**</span><span class="sxs-lookup"><span data-stu-id="9716c-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="9716c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9716c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9716c-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« PartComponent »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| compte Win32 WMI \_ »)</span><span class="sxs-lookup"><span data-stu-id="9716c-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="9716c-122">Référence à l’instance représentant l’utilisateur ou le compte système qui fait partie d’un groupe de comptes.</span><span class="sxs-lookup"><span data-stu-id="9716c-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9716c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9716c-123">Remarks</span></span>

<span data-ttu-id="9716c-124">La classe **Win32 \_ GroupUser** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="9716c-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9716c-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="9716c-125">Examples</span></span>

<span data-ttu-id="9716c-126">Pour obtenir un exemple PowerShell d’utilisation de Win32 \_ GroupUser pour récupérer la liste des membres d’un groupe local, consultez l' [exemple répertorier les membres du groupe local sur un ordinateur distant à l’aide de WMI et PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) dans la Galerie technet.</span><span class="sxs-lookup"><span data-stu-id="9716c-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="9716c-127">L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **Win32 \_ GroupUser** pour extraire les informations utilisateur d’un certain nombre d’ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="9716c-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9716c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9716c-128">Requirements</span></span>



| <span data-ttu-id="9716c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9716c-129">Requirement</span></span> | <span data-ttu-id="9716c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9716c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9716c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9716c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9716c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9716c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9716c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9716c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9716c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9716c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9716c-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9716c-135">Namespace</span></span><br/>                | <span data-ttu-id="9716c-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9716c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9716c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9716c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9716c-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9716c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9716c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9716c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9716c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9716c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9716c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9716c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9716c-142">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="9716c-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="9716c-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9716c-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

