---
description: L' \_ Association Win32 SessionResource représente la relation entre une session et les ressources auxquelles la session donne accès.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Classe Win32_SessionResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748788"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="6dd00-103">\_Classe SessionResource Win32</span><span class="sxs-lookup"><span data-stu-id="6dd00-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="6dd00-104">L' \_ Association Win32 SessionResource représente la relation entre une session et les ressources auxquelles la session donne accès.</span><span class="sxs-lookup"><span data-stu-id="6dd00-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="6dd00-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6dd00-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd00-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dd00-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6dd00-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6dd00-107">Members</span></span>

<span data-ttu-id="6dd00-108">La classe **Win32 \_ SessionResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6dd00-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6dd00-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6dd00-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dd00-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6dd00-110">Properties</span></span>

<span data-ttu-id="6dd00-111">La classe **Win32 \_ SessionResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6dd00-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dd00-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6dd00-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd00-113">Type de données : **Win32 \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="6dd00-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="6dd00-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6dd00-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dd00-115">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6dd00-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6dd00-116">La référence Antecedent représente les ressources utilisées par cette session.</span><span class="sxs-lookup"><span data-stu-id="6dd00-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="6dd00-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6dd00-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd00-118">Type de données **: \_ session Win32**</span><span class="sxs-lookup"><span data-stu-id="6dd00-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="6dd00-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6dd00-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dd00-120">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="6dd00-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6dd00-121">La référence dépendante représente la session utilisant la ressource.</span><span class="sxs-lookup"><span data-stu-id="6dd00-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dd00-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dd00-122">Requirements</span></span>



| <span data-ttu-id="6dd00-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6dd00-123">Requirement</span></span> | <span data-ttu-id="6dd00-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dd00-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd00-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dd00-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd00-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dd00-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6dd00-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dd00-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd00-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dd00-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6dd00-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6dd00-129">Namespace</span></span><br/>                | <span data-ttu-id="6dd00-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6dd00-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6dd00-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6dd00-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dd00-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dd00-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dd00-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd00-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd00-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd00-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dd00-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dd00-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd00-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6dd00-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
