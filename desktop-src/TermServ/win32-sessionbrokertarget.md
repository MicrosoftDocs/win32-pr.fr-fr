---
title: Classe Win32_SessionBrokerTarget
description: Définit la requête pour une cible session Broker.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTarget de la classe Services Bureau à distance
- Win32_SessionBrokerTarget de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844302"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="abfd5-105">\_Classe SessionBrokerTarget Win32</span><span class="sxs-lookup"><span data-stu-id="abfd5-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="abfd5-106">Définit la requête pour une cible session Broker.</span><span class="sxs-lookup"><span data-stu-id="abfd5-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="abfd5-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="abfd5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfd5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abfd5-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="abfd5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="abfd5-109">Members</span></span>

<span data-ttu-id="abfd5-110">La classe **Win32 \_ SessionBrokerTarget** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="abfd5-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="abfd5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abfd5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abfd5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abfd5-112">Properties</span></span>

<span data-ttu-id="abfd5-113">La classe **Win32 \_ SessionBrokerTarget** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="abfd5-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abfd5-114">**Environment**</span><span class="sxs-lookup"><span data-stu-id="abfd5-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abfd5-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abfd5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abfd5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abfd5-117">Nom d'environnement.</span><span class="sxs-lookup"><span data-stu-id="abfd5-117">The environment name.</span></span> <span data-ttu-id="abfd5-118">Dans le cas d’une machine virtuelle (VM) cible, il peut s’agir du nom d’hôte de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="abfd5-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-119">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="abfd5-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abfd5-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abfd5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abfd5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abfd5-122">Nom de la batterie à laquelle la cible appartient.</span><span class="sxs-lookup"><span data-stu-id="abfd5-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-123">**Uniques**</span><span class="sxs-lookup"><span data-stu-id="abfd5-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abfd5-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abfd5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abfd5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="abfd5-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="abfd5-127">GUID (le cas échéant) de la cible.</span><span class="sxs-lookup"><span data-stu-id="abfd5-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="abfd5-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abfd5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abfd5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abfd5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="abfd5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="abfd5-132">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="abfd5-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="abfd5-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abfd5-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abfd5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abfd5-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abfd5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abfd5-136">Nom de la cible.</span><span class="sxs-lookup"><span data-stu-id="abfd5-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="abfd5-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="abfd5-137">Examples</span></span>

<span data-ttu-id="abfd5-138">La chaîne de requête suivante montre comment la \_ classe SessionBrokerTarget Win32 est utilisée dans une requête.</span><span class="sxs-lookup"><span data-stu-id="abfd5-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="abfd5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abfd5-139">Requirements</span></span>



| <span data-ttu-id="abfd5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abfd5-140">Requirement</span></span> | <span data-ttu-id="abfd5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="abfd5-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abfd5-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abfd5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="abfd5-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="abfd5-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="abfd5-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abfd5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="abfd5-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="abfd5-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="abfd5-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="abfd5-146">Namespace</span></span><br/>                | <span data-ttu-id="abfd5-147">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="abfd5-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="abfd5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="abfd5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abfd5-149"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abfd5-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="abfd5-150">DLL</span><span class="sxs-lookup"><span data-stu-id="abfd5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abfd5-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abfd5-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

