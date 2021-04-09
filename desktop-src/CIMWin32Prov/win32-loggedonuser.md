---
description: La \_ classe WMI de l’Association LoggedOnUser Win32 lie une session et un compte d’utilisateur.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Classe Win32_LoggedOnUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861590"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="47448-103">\_Classe LoggedOnUser Win32</span><span class="sxs-lookup"><span data-stu-id="47448-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="47448-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LoggedOnUser Win32** lie une session et un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47448-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="47448-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="47448-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="47448-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="47448-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47448-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47448-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="47448-108">Membres</span><span class="sxs-lookup"><span data-stu-id="47448-108">Members</span></span>

<span data-ttu-id="47448-109">La classe **Win32 \_ LoggedOnUser** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="47448-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="47448-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="47448-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47448-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="47448-111">Properties</span></span>

<span data-ttu-id="47448-112">La classe **Win32 \_ LoggedOnUser** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="47448-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47448-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="47448-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47448-114">Type de données **: \_ compte Win32**</span><span class="sxs-lookup"><span data-stu-id="47448-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="47448-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="47448-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47448-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47448-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47448-117">[**\_ Compte Win32**](win32-account.md) qui décrit le compte utilisé lors de l’initiation de cette session.</span><span class="sxs-lookup"><span data-stu-id="47448-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="47448-118">Le compte peut être un compte d’utilisateur ou un compte système.</span><span class="sxs-lookup"><span data-stu-id="47448-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="47448-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="47448-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47448-120">Type de données : **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="47448-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="47448-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="47448-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47448-122">Qualificateurs : [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (dépendant), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47448-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47448-123">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) qui décrit la session actuellement utilisée par le compte.</span><span class="sxs-lookup"><span data-stu-id="47448-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47448-124">Notes</span><span class="sxs-lookup"><span data-stu-id="47448-124">Remarks</span></span>

<span data-ttu-id="47448-125">La classe **Win32 \_ LoggedOnUser** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="47448-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47448-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="47448-126">Examples</span></span>

<span data-ttu-id="47448-127">L’exemple PowerShell de [fonction loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) obtient les utilisateurs connectés sur un ordinateur local ou distant, avec les informations de session.</span><span class="sxs-lookup"><span data-stu-id="47448-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="47448-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47448-128">Requirements</span></span>



| <span data-ttu-id="47448-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47448-129">Requirement</span></span> | <span data-ttu-id="47448-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="47448-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47448-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47448-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47448-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47448-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47448-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47448-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47448-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47448-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47448-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="47448-135">Namespace</span></span><br/>                | <span data-ttu-id="47448-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="47448-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47448-137">MOF</span><span class="sxs-lookup"><span data-stu-id="47448-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47448-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47448-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47448-139">DLL</span><span class="sxs-lookup"><span data-stu-id="47448-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47448-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47448-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47448-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47448-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47448-142">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="47448-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="47448-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47448-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

