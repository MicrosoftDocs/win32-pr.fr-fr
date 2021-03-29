---
description: Cette classe est la classe de type d’événement pour les événements d’attente de fin ALPC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Classe ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527057"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="9e266-104">\_Classe d’inattente ALPC</span><span class="sxs-lookup"><span data-stu-id="9e266-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="9e266-105">Cette classe est la classe de type d’événement pour les événements d’attente de fin ALPC.</span><span class="sxs-lookup"><span data-stu-id="9e266-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="9e266-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="9e266-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e266-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e266-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="9e266-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9e266-108">Members</span></span>

<span data-ttu-id="9e266-109">La classe d' **\_ inattente ALPC** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e266-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="9e266-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e266-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e266-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e266-111">Properties</span></span>

<span data-ttu-id="9e266-112">La classe de **\_ désattente ALPC** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9e266-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e266-113">**État**</span><span class="sxs-lookup"><span data-stu-id="9e266-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e266-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e266-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e266-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e266-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e266-116">État à partir de l’opération d’attente.</span><span class="sxs-lookup"><span data-stu-id="9e266-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e266-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9e266-117">Requirements</span></span>



| <span data-ttu-id="9e266-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e266-118">Requirement</span></span> | <span data-ttu-id="9e266-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e266-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e266-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e266-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e266-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e266-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e266-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e266-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e266-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e266-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




