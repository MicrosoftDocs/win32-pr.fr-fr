---
title: Classe Win32_RDMSDesktopAssignment
description: Décrit l’attribution de bureau de l’utilisateur de la collection des services Bureau à distance.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317238"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="e55cb-105">\_Classe RDMSDesktopAssignment Win32</span><span class="sxs-lookup"><span data-stu-id="e55cb-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="e55cb-106">Décrit l’attribution de bureau de l’utilisateur de la collection des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e55cb-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="e55cb-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e55cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e55cb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e55cb-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="e55cb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e55cb-109">Members</span></span>

<span data-ttu-id="e55cb-110">La classe **Win32 \_ RDMSDesktopAssignment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e55cb-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="e55cb-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e55cb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e55cb-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e55cb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e55cb-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e55cb-113">Methods</span></span>

<span data-ttu-id="e55cb-114">La classe **Win32 \_ RDMSDesktopAssignment** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e55cb-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="e55cb-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e55cb-115">Method</span></span>                                                                                 | <span data-ttu-id="e55cb-116">Description</span><span class="sxs-lookup"><span data-stu-id="e55cb-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="e55cb-117">**AddDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="e55cb-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="e55cb-118">Ajoute une attribution de bureau.</span><span class="sxs-lookup"><span data-stu-id="e55cb-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="e55cb-119">**RemoveDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="e55cb-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="e55cb-120">Supprime une attribution de bureau.</span><span class="sxs-lookup"><span data-stu-id="e55cb-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e55cb-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e55cb-121">Properties</span></span>

<span data-ttu-id="e55cb-122">La classe **Win32 \_ RDMSDesktopAssignment** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e55cb-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e55cb-123">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="e55cb-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55cb-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e55cb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e55cb-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e55cb-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e55cb-127">Alias de la collection.</span><span class="sxs-lookup"><span data-stu-id="e55cb-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="e55cb-128">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="e55cb-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55cb-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e55cb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e55cb-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e55cb-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e55cb-132">Nom du bureau.</span><span class="sxs-lookup"><span data-stu-id="e55cb-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e55cb-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="e55cb-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55cb-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e55cb-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e55cb-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-136">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e55cb-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e55cb-137">Nom de domaine du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e55cb-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e55cb-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="e55cb-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55cb-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e55cb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e55cb-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e55cb-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e55cb-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e55cb-142">Nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e55cb-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e55cb-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e55cb-143">Requirements</span></span>



| <span data-ttu-id="e55cb-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e55cb-144">Requirement</span></span> | <span data-ttu-id="e55cb-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="e55cb-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55cb-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e55cb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e55cb-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e55cb-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e55cb-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e55cb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e55cb-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e55cb-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e55cb-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e55cb-150">Namespace</span></span><br/>                | <span data-ttu-id="e55cb-151">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="e55cb-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e55cb-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e55cb-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e55cb-153"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e55cb-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e55cb-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e55cb-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e55cb-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e55cb-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

