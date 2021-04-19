---
description: Stocke des informations sur les sections de la mémoire partagée.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Structure SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529311"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="fe52f-103">\_Structure d’en-tête SHAREDMEMORY</span><span class="sxs-lookup"><span data-stu-id="fe52f-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="fe52f-104">Stocke des informations sur les sections de la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="fe52f-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe52f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe52f-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="fe52f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fe52f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe52f-107">**cbTotal**</span><span class="sxs-lookup"><span data-stu-id="fe52f-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-108">Taille, en octets, des données référencées par cette structure d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="fe52f-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-109">**cbOffsetSns**</span><span class="sxs-lookup"><span data-stu-id="fe52f-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-110">Taille, en octets, du décalage des numéros de série par rapport à la structure d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="fe52f-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-111">**idxEvent**</span><span class="sxs-lookup"><span data-stu-id="fe52f-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-112">Index d’événements.</span><span class="sxs-lookup"><span data-stu-id="fe52f-112">The event index.</span></span> <span data-ttu-id="fe52f-113">Cette valeur est incrémentée avec des événements successifs.</span><span class="sxs-lookup"><span data-stu-id="fe52f-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-114">**dwEvent**</span><span class="sxs-lookup"><span data-stu-id="fe52f-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-115">Événement associé à cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="fe52f-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-116">**confirmation**</span><span class="sxs-lookup"><span data-stu-id="fe52f-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-117">Identificateur de curseur référencé par l’en-tête de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="fe52f-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="fe52f-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-119">Numéro de série de l’en-tête de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="fe52f-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-120">**sysEvt**</span><span class="sxs-lookup"><span data-stu-id="fe52f-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-121">Événement système, préfixe SE \_ \* , associé à cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="fe52f-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="fe52f-122">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fe52f-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-123">**sysEvtData**</span><span class="sxs-lookup"><span data-stu-id="fe52f-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-124">Structure [**de \_ \_ données d’événement système**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associée à l’événement système.</span><span class="sxs-lookup"><span data-stu-id="fe52f-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-125">**cPackets**</span><span class="sxs-lookup"><span data-stu-id="fe52f-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-126">Nombre de paquets associés à la mémoire partagée en cours.</span><span class="sxs-lookup"><span data-stu-id="fe52f-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-127">**cbPackets**</span><span class="sxs-lookup"><span data-stu-id="fe52f-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-128">Taille, en octets, des paquets associés à la section de la mémoire partagée actuelle.</span><span class="sxs-lookup"><span data-stu-id="fe52f-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="fe52f-129">**fSnsPresent**</span><span class="sxs-lookup"><span data-stu-id="fe52f-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="fe52f-130">Indicateur qui spécifie si les numéros de série sont présents dans la section de la mémoire partagée actuelle.</span><span class="sxs-lookup"><span data-stu-id="fe52f-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe52f-131">Notes</span><span class="sxs-lookup"><span data-stu-id="fe52f-131">Remarks</span></span>

<span data-ttu-id="fe52f-132">Les valeurs suivantes sont définies pour le membre **sysEvt** .</span><span class="sxs-lookup"><span data-stu-id="fe52f-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="fe52f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe52f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe52f-134">**\_données d’événement système \_**</span><span class="sxs-lookup"><span data-stu-id="fe52f-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



