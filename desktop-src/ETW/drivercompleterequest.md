---
description: Cette classe est la classe de type d’événement pour les événements de requête complète du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: DriverCompleteRequest, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971947"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="28806-104">DriverCompleteRequest, classe</span><span class="sxs-lookup"><span data-stu-id="28806-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="28806-105">Cette classe est la classe de type d’événement pour les événements de requête complète du pilote.</span><span class="sxs-lookup"><span data-stu-id="28806-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="28806-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="28806-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="28806-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28806-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="28806-108">Membres</span><span class="sxs-lookup"><span data-stu-id="28806-108">Members</span></span>

<span data-ttu-id="28806-109">La classe **DriverCompleteRequest** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="28806-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="28806-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28806-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28806-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28806-111">Properties</span></span>

<span data-ttu-id="28806-112">La classe **DriverCompleteRequest** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="28806-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28806-113">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="28806-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28806-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28806-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28806-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28806-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28806-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="28806-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="28806-117">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="28806-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="28806-118">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="28806-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28806-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28806-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28806-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28806-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28806-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="28806-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="28806-122">Adresse de la fonction de pilote appelée.</span><span class="sxs-lookup"><span data-stu-id="28806-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="28806-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="28806-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28806-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28806-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28806-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28806-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28806-126">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="28806-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="28806-127">Identificateur qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="28806-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="28806-128">Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .</span><span class="sxs-lookup"><span data-stu-id="28806-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28806-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28806-129">Requirements</span></span>



| <span data-ttu-id="28806-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28806-130">Requirement</span></span> | <span data-ttu-id="28806-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="28806-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28806-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28806-132">Minimum supported client</span></span><br/> | <span data-ttu-id="28806-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28806-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28806-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28806-134">Minimum supported server</span></span><br/> | <span data-ttu-id="28806-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28806-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28806-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28806-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28806-137">**E**</span><span class="sxs-lookup"><span data-stu-id="28806-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




