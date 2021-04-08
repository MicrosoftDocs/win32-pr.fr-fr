---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contient les informations de configuration d’un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings de la classe Services Bureau à distance
- Win32_TSVirtualDesktopServerSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743268"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="a9231-105">\_Classe TSVirtualDesktopServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="a9231-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="a9231-106">Contient les informations de configuration d’un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="a9231-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="a9231-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a9231-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9231-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9231-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="a9231-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a9231-109">Members</span></span>

<span data-ttu-id="a9231-110">La classe **Win32 \_ TSVirtualDesktopServerSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9231-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="a9231-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9231-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9231-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9231-112">Properties</span></span>

<span data-ttu-id="a9231-113">La classe **Win32 \_ TSVirtualDesktopServerSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a9231-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9231-114">**Concurrency**</span><span class="sxs-lookup"><span data-stu-id="a9231-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9231-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9231-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9231-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a9231-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a9231-117">Nombre maximal de demandes de configuration simultanées autorisées pour ce serveur de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="a9231-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="a9231-118">**PolicySourceSessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="a9231-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9231-119">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="a9231-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9231-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9231-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9231-121">Si la valeur est 0, cela indique que la propriété **SessionBrokerName** est configurée par le serveur. Si la valeur est 1, cela indique que la propriété **SessionBrokerName** est configurée par une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a9231-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="a9231-122">**SessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="a9231-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9231-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9231-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9231-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a9231-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a9231-125">Nom unique du service session Broker pour le serveur hôte de virtualisation des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a9231-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9231-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9231-126">Requirements</span></span>



| <span data-ttu-id="a9231-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9231-127">Requirement</span></span> | <span data-ttu-id="a9231-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9231-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9231-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9231-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a9231-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9231-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a9231-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9231-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a9231-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9231-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a9231-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9231-133">Namespace</span></span><br/>                | <span data-ttu-id="a9231-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a9231-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="a9231-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a9231-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9231-136"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9231-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a9231-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a9231-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9231-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9231-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





