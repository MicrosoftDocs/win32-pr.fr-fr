---
description: Cette classe est la classe de type d’événement pour les événements de retour d’appel de fonction principale du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: DriverMajorFunctionReturn, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525251"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="d57b2-104">DriverMajorFunctionReturn, classe</span><span class="sxs-lookup"><span data-stu-id="d57b2-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="d57b2-105">Cette classe est la classe de type d’événement pour les événements de retour d’appel de fonction principale du pilote.</span><span class="sxs-lookup"><span data-stu-id="d57b2-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="d57b2-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d57b2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57b2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d57b2-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="d57b2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d57b2-108">Members</span></span>

<span data-ttu-id="d57b2-109">La classe **DriverMajorFunctionReturn** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d57b2-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="d57b2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d57b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d57b2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d57b2-111">Properties</span></span>

<span data-ttu-id="d57b2-112">La classe **DriverMajorFunctionReturn** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d57b2-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d57b2-113">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="d57b2-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d57b2-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d57b2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d57b2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d57b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d57b2-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="d57b2-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d57b2-117">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="d57b2-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="d57b2-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="d57b2-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d57b2-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d57b2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d57b2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d57b2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d57b2-121">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="d57b2-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d57b2-122">Identificateur qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="d57b2-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="d57b2-123">Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="d57b2-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d57b2-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d57b2-124">Requirements</span></span>



| <span data-ttu-id="d57b2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57b2-125">Requirement</span></span> | <span data-ttu-id="d57b2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57b2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d57b2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57b2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d57b2-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57b2-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d57b2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57b2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d57b2-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57b2-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d57b2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d57b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57b2-132">**E**</span><span class="sxs-lookup"><span data-stu-id="d57b2-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




