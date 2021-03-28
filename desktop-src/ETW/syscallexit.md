---
description: Cette classe est la classe de type d’événement pour les événements de sortie d’appel système. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973410"
---
# <a name="syscallexit-class"></a><span data-ttu-id="14e6b-104">SysCallExit, classe</span><span class="sxs-lookup"><span data-stu-id="14e6b-104">SysCallExit class</span></span>

<span data-ttu-id="14e6b-105">Cette classe est la classe de type d’événement pour les événements de sortie d’appel système.</span><span class="sxs-lookup"><span data-stu-id="14e6b-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="14e6b-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="14e6b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e6b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14e6b-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="14e6b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="14e6b-108">Members</span></span>

<span data-ttu-id="14e6b-109">La classe **SysCallExit** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14e6b-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="14e6b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14e6b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14e6b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14e6b-111">Properties</span></span>

<span data-ttu-id="14e6b-112">La classe **SysCallExit** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="14e6b-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14e6b-113">**SysCallNtStatus**</span><span class="sxs-lookup"><span data-stu-id="14e6b-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14e6b-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14e6b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14e6b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14e6b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14e6b-116">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="14e6b-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="14e6b-117">Code d’état retourné par l’appel système NT.</span><span class="sxs-lookup"><span data-stu-id="14e6b-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14e6b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="14e6b-118">Requirements</span></span>



| <span data-ttu-id="14e6b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14e6b-119">Requirement</span></span> | <span data-ttu-id="14e6b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e6b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14e6b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14e6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14e6b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14e6b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14e6b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14e6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14e6b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14e6b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




