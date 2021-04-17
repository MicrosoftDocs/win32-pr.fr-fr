---
description: L' \_ Association de sous-session Win32 définit des relations entre les sessions dans lesquelles une session fait partie d’une autre session ou utilise une autre session, par exemple lorsqu’une session Terminal Server utilise une session de connexion.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Classe Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524087"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="a5e09-103">\_Classe de sous-session Win32</span><span class="sxs-lookup"><span data-stu-id="a5e09-103">Win32\_SubSession class</span></span>

<span data-ttu-id="a5e09-104">L' \_ Association de sous-session Win32 définit des relations entre les sessions dans lesquelles une session fait partie d’une autre session ou utilise une autre session, par exemple lorsqu’une session Terminal Server utilise une session de connexion.</span><span class="sxs-lookup"><span data-stu-id="a5e09-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="a5e09-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a5e09-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e09-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5e09-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a5e09-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a5e09-107">Members</span></span>

<span data-ttu-id="a5e09-108">La classe de sous- **\_ session Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a5e09-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="a5e09-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5e09-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5e09-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5e09-110">Properties</span></span>

<span data-ttu-id="a5e09-111">La classe de sous- **\_ session Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a5e09-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5e09-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="a5e09-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e09-113">Type de données **: \_ session Win32**</span><span class="sxs-lookup"><span data-stu-id="a5e09-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="a5e09-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5e09-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5e09-115">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="a5e09-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="a5e09-116">[**\_ Session Win32**](win32-session.md) qui décrit la session qui a une sous-session.</span><span class="sxs-lookup"><span data-stu-id="a5e09-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="a5e09-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="a5e09-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e09-118">Type de données **: \_ session Win32**</span><span class="sxs-lookup"><span data-stu-id="a5e09-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="a5e09-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5e09-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5e09-120">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (Dependent)</span><span class="sxs-lookup"><span data-stu-id="a5e09-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="a5e09-121">[**\_ Session Win32**](win32-session.md) qui décrit la session qui est la sous-session.</span><span class="sxs-lookup"><span data-stu-id="a5e09-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5e09-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5e09-122">Requirements</span></span>



| <span data-ttu-id="a5e09-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5e09-123">Requirement</span></span> | <span data-ttu-id="a5e09-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5e09-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e09-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e09-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5e09-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5e09-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e09-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5e09-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5e09-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5e09-129">Namespace</span></span><br/>                | <span data-ttu-id="a5e09-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a5e09-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5e09-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a5e09-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5e09-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5e09-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5e09-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e09-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5e09-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e09-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5e09-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5e09-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e09-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="a5e09-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
