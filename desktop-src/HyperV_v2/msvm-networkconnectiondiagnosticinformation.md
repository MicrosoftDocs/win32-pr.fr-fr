---
description: Fournit des informations sur la connectivité réseau pour un ordinateur virtuel.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Classe Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952962"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="46952-103">MSVM \_ NetworkConnectionDiagnosticInformation, classe</span><span class="sxs-lookup"><span data-stu-id="46952-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="46952-104">Fournit des informations sur la connectivité réseau pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="46952-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="46952-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="46952-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46952-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46952-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="46952-107">Membres</span><span class="sxs-lookup"><span data-stu-id="46952-107">Members</span></span>

<span data-ttu-id="46952-108">La classe **MSVM \_ NetworkConnectionDiagnosticInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46952-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="46952-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46952-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46952-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46952-110">Properties</span></span>

<span data-ttu-id="46952-111">La classe **MSVM \_ NetworkConnectionDiagnosticInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="46952-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46952-112">**RoundTripTime**</span><span class="sxs-lookup"><span data-stu-id="46952-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46952-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46952-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46952-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46952-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46952-115">Durée aller-retour pour la demande Ping.</span><span class="sxs-lookup"><span data-stu-id="46952-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46952-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46952-116">Requirements</span></span>



| <span data-ttu-id="46952-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46952-117">Requirement</span></span> | <span data-ttu-id="46952-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="46952-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46952-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46952-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46952-120">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46952-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46952-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46952-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46952-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="46952-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="46952-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46952-123">Namespace</span></span><br/>                | <span data-ttu-id="46952-124">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="46952-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46952-125">MOF</span><span class="sxs-lookup"><span data-stu-id="46952-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46952-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46952-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46952-127">DLL</span><span class="sxs-lookup"><span data-stu-id="46952-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46952-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46952-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




