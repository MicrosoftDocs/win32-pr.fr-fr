---
description: La \_ structure de mappage PID contient identifie le contenu d’un ID de paquet de flux de transport MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Structure PID_MAP (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541713"
---
# <a name="pid_map-structure"></a><span data-ttu-id="a67a3-103">Structure de la \_ carte PID</span><span class="sxs-lookup"><span data-stu-id="a67a3-103">PID\_MAP structure</span></span>

<span data-ttu-id="a67a3-104">La `PID_MAP` structure contient identifie le contenu d’un ID de paquet de flux de transport MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a67a3-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a67a3-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="a67a3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a67a3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a67a3-107">**ulPID**</span><span class="sxs-lookup"><span data-stu-id="a67a3-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="a67a3-108">Spécifie l’ID de paquet (PID)</span><span class="sxs-lookup"><span data-stu-id="a67a3-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="a67a3-109">**MediaSampleContent**</span><span class="sxs-lookup"><span data-stu-id="a67a3-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="a67a3-110">Spécifie le contenu de la charge utile du paquet, sous la forme d’un exemple de type d’énumération de [**\_ \_ contenu multimédia**](media-sample-content.md) .</span><span class="sxs-lookup"><span data-stu-id="a67a3-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a67a3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a67a3-111">Requirements</span></span>



| <span data-ttu-id="a67a3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a67a3-112">Requirement</span></span> | <span data-ttu-id="a67a3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67a3-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a67a3-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="a67a3-114">Header</span></span><br/> | <dl> <span data-ttu-id="a67a3-115"><dt>Bdatypes. h (inclure Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a67a3-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67a3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a67a3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67a3-117">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="a67a3-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="a67a3-118">**Interface IEnumPIDMap**</span><span class="sxs-lookup"><span data-stu-id="a67a3-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




