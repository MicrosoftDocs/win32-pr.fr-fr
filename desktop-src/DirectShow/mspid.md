---
description: Notez que cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser. Le type de données MSPID identifie l’objectif d’un flux de média.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537804"
---
# <a name="mspid"></a><span data-ttu-id="b6746-105">MSPID</span><span class="sxs-lookup"><span data-stu-id="b6746-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="b6746-106">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b6746-106">This API is deprecated.</span></span> <span data-ttu-id="b6746-107">Les nouvelles applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b6746-107">New applications should not use it.</span></span>

 

<span data-ttu-id="b6746-108">Le type de données **MSPID** identifie l’objectif d’un flux de média.</span><span class="sxs-lookup"><span data-stu-id="b6746-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="b6746-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b6746-109">Remarks</span></span>

<span data-ttu-id="b6746-110">**MSPID** est simplement un typedef pour GUID.</span><span class="sxs-lookup"><span data-stu-id="b6746-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="b6746-111">Les MSPIDs suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="b6746-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="b6746-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6746-112">Value</span></span>               | <span data-ttu-id="b6746-113">Description</span><span class="sxs-lookup"><span data-stu-id="b6746-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="b6746-114">MSPID \_ PrimaryVideo</span><span class="sxs-lookup"><span data-stu-id="b6746-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="b6746-115">Flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b6746-115">Primary video stream.</span></span> |
| <span data-ttu-id="b6746-116">MSPID \_ PrimaryAudio</span><span class="sxs-lookup"><span data-stu-id="b6746-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="b6746-117">Flux audio principal.</span><span class="sxs-lookup"><span data-stu-id="b6746-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="b6746-118">Le type **REFMSPID** définit une référence à un **MSPID**.</span><span class="sxs-lookup"><span data-stu-id="b6746-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6746-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6746-119">Requirements</span></span>



| <span data-ttu-id="b6746-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6746-120">Requirement</span></span> | <span data-ttu-id="b6746-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6746-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6746-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6746-122">Header</span></span><br/> | <dl> <span data-ttu-id="b6746-123"><dt>Mmstream. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6746-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6746-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6746-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6746-125">Types de données de diffusion multimédia</span><span class="sxs-lookup"><span data-stu-id="b6746-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




