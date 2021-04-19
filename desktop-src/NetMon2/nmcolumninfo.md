---
description: La structure NMCOLUMNINFO définit une colonne dans le volet supérieur de la observateur d’événements.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: NMCOLUMNINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525729"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="060ea-103">NMCOLUMNINFO, structure</span><span class="sxs-lookup"><span data-stu-id="060ea-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="060ea-104">La structure **NMCOLUMNINFO** définit une colonne dans le volet supérieur de la observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="060ea-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="060ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="060ea-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="060ea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="060ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="060ea-107">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="060ea-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="060ea-108">Nom affichable d’une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="060ea-108">Displayable name of a specific column.</span></span> <span data-ttu-id="060ea-109">Si le nom est trop long, il ne sera pas complètement visible dans la configuration de observateur d’événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="060ea-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="060ea-110">**VariantData**</span><span class="sxs-lookup"><span data-stu-id="060ea-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="060ea-111">Données insérées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="060ea-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="060ea-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="060ea-112">Requirements</span></span>



| <span data-ttu-id="060ea-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="060ea-113">Requirement</span></span> | <span data-ttu-id="060ea-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="060ea-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="060ea-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="060ea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="060ea-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="060ea-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="060ea-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="060ea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="060ea-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="060ea-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="060ea-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="060ea-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="060ea-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="060ea-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




