---
title: Classe Win32_SessionDirectoryVirtualDesktopServer
description: Représente un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) joint à un service session Broker.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer de la classe Services Bureau à distance
- Win32_SessionDirectoryVirtualDesktopServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032578"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="7d86d-105">\_Classe SessionDirectoryVirtualDesktopServer Win32</span><span class="sxs-lookup"><span data-stu-id="7d86d-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="7d86d-106">Représente un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) joint à un service session Broker.</span><span class="sxs-lookup"><span data-stu-id="7d86d-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="7d86d-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7d86d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d86d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d86d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7d86d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7d86d-109">Members</span></span>

<span data-ttu-id="7d86d-110">La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7d86d-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="7d86d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d86d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d86d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d86d-112">Properties</span></span>

<span data-ttu-id="7d86d-113">La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7d86d-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d86d-114">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7d86d-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d86d-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7d86d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7d86d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d86d-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7d86d-118">Nom DNS du serveur hôte de virtualisation des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7d86d-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="7d86d-119">Ce nom se présente sous la forme «*MachineName*. *Domain*. com».</span><span class="sxs-lookup"><span data-stu-id="7d86d-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d86d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d86d-120">Requirements</span></span>



| <span data-ttu-id="7d86d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d86d-121">Requirement</span></span> | <span data-ttu-id="7d86d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d86d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d86d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d86d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7d86d-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d86d-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7d86d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d86d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7d86d-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d86d-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7d86d-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7d86d-127">Namespace</span></span><br/>                | <span data-ttu-id="7d86d-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7d86d-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="7d86d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7d86d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d86d-130"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d86d-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d86d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7d86d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d86d-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d86d-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

