---
description: Cette classe est la classe de type d’événement pour les événements d’e/s fractionnées. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: Classe SplitIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867981"
---
# <a name="splitio_info-class"></a><span data-ttu-id="004d7-104">\_Classe SplitIo info</span><span class="sxs-lookup"><span data-stu-id="004d7-104">SplitIo\_Info class</span></span>

<span data-ttu-id="004d7-105">Cette classe est la classe de type d’événement pour les événements d’e/s fractionnées.</span><span class="sxs-lookup"><span data-stu-id="004d7-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="004d7-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="004d7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="004d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="004d7-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="004d7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="004d7-108">Members</span></span>

<span data-ttu-id="004d7-109">La classe **SplitIo \_ info** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="004d7-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="004d7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="004d7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="004d7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="004d7-111">Properties</span></span>

<span data-ttu-id="004d7-112">La classe **SplitIo \_ info** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="004d7-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="004d7-113">**ChildIrp**</span><span class="sxs-lookup"><span data-stu-id="004d7-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004d7-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="004d7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="004d7-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="004d7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="004d7-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="004d7-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="004d7-117">Paquet de demande d’e/s enfant.</span><span class="sxs-lookup"><span data-stu-id="004d7-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="004d7-118">**ParentIrp**</span><span class="sxs-lookup"><span data-stu-id="004d7-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004d7-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="004d7-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="004d7-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="004d7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="004d7-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="004d7-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="004d7-122">Paquet de demande d’e/s parente.</span><span class="sxs-lookup"><span data-stu-id="004d7-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="004d7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="004d7-123">Remarks</span></span>

<span data-ttu-id="004d7-124">Indique que le gestionnaire de volume divise l’IRP en deux IRP.</span><span class="sxs-lookup"><span data-stu-id="004d7-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="004d7-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="004d7-125">Requirements</span></span>



| <span data-ttu-id="004d7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="004d7-126">Requirement</span></span> | <span data-ttu-id="004d7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="004d7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="004d7-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="004d7-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004d7-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="004d7-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="004d7-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004d7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




