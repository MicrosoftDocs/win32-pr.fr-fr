---
title: Classe Win32_SessionBrokerFarm
description: Définit la requête pour une batterie de serveurs session Broker.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarm de la classe Services Bureau à distance
- Win32_SessionBrokerFarm de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465294"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="2f9f1-105">\_Classe SessionBrokerFarm Win32</span><span class="sxs-lookup"><span data-stu-id="2f9f1-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="2f9f1-106">Définit la requête pour une batterie de serveurs session Broker.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="2f9f1-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9f1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f9f1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="2f9f1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2f9f1-109">Members</span></span>

<span data-ttu-id="2f9f1-110">La classe **Win32 \_ SessionBrokerFarm** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f9f1-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="2f9f1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f9f1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f9f1-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f9f1-112">Properties</span></span>

<span data-ttu-id="2f9f1-113">La classe **Win32 \_ SessionBrokerFarm** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f9f1-114">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="2f9f1-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9f1-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f9f1-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9f1-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f9f1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f9f1-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f9f1-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f9f1-118">Nom de la batterie session Broker qui doit être interrogée.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="2f9f1-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="2f9f1-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9f1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f9f1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9f1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f9f1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f9f1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f9f1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f9f1-123">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2f9f1-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="2f9f1-124">Examples</span></span>

<span data-ttu-id="2f9f1-125">La chaîne de requête suivante montre comment la classe **\_ SessionBrokerFarm Win32** est utilisée dans une requête.</span><span class="sxs-lookup"><span data-stu-id="2f9f1-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="2f9f1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f9f1-126">Requirements</span></span>



| <span data-ttu-id="2f9f1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f9f1-127">Requirement</span></span> | <span data-ttu-id="2f9f1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f9f1-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9f1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f9f1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9f1-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f9f1-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2f9f1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f9f1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9f1-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f9f1-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="2f9f1-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2f9f1-133">Namespace</span></span><br/>                | <span data-ttu-id="2f9f1-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2f9f1-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="2f9f1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2f9f1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f9f1-136"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f1-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f9f1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2f9f1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f9f1-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f1-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

