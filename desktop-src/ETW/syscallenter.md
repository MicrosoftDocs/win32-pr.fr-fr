---
description: Cette classe est la classe de type d’événement pour les événements d’entrée d’appel système. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: SysCallEnter, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973411"
---
# <a name="syscallenter-class"></a><span data-ttu-id="91b5c-104">SysCallEnter, classe</span><span class="sxs-lookup"><span data-stu-id="91b5c-104">SysCallEnter class</span></span>

<span data-ttu-id="91b5c-105">Cette classe est la classe de type d’événement pour les événements d’entrée d’appel système.</span><span class="sxs-lookup"><span data-stu-id="91b5c-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="91b5c-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="91b5c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b5c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91b5c-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="91b5c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="91b5c-108">Members</span></span>

<span data-ttu-id="91b5c-109">La classe **SysCallEnter** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="91b5c-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="91b5c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91b5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91b5c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91b5c-111">Properties</span></span>

<span data-ttu-id="91b5c-112">La classe **SysCallEnter** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="91b5c-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91b5c-113">**SysCallAddress**</span><span class="sxs-lookup"><span data-stu-id="91b5c-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91b5c-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91b5c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91b5c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91b5c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91b5c-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="91b5c-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91b5c-117">Adresse de l’appel de fonction NT en cours d’entrée.</span><span class="sxs-lookup"><span data-stu-id="91b5c-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91b5c-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="91b5c-118">Requirements</span></span>



| <span data-ttu-id="91b5c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91b5c-119">Requirement</span></span> | <span data-ttu-id="91b5c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b5c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91b5c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91b5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91b5c-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91b5c-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91b5c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91b5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91b5c-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91b5c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




